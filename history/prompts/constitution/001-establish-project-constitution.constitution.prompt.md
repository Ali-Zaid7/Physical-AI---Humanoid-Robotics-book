---
id: 001
title: Establish Project Constitution for Humanoid Robotics Book
stage: constitution
date: 2025-12-26
surface: agent
model: gemini
feature: none
branch: master
user: 
command: /sp.constitution
labels: [constitution, setup]
links:
  spec: "null"
  ticket: "null"
  adr: "null"
  pr: "null"
files:
  - .specify/memory/constitution.md
  - .specify/templates/plan-template.md
tests:
  []
---

## Prompt

/sp.constitution

Project: Humanoid Robotics Book  
Scope: AI, Software Systems, and Embodied Intelligence

Purpose:
Develop a high-quality, spec-driven technical book on humanoid robotics using Spec-Kit Plus and Claude Code. The book must be authored in Docusaurus (with MCP connected via Context7) and deployed to GitHub Pages as the final publishing target.

Core Principles:
- Spec-first execution: every chapter, section, and change must originate from an approved spec
- Technical correctness: all robotics, AI, and software concepts must be accurate and defensible
- Progressive clarity: content must evolve from foundational concepts to advanced topics
- Practical grounding: theory must be reinforced with examples, diagrams, or code
- AI-compatible structure: writing must support automated review, iteration, and validation

Documentation & Writing Standards:
- Target audience: students and practitioners with basic programming knowledge
- Language: precise technical English, concise and unambiguous
- Every chapter must include:
  - Clear learning objectives
  - Conceptual explanation
  - Practical examples or real-world applications
  - A concise summary
- Terminology and naming conventions must remain consistent across the book

Docusaurus Requirements:
- All content must be written in Docusaurus-compatible Markdown
- Pages must include frontmatter metadata (title, description)
- Sidebar structure must reflect a logical learning progression
- Images and diagrams must reside in a dedicated assets directory
- All internal links must be relative, valid, and build-safe

AI & Spec-Kit Plus Governance:
- Spec-Kit Plus is the single source of truth for structure and tasks
- Claude Code may operate only within explicitly defined specs
- No content may be written, edited, or expanded without an associated spec
- Specs must be updated before content changes, never retroactively

Version Control & GitHub Discipline:
- GitHub is the authoritative repository of record
- A commit is mandatory after each completed step, including:
  - Spec creation or modification
  - Chapter or section draft completion
  - Revisions, corrections, or refactors
- Commits must be small, atomic, and descriptively messaged
- Long-lived uncommitted changes are prohibited

Constraints:
- Output format: Docusaurus site deployed via GitHub Pages
- All content must be original and plagiarism-free
- Code examples must be executable or clearly illustrative
- External references must be cited or linked explicitly

Success Criteria:
- The book builds successfully with Docusaurus without errors.
- GitHub Pages deployment is live and accessible.
- Every chapter and section maps directly to an approved spec.
- Content is technically accurate, structured, and readable.
- Git history demonstrates disciplined, incremental progress

## Response snapshot

I have updated the project constitution at `.specify/memory/constitution.md` and modified the `.specify/templates/plan-template.md` to align with the new principles.

## Outcome

- ✅ Impact: Established the project constitution, version 1.0.0.
- 🧪 Tests: None
- 📁 Files: 
  - .specify/memory/constitution.md (created)
  - .specify/templates/plan-template.md (modified)
- 🔁 Next prompts: /sp.specify
- 🧠 Reflection: The process of parsing the user's detailed input and mapping it to the template was successful. The native-agent PHR creation flow was used as the bash script was not present.

## Evaluation notes (flywheel)

- Failure modes observed: None
- Graders run and results (PASS/FAIL): PASS
- Prompt variant (if applicable): None
- Next experiment (smallest change to try): None
