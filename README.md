# AI Development Workflow Templates

A community-driven repository of AI agent templates, playbooks, and task definitions for coding workflows. This project provides a collection of standardized, reusable templates that enable AI agents to assist developers more effectively.

## Vision

- **Standardize AI-assisted workflows** across different development scenarios
- **Improve AI agent effectiveness** through clear, structured instructions
- **Reduce setup time** for common development tasks
- **Promote best practices** in AI-assisted development
- **Build a community** of contributors sharing knowledge and workflows

## Available Templates

| File | Description |
| --- | --- |
| [templates/001_task_planning.md](templates/001_task_planning.md) | A systematic framework for planning and executing technical projects with AI assistance. |
| [templates/002_bug_fix.md](templates/002_bug_fix.md) | A structured approach to identifying, analyzing, and resolving bugs. |
| [templates/003_code_review.md](templates/003_code_review.md) | A comprehensive template for conducting thorough code reviews. |
| [templates/004_git_commit_workflow.md](templates/004_git_commit_workflow.md) | A workflow for creating clear, consistent, and conventional git commits. |

## Available Skills

Skills are reusable agent capabilities that can be invoked by name to perform specialized tasks. They leverage browser automation and developer tooling via MCP servers.

| Skill | Description |
| --- | --- |
| [skills/scraping-website/](skills/scraping-website/SKILL.md) | Discovers hidden JSON APIs on websites by monitoring network traffic, enabling reliable data extraction without HTML parsing. |
| [skills/chrome-inspect/](skills/chrome-inspect/SKILL.md) | Inspects live browser tabs using Chrome DevTools — reads cookies, localStorage, JWT tokens, DOM elements, network requests, and console logs. |

## How to Use

These templates are designed to be used by AI coding assistants following a standardized workflow:

1. **Explain your request** to your coding assistant (e.g., "I need to fix a bug in my authentication system" or "I want to add a new feature for user profiles").

2. **The AI assistant automatically:**
   - Reviews the `AGENTS.md` file to understand the workflow
   - Identifies the appropriate template or skill based on your request:
     - Bug fixes → `templates/002_bug_fix.md`
     - New features/development → `templates/001_task_planning.md`
     - Code reviews → `templates/003_code_review.md`
     - Git commits → `templates/004_git_commit_workflow.md`
     - Scraping a website → `skills/scraping-website/`
     - Inspecting a browser tab → `skills/chrome-inspect/`
   - Follows the template's instructions to complete your task

## Contributing

We welcome contributions! If you have a workflow that could be standardized into a template, please consider contributing. Our goal is to build a comprehensive library of templates for all aspects of software development.

Please read our [Contributing Guidelines](CONTRIBUTORS.md) to get started.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.