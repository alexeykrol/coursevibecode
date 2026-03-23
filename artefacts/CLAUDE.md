# Udemy Course Transcript Extraction Project

## Goal

Create local copies of Udemy course content (transcripts, screenshots, resources) in structured Markdown for later condensation and analysis.

---

## Autonomy Policy

**Work fully autonomously.** Once the user gives a course URL or says "start", process the entire course end-to-end without asking for confirmation at each step. Only interrupt the user if:

- Udemy requires re-login (session expired, access denied).
- A lecture type is completely unknown and cannot be handled by any edge-case rule below.
- A critical tool failure persists after 2-3 retry attempts.

Everything else — navigating between lectures, activating transcripts, extracting text, taking screenshots, creating folders and files, building index and summary — must be done silently and autonomously. Report back only when the entire course (or all assigned courses) is complete, with a brief summary of what was done.

When processing multiple courses in one session, finish one course completely before moving to the next.

---

## How to Start a New Course

When the user provides a new Udemy course URL or opens a course tab in Chrome:

1. **Read this entire file** to understand the methodology.
2. **Create the course folder** using the naming convention below.
3. **Gather the course structure** — open the course page, extract all sections and lectures from the "Course content" sidebar, save as `00-course-index.md` (initially without descriptions — fill them in as lectures are processed).
4. **Process each lecture sequentially** — open it, activate transcript, extract text, check for resources, take screenshots of key visuals, save as individual Markdown files.
5. **Finalize the index** — go back to `00-course-index.md` and add one-line descriptions for each lecture now that content is known.
6. **Create `00-course-summary.md`** — write a condensed thesis-style summary of the entire course with links to lecture files.
7. **Update `README.md`** at the repository root with the new course entry.
8. **Update the course table** below with the course status.

---

## Active Courses

<!-- Add courses here as they are assigned. Update status as work progresses. -->

| # | Course Name | Udemy Slug | Folder | Status |
|---|-------------|------------|--------|--------|
| 1 | Claude Code Beginner Crash Course | `claudecode` | `Course-01-Claude-Code-Crash-Course` | Complete |
| 2 | Claude Code Beginner to Pro | `learn-claude-code` | `Course-02-Claude-Code-Beginner-to-Pro` | Complete |
| 3 | Claude, Claude Code, Cowork & MS Office | `claude-ai` | `Course-03-Claude-Cowork-MS-Office` | Complete |

---

## Folder Structure

```
/Udemy/
  CLAUDE.md                              ← This file (project instructions)
  .claude/
    settings.local.json                  ← Claude Code / Cowork permissions
  README.md                              ← Top-level README for GitHub
  .gitignore                             ← Exclude .claude/, .DS_Store, etc.
  Course-XX-Short-Name/
    00-course-index.md                   ← Full TOC: sections, lectures, durations
    00-course-summary.md                 ← Condensed summary of the entire course
    screenshots/                         ← All screenshots for this course
      SXX-LXX-description.png
    Section-XX-Name/
      XX-Lecture-Title.md                ← One file per lecture
```

### Naming Conventions

| Element | Pattern | Example |
|---------|---------|---------|
| Course folder | `Course-XX-Short-Name` | `Course-01-Claude-Code-Crash-Course` |
| Section folder | `Section-XX-Short-Name` | `Section-03-The-GIST-of-Claude-Code` |
| Lecture file | `XX-Lecture-Title.md` | `01-Course-Objectives.md` |
| Screenshot | `SXX-LXX-description.png` | `S01-L01-course-objectives-slide.png` |

Rules: hyphens instead of spaces, no special characters, concise but recognizable names.

---

## Lecture File Template

Every lecture transcript file must follow this structure:

```markdown
# <Lecture Title>

**Course:** <Full Course Name>
**Section:** <Section #> — <Section Name>
**Lecture:** <Lecture #>
**Duration:** <Duration>
**URL:** <Full Udemy lecture URL>

---

## Transcript

<Full transcript text, cleaned up for readability.>
<Paragraphs separated by blank lines.>
<Remove timestamps unless they add value.>

---

## Screenshots

<!-- Include only if lecture has important visuals -->
![Description](../screenshots/SXX-LXX-description.png)

---

## Resources & Links

<!-- Downloadable files, external links mentioned in the lecture -->
- [Resource name](URL)

---

## Notes

<!-- Editorial notes, observations, key takeaways, flags for processing -->
```

---

## Extraction Workflow (Chrome via Cowork / Claude in Chrome)

### Prerequisites

- Chrome browser open with the Claude in Chrome extension connected.
- User logged into Udemy with access to the course.
- A tab group created via `tabs_context_mcp(createIfEmpty: true)`.

### Step 1: Gather Course Structure

1. Navigate to the first lecture of the course.
2. The right sidebar shows "Course content" with all sections and lectures.
3. Use `read_page` on the sidebar to extract the full list.
4. If not all sections are visible, expand them by clicking each section header.
5. Save the extracted TOC as `00-course-index.md` in the course folder.

### Step 2: Open a Lecture

1. Navigate to the lecture URL via `navigate(url, tabId)`.
2. Wait 2-3 seconds for the page to load: `computer(action: "wait", duration: 3)`.

### Step 3: Activate Transcript

**This must be done for every lecture — transcripts don't carry over.**

1. Use `find("transcript button")` to locate the Transcript button in the DOM.
2. Click the button by its `ref`: `computer(action: "left_click", ref: "<ref_id>")`.
3. The transcript panel opens on the right side, replacing "Course content".

> **Key insight**: The Transcript button is always in the DOM and clickable via `ref`, even when the video control bar is visually hidden. No hover needed — just `find` → click.

### Step 4: Extract Transcript Text

1. Use `get_page_text(tabId)` to capture the full page text including the transcript.
2. Alternatively, use `read_page(tabId)` and focus on the transcript panel element for cleaner output.
3. If transcript is long, scroll the transcript panel to ensure all text is loaded.
4. Clean up: remove timestamps, fix line breaks, separate into logical paragraphs.

### Step 5: Check for Resources

1. Look for a "Resources" button/dropdown next to the lecture title in the sidebar.
2. It appears as a small button, sometimes with a folder icon.
3. If present, click it and record any downloadable files or external links.

### Step 6: Take Screenshots (When Needed)

Take screenshots when the lecture displays:
- Presentation slides with key information
- Architecture diagrams or flowcharts
- Code examples that are being demonstrated
- Important UI demonstrations

How to capture:
1. Pause the video (click on the video area or press Space).
2. `computer(action: "screenshot", save_to_disk: true, tabId)` — saves to disk.
3. Copy the saved file to `screenshots/SXX-LXX-description.png`.
4. Reference it in the lecture Markdown.

### Step 7: Save and Move On

1. Assemble the Markdown file using the template.
2. Write it to the correct Section folder.
3. Navigate to the next lecture and repeat from Step 2.

---

## Handling Edge Cases

| Situation | Action |
|-----------|--------|
| Lecture has no transcript | Create the .md file anyway, note "No transcript available" in the Transcript section |
| Lecture is a quiz or exercise | Create a minimal .md file noting the type ("Quiz", "Coding Exercise", etc.) |
| Transcript panel shows "Course content" tab instead | Click on the "Transcript" tab at the top of the sidebar panel |
| Transcript text is auto-scrolling with video | Uncheck "Autoscroll" checkbox at the bottom of the transcript panel, then scroll manually |
| Page requires re-login | Pause and notify the user |
| Very long transcript | Extract in chunks by scrolling the transcript panel |

---

## Final Deliverables (Per Course)

After all lectures are extracted, create two summary files in the course folder:

### 1. `00-course-index.md` — Index File

Full table of contents with short descriptions of every lecture. Format:

```markdown
# <Course Name> — Index

| # | Section | Lecture | Duration | Description | File |
|---|---------|---------|----------|-------------|------|
| 1 | Section 1 — Intro | Course Objectives | 8 min | Overview of course goals and structure | [Link](Section-01-Intro/01-Course-Objectives.md) |
| 2 | Section 1 — Intro | About Me | 1 min | Instructor background | [Link](Section-01-Intro/02-About-Me.md) |
| ... | ... | ... | ... | ... | ... |
```

The "Description" column is a **one-line summary** of what the lecture covers. Links point to the actual transcript files using relative paths.

### 2. `00-course-summary.md` — Condensed Course Summary

A concise, thesis-style overview of the entire course — designed for quick review. Structure:

```markdown
# <Course Name> — Summary

## Course Overview
<2-3 sentences: what the course teaches, who it's for, what you'll be able to do after.>

## Key Takeaways by Section

### Section 1: <Name>
- <Key point 1> → [Lecture 1](Section-01/01-Name.md)
- <Key point 2> → [Lecture 2](Section-01/02-Name.md)

### Section 2: <Name>
- <Key point 1> → [Lecture 3](Section-02/03-Name.md)
...

## Core Concepts & Terms
<Bullet list of the main concepts, frameworks, tools, or vocabulary introduced in the course.>

## Practical Exercises & Projects
<Summary of any hands-on work, coding exercises, projects, or quizzes in the course.>
```

Every key point must link back to the corresponding lecture transcript file.

---

## GitHub Preparation

The repository must be clean and ready for `git push`. Before pushing:

### `README.md` (root level)

Auto-generated overview of the entire repository:

```markdown
# Udemy Course Transcripts

Structured transcripts and summaries of Udemy courses on Claude Code and AI workflows.

## Courses

| # | Course | Lectures | Status | Summary |
|---|--------|----------|--------|---------|
| 1 | [Course Name](Course-01-Name/) | XX lectures | Complete | [Summary](Course-01-Name/00-course-summary.md) |
| ... | ... | ... | ... | ... |

## Structure

Each course folder contains:
- `00-course-index.md` — Full index with one-line descriptions and links
- `00-course-summary.md` — Condensed thesis-style summary
- `Section-XX/` folders with individual lecture transcripts
- `screenshots/` — Key visuals from video lectures
```

### `.gitignore`

```
.DS_Store
.claude/
```

The `.claude/` folder (with `settings.local.json`) is local-only and must NOT be committed. `CLAUDE.md` in the root IS committed — it serves as project documentation.

---

## Quality Checklist (Per Course)

- [ ] `00-course-index.md` exists with complete TOC and one-line descriptions
- [ ] `00-course-summary.md` exists with condensed thesis-style overview
- [ ] Every lecture has its own .md file
- [ ] All transcripts are complete (not cut off)
- [ ] Screenshots captured for lectures with important visuals
- [ ] Resources noted where available
- [ ] File naming follows conventions
- [ ] All links in index and summary are valid relative paths
- [ ] Course status updated in the Active Courses table above

## Quality Checklist (Repository)

- [ ] `README.md` exists with course listing and links
- [ ] `.gitignore` excludes `.DS_Store` and `.claude/`
- [ ] No sensitive data or credentials in any file
- [ ] All relative links work correctly
