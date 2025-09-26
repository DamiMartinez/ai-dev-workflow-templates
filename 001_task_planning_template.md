# AI Task Planning Template

> **About This Template:** This is a systematic framework for planning and executing technical projects with AI assistance. Use this structure to break down complex features, improvements, or fixes into manageable, trackable tasks that AI agents can execute effectively.

---

## 1. Task Overview

### Task Title
<!-- Give your task a clear, specific name that describes what you're building or fixing -->
**Title:** [Brief, descriptive title - e.g., "Add User Authentication System" or "Fix Payment Integration Bug"]

### Goal Statement
<!-- Write one paragraph explaining what you want to achieve and why it matters for your project -->
**Goal:** [Clear statement of the end result you want and the business/user value it provides]

### Branch Name
<!-- Specify the name of the branch created for this task -->
**Branch:** [e.g., `feat/T-123-add-user-auth` or `fix/T-456-bug-fix`]


---

## 2. Project Analysis & Current State

### Technology & Architecture
<!-- This is where you document your current tech stack so the AI understands your environment -->
- **Frameworks & Versions:** TODO: List your main frameworks and versions (use >= for minimum versions to avoid conflicts)
- **Language:** TODO: Specify your programming language and version
- **Database & ORM:** TODO: Define your database and ORM choice (if applicable)
- **UI & Styling:** TODO: List your UI framework and styling approach (if applicable)
- **Authentication:** TODO: Specify your authentication system (if applicable)
- **Key Architectural Patterns:** TODO: List your main architectural patterns
- **Dependency Management:** TODO: Use minimum version constraints (>=) instead of exact versions (==) to avoid conflicts

### Current State
<!-- Describe what exists today - what's working, what's broken, what's missing -->
[Analysis of your current codebase state, existing functionality, and what needs to be changed]

## 3. Context & Problem Definition

### Problem Statement
<!-- This is where you clearly define the specific problem you're solving -->
[Detailed explanation of the problem, including user impact, pain points, and why it needs to be solved now]

### Success Criteria
<!-- Define exactly how you'll know when this task is complete and successful -->
- [ ] [Specific, measurable outcome 1]
- [ ] [Specific, measurable outcome 2]
- [ ] [Specific, measurable outcome 3]

### Deliverables
- A new task document created in the project's `tasks/` directory (e.g., `tasks/001_add_user_auth.md`)
- The task document will contain the complete plan for the new feature, including technical requirements, implementation plan, and AI agent instructions.

---

## 4. Development Mode Context

### Development Mode Context
<!-- This is where you tell the AI agent about your project's constraints and priorities -->
- **🚨 Project Stage:** TODO: Define if this is new development, production system, or legacy migration
- **Breaking Changes:** TODO: Specify if breaking changes are acceptable or must be avoided
- **Data Handling:** TODO: Define data preservation requirements
- **User Base:** TODO: Describe who will be affected by changes
- **Priority:** TODO: Set your speed vs stability priorities

---

## 5. Technical Requirements

### Functional Requirements
<!-- This is where the AI will understand exactly what the system should do - be specific about user actions and system behaviors -->

TODO: Define what users can do and what the system will automatically handle
- Example format: "User can [specific action]"
- Example format: "System automatically [specific behavior]" 
- Example format: "When [condition] occurs, then [system response]"

### Non-Functional Requirements
<!-- This is where you define performance, security, and usability standards -->
- **Performance:** TODO: Define response time and load handling requirements
- **Security:** TODO: Specify authentication and data protection needs
- **Usability:** TODO: Set user experience and accessibility standards
- **Responsive Design:** TODO: Define mobile, tablet, desktop support requirements
- **Theme Support:** TODO: Specify light/dark mode and brand requirements

### Technical Constraints
<!-- This is where you list limitations the AI agent must work within -->
- [Must use existing system X]
- [Cannot modify database table Y]
- [Must maintain compatibility with feature Z]

---

## 6. Data & Database Changes

### Database Schema Changes
<!-- This is where you specify any database modifications needed (if applicable) -->

TODO: Add your database schema changes here (new tables, columns, indexes, etc.)

### Data Model Updates
<!-- This is where you define data types, schema updates, or data structure changes -->

TODO: Define your data types, interfaces, and data structure changes

### Data Migration Plan
<!-- This is where you plan how to handle existing data during changes (if applicable) -->

TODO: Plan your data migration steps (backup, apply changes, transform data, validate)

---

## 7. API & Backend Changes

### Data Access Pattern Rules
<!-- This is where you tell the AI agent how to structure backend code in your project (if applicable) -->

TODO: Define where different types of code should go in your project (mutations, queries, API routes)

### Server Actions
<!-- List the backend mutation operations you need (if applicable) -->

TODO: List your create, update, delete operations and what they do

### Database Queries
<!-- Specify how you'll fetch data (if applicable) -->

TODO: Define your data fetching approach (direct queries vs separate functions)

---

## 8. Frontend Changes

### New Components
<!-- This is where you specify UI components to be created (if applicable) -->

TODO: List the new components you need to create and their purpose

### Page Updates
<!-- This is where you list pages that need modifications (if applicable) -->

TODO: List the pages that need changes and what modifications are required

### State Management
<!-- This is where you plan how data flows through your frontend (if applicable) -->

TODO: Define your state management approach and data flow strategy

---

## 9. Implementation Plan

TODO: Break your work into phases with specific tasks and file paths

---

## 10. Task Completion Tracking

### Real-Time Progress Tracking
<!-- This is where you tell the AI agent to update progress as work is completed -->

TODO: Define how you want the AI to track and report progress on tasks

---

## 11. File Structure & Organization

TODO: Plan what new files to create and existing files to modify

---

## 12. AI Agent Instructions

### Implementation Workflow
<!-- This is where you give specific instructions to your AI agent -->
🎯 **MANDATORY PROCESS:**
1.  **Virtual Environment:** Always activate the project's virtual environment before starting any work (e.g., `ai-env`, `source venv/bin/activate`, `conda activate`, etc.).
2.  **Branching:** Before starting implementation, ensure you are on the `main` branch and it is up to date. Create a new branch for the task with a descriptive name (e.g., `feat/T-123-add-user-auth`).
TODO:

### Communication Preferences
<!-- This is where you set expectations for how the AI should communicate -->
TODO: How do you want the agent to communicate with you

### Code Quality Standards
<!-- This is where you define your coding standards for the AI to follow -->
- **Code Style:** Follow the project's established coding conventions and style guidelines
- **Architecture Patterns:** Use established architectural patterns from the project's reference implementations
- **Error Handling:** Implement proper error handling and logging patterns
- **Testing:** Follow the project's testing conventions and ensure adequate test coverage
- **Documentation:** Maintain clear and up-to-date documentation for all new code

### Dependency Management Standards
<!-- This is where you define dependency management best practices -->
- **Version Constraints:** Use minimum version constraints (>=) instead of exact versions (==) to avoid conflicts
- **Conflict Resolution:** Check for dependency conflicts between packages before finalizing requirements
- **Compatibility:** Ensure all dependencies are compatible with each other and the project's requirements
- **Testing Dependencies:** Always test dependency installation in a clean environment

### Implementation Standards
<!-- This is where you define implementation best practices -->
- **Generic Implementations:** Always implement generic solutions unless explicitly told to use specific tools/services
- **No Assumptions:** Do not assume specific services unless explicitly mentioned
- **Flexible Design:** Design for flexibility and portability across different providers
- **Explicit Requirements:** Only use specific tools when explicitly requested by the user
- **Reference Implementation:** For any specialized tasks, reference and follow patterns from the project's reference implementations

---

## 13. Second-Order Impact Analysis

### Impact Assessment
<!-- This is where you think through broader consequences of your changes -->

TODO: Tell the AI what sections of code you're worried about breaking, performance concerns, and user workflow impacts

