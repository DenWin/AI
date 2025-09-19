# AI

A collection of structured prompts and policy definitions designed for use within AI agents. This repository provides reusable instructions, guidelines, and templates to ensure consistent behavior, reasoning, and compliance across different tasks and environments.

## Repository Structure

```
├── README.md              # Project documentation
├── aliases.yml            # Global aliases configuration
├── .gitignore            # Git ignore rules for md/yml files
├── prompts/              # Prompt templates and definitions
│   ├── aliases.yml       # Prompt-specific aliases
│   ├── analyze.md        # Analysis prompts
│   └── template.md       # Reusable prompt template
└── policies/             # Policy definitions and guidelines
    ├── common/           # Common policies across all environments
    │   └── base.yml      # Base policy configuration
    └── languages/        # Language-specific policies
        └── java/         # Java development policies
            └── java-style.yml
```

## Getting Started

1. **Prompts**: Use the templates in `prompts/` to create structured, reusable AI prompts
2. **Policies**: Reference policy files in `policies/` for consistent behavior guidelines
3. **Templates**: Start with `prompts/template.md` as a foundation for new prompts

## Usage

This repository is designed to be:
- **Modular**: Each component can be used independently
- **Reusable**: Templates and policies can be referenced across different AI systems
- **Structured**: Consistent organization for easy navigation and maintenance
- **Extensible**: Easy to add new prompts, policies, and configurations

## Contributing

When adding new content:
- Follow the established directory structure
- Use clear, descriptive filenames
- Include appropriate documentation
- Test prompts before committing
