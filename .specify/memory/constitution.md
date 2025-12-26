<!--
Sync Impact Report

- Version change: 0.0.0 → 1.0.0
- List of modified principles:
  - PRINCIPLE_1_NAME -> I. Spec-First Execution
  - PRINCIPLE_2_NAME -> II. Technical Correctness
  - PRINCIPLE_3_NAME -> III. Progressive Clarity
  - PRINCIPLE_4_NAME -> IV. Practical Grounding
  - PRINCIPLE_5_NAME -> V. AI-Compatible Structure
- Added sections:
  - Documentation & Writing Standards
  - Docusaurus Requirements
  - AI & Spec-Kit Plus Governance
  - Version Control & GitHub Discipline
  - Constraints
  - Success Criteria
- Removed sections:
  - PRINCIPLE_6
- Templates requiring updates:
  - ✅ .specify/templates/plan-template.md
  - - .specify/templates/spec-template.md
  - - .specify/templates/tasks-template.md
- Follow-up TODOs: None
-->
# Humanoid Robotics Book Constitution

## Core Principles

### I. Spec-First Execution
Every chapter, section, and change must originate from an approved spec.

### II. Technical Correctness
All robotics, AI, and software concepts must be accurate and defensible.

### III. Progressive Clarity
Content must evolve from foundational concepts to advanced topics.

### IV. Practical Grounding
Theory must be reinforced with examples, diagrams, or code.

### V. AI-Compatible Structure
Writing must support automated review, iteration, and validation.

## Documentation & Writing Standards

- Target audience: students and practitioners with basic programming knowledge
- Language: precise technical English, concise and unambiguous
- Every chapter must include:
  - Clear learning objectives
  - Conceptual explanation
  - Practical examples or real-world applications
  - A concise summary
- Terminology and naming conventions must remain consistent across the book.

## Docusaurus Requirements

- All content must be written in Docusaurus-compatible Markdown.
- Pages must include frontmatter metadata (title, description).
- Sidebar structure must reflect a logical learning progression.
- Images and diagrams must reside in a dedicated assets directory.
- All internal links must be relative, valid, and build-safe.

## AI & Spec-Kit Plus Governance

- Spec-Kit Plus is the single source of truth for structure and tasks.
- Claude Code may operate only within explicitly defined specs.
- No content may be written, edited, or expanded without an associated spec.
- Specs must be updated before content changes, never retroactively.

## Version Control & GitHub Discipline

- GitHub is the authoritative repository of record.
- A commit is mandatory after each completed step, including:
  - Spec creation or modification
  - Chapter or section draft completion
  - Revisions, corrections, or refactors
- Commits must be small, atomic, and descriptively messaged.
- Long-lived uncommitted changes are prohibited.

## Constraints

- Output format: Docusaurus site deployed via GitHub Pages
- All content must be original and plagiarism-free.
- Code examples must be executable or clearly illustrative.
- External references must be cited or linked explicitly.

## Success Criteria

- The book builds successfully with Docusaurus without errors.
- GitHub Pages deployment is live and accessible.
- Every chapter and section maps directly to an approved spec.
- Content is technically accurate, structured, and readable.
- Git history demonstrates disciplined, incremental progress.

## Governance

This constitution guides the development of the Humanoid Robotics Book. All development activities must adhere to these principles and standards. Amendments to this constitution require documentation, review, and approval.

**Version**: 1.0.0 | **Ratified**: 2025-12-26 | **Last Amended**: 2025-12-26