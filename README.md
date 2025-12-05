# GitHub Copilot Prompt Templates

A comprehensive collection of prompt templates and configurations for GitHub Copilot to enhance your development workflow.

## 📋 Overview

This repository provides:
- **VS Code Chat Configuration** (`.vscode/chat.json`) - Custom chat participants for specialized tasks
- **Workspace Instructions** (`.github/copilot-instructions.md`) - Project-level Copilot guidelines
- **Prompt Templates** (`prompts/examples/`) - Ready-to-use prompts for common development tasks

## 🚀 Quick Start

### 1. Clone or Download This Repository

```bash
git clone https://github.com/kennycyb/copilot-prompt.git
cd copilot-prompt
```

### 2. Copy Files to Your Project

Copy the relevant files to your project:

```bash
# Copy VS Code chat configuration
cp -r .vscode /path/to/your/project/

# Copy GitHub Copilot instructions
cp -r .github /path/to/your/project/

# (Optional) Copy prompt examples for reference
cp -r prompts /path/to/your/project/
```

### 3. Customize for Your Project

Edit the files to match your project's needs:
- **`.github/copilot-instructions.md`** - Update with your project's coding standards, conventions, and practices
- **`.vscode/chat.json`** - Adjust chat participants or add new ones specific to your project

## 📁 Repository Structure

```
copilot-prompt/
├── .github/
│   └── copilot-instructions.md    # Workspace-level Copilot instructions
├── .vscode/
│   └── chat.json                  # VS Code chat participant configuration
├── prompts/
│   └── examples/                  # Example prompt templates
│       ├── code-review.md         # Code review prompts
│       ├── documentation.md       # Documentation generation prompts
│       ├── testing.md             # Test writing prompts
│       ├── debugging.md           # Debugging assistance prompts
│       ├── refactoring.md         # Code refactoring prompts
│       └── architecture.md        # Architecture and design prompts
└── README.md
```

## 🎯 Available Chat Participants

The `.vscode/chat.json` configuration includes the following specialized chat participants:

### Code Reviewer
Expert in code quality, security, and best practices. Use for thorough code reviews.

### Documentation Expert
Specialized in creating clear, comprehensive documentation, API docs, and README files.

### Test Writer
Focused on writing comprehensive tests including unit, integration, and e2e tests.

### Debugger
Expert at identifying root causes of bugs and providing debugging strategies.

### Solution Architect
Specialized in system design, architecture patterns, and scalability.

## 📝 Prompt Templates

Browse the `prompts/examples/` directory for ready-to-use templates:

- **[Code Review](prompts/examples/code-review.md)** - Review code for quality, security, and best practices
- **[Documentation](prompts/examples/documentation.md)** - Generate documentation for code, APIs, and projects
- **[Testing](prompts/examples/testing.md)** - Create comprehensive test suites
- **[Debugging](prompts/examples/debugging.md)** - Get help troubleshooting issues
- **[Refactoring](prompts/examples/refactoring.md)** - Improve code quality and structure
- **[Architecture](prompts/examples/architecture.md)** - Design systems and make architectural decisions

## 💡 Usage Tips

### Using Workspace Instructions

Once `.github/copilot-instructions.md` is in your project, GitHub Copilot will automatically use these instructions when providing suggestions and chat responses. Update this file with:

- Your project's coding standards
- Preferred libraries and frameworks
- Security requirements
- Testing conventions
- Documentation standards

### Using Chat Participants

In VS Code with Copilot Chat, you can reference chat participants using `@participant-id`. For example:

```
@code-review Please review this authentication function
@documentation Generate API docs for this endpoint
@test-writer Create unit tests for this validation function
```

### Using Prompt Templates

The prompt templates in `prompts/examples/` are starting points. Customize them by:

1. Replacing `[PLACEHOLDERS]` with your specific content
2. Adding or removing sections based on your needs
3. Adapting the language to match your project's context

## 🔧 Customization Guide

### Adding Custom Chat Participants

Edit `.vscode/chat.json` to add your own participants:

```json
{
  "id": "your-participant-id",
  "name": "Your Participant Name",
  "description": "Brief description",
  "systemPrompt": "Detailed instructions for the AI..."
}
```

### Creating Custom Prompt Templates

Add new templates to `prompts/examples/` following this structure:

```markdown
# [Template Name] Prompt Template

Use this template when [describe use case].

## Prompt

[Provide the prompt template with placeholders]

## Example Usage

[Show concrete examples]

## Tips

[Provide helpful tips for using the template]
```

## 🤝 Contributing

This is a template repository. Feel free to:

1. Fork this repository
2. Customize for your needs
3. Share your improvements via pull requests

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Resources

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [VS Code Copilot Chat](https://code.visualstudio.com/docs/copilot/copilot-chat)
- [Copilot Instructions Documentation](https://docs.github.com/en/copilot/customizing-copilot/adding-custom-instructions-for-github-copilot)

## ⭐ Support

If you find this template helpful, please consider giving it a star on GitHub!