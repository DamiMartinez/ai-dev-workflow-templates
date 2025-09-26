# Git Commit Workflow

This document outlines the standard procedure for committing code changes to a repository. All contributors, including AI agents, must follow these guidelines to maintain a clean, readable, and consistent commit history.

## Core Principles

- **Atomic Commits:** Each commit should represent a single logical change. Avoid bundling unrelated changes into one commit.
- **Clarity:** Commit messages should be clear, concise, and descriptive. They serve as the primary documentation for the project's history.
- **Consistency:** Following a consistent format for commit messages makes the history easier to read and allows for automated tools to parse it.

## The Commit Process

Follow these steps every time you commit changes:

1.  **Verify Branch:**
    *   Ensure you are on the correct branch for the changes you are committing.
    *   **Command:** `git branch --show-current`

2.  **Review Changes:**
    *   Before staging, check the modifications you have made.
    *   **Command:** `git status`
    *   **Command:** `git diff` (to see unstaged changes)
    *   **Command:** `git diff --staged` (to see staged changes)

2.  **Stage Files:**
    *   Add only the files that belong to a single logical change to the staging area.
    *   **Command:** `git add <file_path_1> <file_path_2>`
    *   For new files: `git add <new_file_path>`

3.  **Construct the Commit Message:**
    *   The commit message **must** follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.
    *   The format is: `type(scope): subject`
    *   **`type`**: Must be one of the following:
        *   **feat**: A new feature.
        *   **fix**: A bug fix.
        *   **docs**: Documentation only changes.
        *   **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
        *   **refactor**: A code change that neither fixes a bug nor adds a feature.
        *   **perf**: A code change that improves performance.
        *   **test**: Adding missing tests or correcting existing tests.
        *   **build**: Changes that affect the build system or external dependencies (e.g., `pyproject.toml`, `package.json`).
        *   **ci**: Changes to CI configuration files and scripts.
        *   **chore**: Other changes that don't modify `src` or `test` files.
    *   **`scope`** (optional): A noun specifying the section of the codebase affected (e.g., `api`, `ui`, `database`).
    *   **`subject`**: A concise description of the change.
        *   Use the imperative, present tense: "add" not "added" nor "adds".
        *   Don't capitalize the first letter.
        *   No dot (.) at the end.
    *   **`body`** (optional): A longer description providing context and the "why" behind the change. Use it to explain what and why vs. how.
    *   **`footer`** (optional):
        *   Use for `BREAKING CHANGE:` followed by a description of the change. A breaking change **must** have a `!` after the type/scope (e.g., `feat(api)!: ...`).
        *   Use to reference issue numbers (e.g., `Closes #123`).

4.  **Propose the Commit:**
    *   As an AI agent, you must present the full commit message to the user for approval before executing the commit.

5.  **Await User Approval:**
    *   Do not proceed with the `git commit` command until the user explicitly approves it.

6.  **Execute the Commit:**
    *   Once approved, run the commit command.
    *   **Command:** `git commit -m "<subject>" -m "<body>"`

7.  **Verify:**
    *   After committing, run `git log -1` to ensure the commit was created correctly.

## Commit Message Examples

### Feature
```
feat(agent): add tool for reading CSV files

The new CsvReaderTool allows the agent to ingest and process data from CSV files, enabling it to answer questions based on structured data.
```

### Fix with Scope
```
fix(api): correct pagination logic for user endpoint

The pagination for the `/users` endpoint was not calculating the offset correctly, causing it to skip records on subsequent pages. This commit fixes the offset calculation.

Closes #42
```

### Breaking Change
```
refactor(auth)!: replace JWT with session-based authentication

BREAKING CHANGE: The authentication mechanism has been changed from stateless JWT tokens to stateful server-side sessions. All API clients must be updated to handle cookies for session management instead of sending an `Authorization` header.
```

### Documentation
```
docs: update README with new setup instructions
```

### Deliverables
- A Git commit with a message that adheres to the Conventional Commits specification.
- The commit should represent a single, logical change.
