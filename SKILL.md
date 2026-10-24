---
name: brain-drift
description: >-
  Detects drift between your codebase and Second Brain. Checks if recent code violates
  established Second Brain rules/constraints, or if code changes have rendered existing
  memories obsolete, contradictory, or inaccurate.
---

# Brain Drift — Code vs. Memory Alignment Checker (`/brain-drift`)

Use this skill to audit whether your codebase has drifted away from your documented architectural rules, or whether your Second Brain contains obsolete instructions that no longer reflect your real code.

---

## What Happens When Invoked

When `/brain-drift` is triggered, execute these steps:

### Step 1: Fetch Canonical Project Constraints from Brain
1. Query `second-brain` using `recall` for the active project's rules:
   - Example: `"Canonical rules, technical constraints, port allocations, and architecture standards for [project]"`
2. Extract all explicit constraints (e.g. "Do not patch Producer Pal files", "Live 12 Standard compatibility only", "settings.json must live in project root", "WebSocket on port 8080").

### Step 2: Inspect Current Codebase
1. Scan project source code, configuration files, and dependencies to check for compliance against those rules.
2. Flag any **Rule Violations**:
   - Code pattern violates a durable constraint recorded in the brain.

### Step 3: Check for Obsolete Memories
1. Inspect whether recent commits, file renames, or refactors contradict older memories:
   - e.g. Memory says "App uses Axios", but code now uses native `fetch`.
   - e.g. Memory points to an old file path that was deleted or relocated.
2. Flag any **Stale Memories**:
   - Second Brain entries that should be updated or marked `deprecated`.

### Step 4: Present Alignment Matrix & Remediation
Output a 2-sided alignment report:
- ⚠️ **Code Violating Rules**: Specific lines/files that break documented standards.
- 🔄 **Brain Memories Needing Update**: Memories that are now out of date, with recommended `/brain-update` or `/brain status <id> deprecated` commands.

---

## Syntax

```
/brain-drift [optional project name]
```

## Examples

```
/brain-drift
/brain-drift Live Actions
```
