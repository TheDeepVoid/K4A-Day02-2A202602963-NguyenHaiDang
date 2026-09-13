# Project Instructions for OpenCode

These rules are automatically injected into every conversation in this workspace.
They persist across model swaps because they are loaded from config, not from model memory.

---

## 1. Project Context

- This is a **K4A Day 02 lab assignment** repo for student **2A202602963 - Nguyen Hai Dang**.
- The repo contains Vietnamese-language Markdown deliverables, not software source code.
- The assignment is about identifying good problems for AI, designing workflows, and writing a Problem Statement.

### Directory Structure (do not modify)

```
Day02-2A202602963-NguyenHaiDang/
├── README.md                          # Repo overview (instructor-provided)
├── 01-worksheet.md                    # Lab guide (instructor-provided, READ-ONLY)
├── 02-deliverable-example.md          # Example submission (instructor-provided, READ-ONLY)
├── 01-individual-problem-scan/        # Individual work
├── 02-group-problem-statement/        # Group deliverable (shared with team)
└── 03-individual-reflection/          # Personal reflection
```

### File Naming Convention

Supplementary files follow the pattern: `{section-prefix}-{descriptive-name}.{ext}`

Examples:
- `01-individual-problem-scan-workflow-card-1.png`
- `02-group-problem-statement-research-notes.md`

---

## 2. Language & Format Rules

- **All content must be written in Vietnamese**, matching the existing repo language.
- Use proper **GitHub-Flavored Markdown**: ATX headings (`#`), fenced code blocks, pipe tables.
- Preserve the existing heading hierarchy within each file.
- Use Mermaid syntax for workflow diagrams when appropriate.
- Tables must have proper alignment and be readable in plain text.

---

## 3. Forbidden Actions

### Content Integrity (Critical)

- **NEVER write AI-generated content for reflection or personal-thinking sections.**
  The assignment principle states: "Tự làm trước, AI sau" and "AI hỗ trợ, không thay quyết định."
  Sections in `03-individual-reflection/` and personal pitch/challenge parts must be written by the student.
- When asked to help with these sections, provide **scaffolding only** (headings, bullet prompts, questions to consider) — never substantive answers.

### Structural Integrity

- Do NOT delete or rename `01-individual-problem-scan/`, `02-group-problem-statement/`, or `03-individual-reflection/`.
- Do NOT modify `01-worksheet.md` or `02-deliverable-example.md` — these are instructor-provided templates.
- Do NOT modify `README.md` unless the student explicitly requests it.

### Forbidden Operations

- No `rm -rf` or recursive deletion of any kind.
- No `git push --force` or `git reset --hard`.
- No execution of downloaded scripts (`curl | sh`, `wget | sh`).
- No `sudo` commands.
- No modification of `.git/` internals.

---

## 4. Output Format Rules

- **Always explain what will change before making any edit.** State which file, which section, and what the change accomplishes.
- When suggesting content, **clearly distinguish** between:
  - Structural scaffolding (headings, table templates, placeholder prompts) — AI can generate this.
  - Substantive content (analysis, reflection, personal opinion) — student must write this.
- Use a clear marker like `[Student fills in]` for sections the student must complete themselves.
- Keep responses concise; this is a CLI environment, not a document editor.

---

## 5. Collaboration Context

- `02-group-problem-statement/` is a **shared group deliverable** (3-4 students work together).
- When editing files in this directory, flag that changes affect the shared group submission.
- Each student copies the final group version into their personal repo.

---

## 6. Quality Standards

- Problem Cards must include: Actor, Workflow (before/after), Bottleneck, Metric.
- Workflow diagrams should show clear before/after comparisons.
- Problem Statements must follow the format in `02-deliverable-example.md`.
- The Go / Not Yet / No-Go decision must be justified with evidence, not just stated.
