# AI Assistant Instructions

## Project Overview
This file contains instructions for AI assistants to follow when helping with this project. Include this file in all projects to maintain consistency in code style, development approaches, and project-specific conventions.

## General Guidelines

### Code Style and Conventions
- Follow the language-specific style guides for each file type
- Use consistent indentation (spaces or tabs as per project configuration)
- Write clear, descriptive variable and function names
- Include appropriate comments for complex logic
- Organize code in a modular and maintainable way

### Documentation
- Document all public APIs, classes, and functions
- Keep documentation up-to-date with code changes
- Use markdown for documentation files
- Include examples where appropriate

### Version Control
- Write clear, descriptive commit messages
- Follow the project's branching strategy
- Reference issue numbers in commits and pull requests where applicable

## Development Workflow

### Feature Development
1. Understand requirements thoroughly before implementation
2. Break down complex tasks into smaller, manageable steps
3. Consider edge cases and error handling
4. Add appropriate tests for new features

### Bug Fixing
1. Reproduce the issue first
2. Identify the root cause
3. Fix the issue at its source, not just the symptoms
4. Add regression tests to prevent recurrence

### Code Review Criteria
- Functionality: Does the code work as expected?
- Security: Are there potential security issues?
- Performance: Is the code efficient?
- Maintainability: Is the code easy to understand and modify?
- Error handling: Are errors handled appropriately?

## Project-Specific Instructions

### Directory Structure
Maintain the following directory structure for consistency:
```
project_root/
  ├── src/               # Source code
  ├── tests/             # Test files
  ├── docs/              # Documentation
  ├── scripts/           # Utility scripts
  ├── config/            # Configuration files
  ├── copilot_instructions.md # This file
  └── README.md          # Project documentation
```

### Preferred Technologies
- Add project-specific preferred technologies, libraries, and frameworks here

### Avoid
- Add technologies, patterns, or approaches to avoid in this project

## How to Use This File

1. Include this file in the root directory of each project
2. Update project-specific sections for each project
3. Reference this file when requesting assistance from AI tools
4. Update as project requirements evolve

## Project-Specific Notes

Add any project-specific notes, special requirements, or conventions below:

- [Project-specific note 1]
- [Project-specific note 2]

## AI Assistant Configuration

### When To Ask For Clarification
- If requirements are ambiguous or contradictory
- If making architectural decisions with long-term implications
- If suggesting significant refactoring of existing code
- If implementing security-critical features

### Default Assumptions
- Prefer readability over cleverness
- Prioritize maintainability and future extensibility
- Use simple solutions until complexity is justified
- Follow the principle of least surprise

### Response Format Preferences
- Explain your reasoning before providing code solutions
- Include relevant code snippets with clear explanations
- Provide step-by-step instructions for complex tasks
- Suggest tests or validation approaches when implementing features

### Common Commands and Procedures
- Document common build commands, testing procedures, and dev environment setup
- Include any custom scripts or utilities specific to the project
- Document required environment variables and configuration settings

## Accessibility Guidelines
- Ensure UI components are accessible to users with disabilities
- Follow WCAG standards for web projects
- Use semantic HTML for web projects
- Include alternative text for images

## Performance Considerations
- Optimize resource-intensive operations
- Minimize network requests
- Use appropriate caching strategies
- Consider pagination for large data sets

## MCP Server Management and Autonomous Operations
- Start all MCP (Model Context Protocol) servers for every project automatically
- Intelligently and autonomously use all available tools with or without explicit direction
- Install new MCP servers as needed based on project requirements
- Create new MCP servers when required, autonomously determining appropriate configurations
- Proactively suggest optimizations and improvements to existing MCP server configurations
- Monitor and report on MCP server health and performance
- Handle error recovery and server restarts autonomously
- Implement appropriate security measures for MCP servers
- Ensure seamless integration between different MCP servers and project components

## AI Autonomy Guidelines
- Take initiative to solve problems without explicit direction when confident in the approach
- Intelligently determine when to ask for confirmation versus when to proceed autonomously
- Use available context and tools to gather necessary information before taking action
- Document all autonomous actions taken for user transparency
- Learn from project patterns to improve future autonomous decisions
- Balance autonomy with adherence to project-specific guidelines and preferences
- Proactively identify potential issues and suggest preventative measures
- Adapt approach based on feedback and evolving project requirements

---

Last updated: May 12, 2025
