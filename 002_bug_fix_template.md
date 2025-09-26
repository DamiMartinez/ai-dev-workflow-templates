# AI Bug Fix Template

> **About This Template:** This template provides a structured approach to identifying, analyzing, and resolving bugs with the assistance of an AI agent. Following this process ensures that bugs are fixed systematically and reduces the risk of introducing new issues.

---

## 1. Bug Identification

### Bug Title
**Title:** [Brief, descriptive title of the bug - e.g., "User Logout Fails on Safari" or "Incorrect Calculation in Reporting Module"]

### Bug Classification
- **Severity:** [Critical, High, Medium, Low]
- **Type:** [Functional, Performance, UI/UX, Data]

### Bug Description
**Description:** [Detailed description of the bug, including what is happening, what should be happening, and the impact on the user or system.]

### Steps to Reproduce
**Steps:**
1. [First step to reproduce the bug]
2. [Second step to reproduce the bug]
3. [Third step to reproduce the bug]
...

### Environment
- **Operating System:** [e.g., Windows, macOS, Linux]
- **Browser (if applicable):** [e.g., Chrome, Firefox, Safari, Edge]
- **App Version/Commit:** [The version or commit hash where the bug was observed]
- **Dependencies:** [Python/Node version if relevant]

---

## 2. Analysis and Diagnosis

### Initial Analysis
[Initial thoughts on the potential cause of the bug. This is where the AI can start its investigation.]

### Relevant Files
[List of files that might be related to the bug. The AI can use this as a starting point for its code analysis.]

### Error Messages
[Any error messages from logs, console, or user reports that are relevant to the bug.]

---

## 3. Proposed Fix

### Root Cause
[A clear explanation of the root cause of the bug, based on the analysis.]

### Proposed Changes
[A detailed description of the code changes required to fix the bug. This should include file names and specific code modifications.]

### Deliverables
- A Git commit with the bug fix, following the project's commit conventions.
- The commit message should clearly describe the bug and the fix.

---

## 4. Implementation and Verification

### Implementation Steps
1. **Code Changes:** Apply the proposed code changes on the current branch.
2. **Testing (On-Demand):**
    - Do not run any tests or start any servers/applications by default. Assume they are already running.
    - If requested by the user, perform specific tests.
    - **Unit Tests:** If requested, add or update unit tests to cover the bug fix.
    - **Integration Tests:** If requested, run integration tests to ensure the fix doesn't break other parts of the system.
    - **Manual Testing:** If requested, manually verify that the bug is resolved by following the reproduction steps. Assume the server and/or app are up and running.

### Verification
- [ ] The bug is no longer reproducible (if tested).
- [ ] All relevant tests pass (if tested).
- [ ] The fix does not introduce any new bugs (regression testing, if performed).

### Quick Checklist
- [ ] Bug reproduced locally
- [ ] Root cause identified
- [ ] Fix implemented
- [ ] Code formatted with appropriate formatter
- [ ] Fix tested (if requested by user)
- [ ] No regressions introduced (if tested)

---

## 5. AI Agent Instructions

### Implementation Workflow
🎯 **MANDATORY PROCESS:**
1.  **Information Gathering:** Before starting, ensure the user has provided all necessary information in the "Bug Identification" section. If any information is missing, ask the user for it.
2.  **Virtual Environment:** Always activate the project's virtual environment before starting any work (e.g., `ai-env`, `source venv/bin/activate`, `conda activate`, etc.).
3.  **Analysis:** Analyze the provided bug description, steps to reproduce, and relevant files to understand the issue. Trust the user's assessment of what is already working and focus the investigation on the described problem, unless additional checks are necessary to understand the full context. Use all available project resources, including examples in the project's references folder. For potential library version issues, consult the `context7` mcp server if available. Check for similar bugs in recent commits.
4.  **Propose Fix:** Propose a fix based on the analysis.
5.  **Confirmation:** Present the proposed fix to the user and get their confirmation before proceeding.
6.  **Implement Fix:** Implement the fix as per the proposed changes on the current branch.
7.  **Verify Fix (On-Demand):** Do not run tests or perform verification unless explicitly instructed by the user. If asked to test, assume any required servers or applications are already running.
8.  **Code Formatting:** Run the appropriate code formatter for the project (e.g., `poetry run black .`, `npm run format`, `prettier --write .`, etc.).

### Communication Preferences
- Provide regular updates on the progress of the bug fix.
- Clearly communicate the root cause and the proposed solution before implementing the fix.
- Report any issues or blockers encountered during the process.