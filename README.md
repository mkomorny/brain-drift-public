# Brain Drift

> **Tri-Platform Agent Skill** for Claude Desktop / Code, Grok CLI, and Google Antigravity / Gemini.  
> Codebase vs Memory Rule Auditor — Detects drift between codebase implementation and Second Brain records, checking if recent code violates rules or if code changes made memories obsolete.

---

## Overview

`brain-drift` provides standardized capabilities across conversational AI platforms:
- Bidirectional drift detection (code violates brain constraints vs brain records are obsolete).
- AST and pattern matching against documented architecture constraints.
- Actionable drift report with recommended memory updates or code refactors.
- Tri-platform NTFS junctions connecting Claude, Grok, and Antigravity.
- Standard documentation suite: SKILL.md, HOW_TO_USE.txt, IMPLEMENTATION_PLAN.md, and README.md.

---

## Tri-Platform Architecture

Zero duplicate code across platforms. Canonical source resides in `.agents`:
- **Canonical Source**: `C:\Users\<you>\.agents\skills\brain-drift`
- **Claude**: `C:\Users\<you>\.claude\skills\brain-drift` (NTFS Junction)
- **Grok**: `C:\Users\<you>\.grok\skills\brain-drift` (NTFS Junction)
- **Antigravity**: `C:\Users\<you>\.gemini\config\skills\brain-drift` (NTFS Junction)

---

## Documentation Suite

- [`HOW_TO_USE.txt`](HOW_TO_USE.txt): Standardized user guide and prompt templates.
- [`IMPLEMENTATION_PLAN.md`](IMPLEMENTATION_PLAN.md): Feature checklist and roadmap.
- [`App Changes Tracker.html`](App%20Changes%20Tracker.html): Interactive visual version log.
- [`SKILL.md`](SKILL.md): Agent system instructions and triggers.
