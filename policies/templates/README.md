# Policy Templates

This directory contains templates for creating new policies, documentation, and examples. Use these templates to maintain consistency across the repository.

## Available Templates

### 1. Policy File Template
**File:** [policy-template.yml](./policy-template.yml)  
**Purpose:** Template for creating new policy YAML files  
**Usage:** Copy and customize for new policy categories

**Features:**
- RFC-2119 compliant structure
- Consistent formatting
- Clear placeholder guidance
- Token-friendly design for AI consumption

### 2. README Template  
**File:** [README-template.md](./README-template.md)  
**Purpose:** Template for policy README files  
**Usage:** Copy and customize for each policy directory

**Features:**
- Consistent heading hierarchy
- Table of contents structure
- Rule/Rationale/Examples format
- Navigation with "Back to top" links
- Comprehensive placeholder guidance

### 3. Documentation Example Template
**File:** [docs/example-template.md](./docs/example-template.md)  
**Purpose:** Template for detailed policy examples  
**Usage:** Copy and customize when detailed examples are needed

**Features:**
- Good/bad example sections
- Implementation guidelines
- Language-specific considerations
- Step-by-step guidance

## Creating New Policies

### Step 1: Create Policy Directory
```bash
mkdir -p policies/[category]/[subcategory]/docs
```

### Step 2: Copy and Customize Policy File
1. Copy `policy-template.yml` to your new directory
2. Rename to descriptive name (e.g., `security.yml`, `java-style.yml`)
3. Replace all placeholders with actual content
4. Follow RFC-2119 keywords (MUST, SHOULD, etc.)

### Step 3: Create README
1. Copy `README-template.md` to your policy directory
2. Replace all placeholders with actual content
3. Ensure all links and anchors work correctly
4. Follow the established heading hierarchy

### Step 4: Add Examples (If Needed)
1. Copy `docs/example-template.md` for complex rules
2. Create one file per rule that needs detailed examples
3. Use naming convention: `[PREFIX]-[NUMBER]-[title].md`
4. Only create when README guidance isn't sufficient

## Template Guidelines

### Policy File Guidelines
- Use clear, descriptive rule titles
- Make rules specific and actionable
- Include appropriate RFC-2119 keywords
- Keep rules token-friendly for AI consumption
- Number rules sequentially within categories

### README Guidelines
- Start with HTML anchor for navigation
- Use consistent heading hierarchy (### for sections, #### for rules)
- Include comprehensive rationale for each rule
- Add best practices and common pitfalls
- Provide "Back to top" navigation
- Keep content language-agnostic for common policies

### Documentation Guidelines
- Only create detailed examples when necessary
- Include both good and bad examples
- Explain the reasoning behind examples
- Consider multiple scenarios and edge cases
- Separate language-specific guidance
- Update examples when policies change

## Naming Conventions

### Policy Files
- Use descriptive names: `security.yml`, `testing.yml`, `java-style.yml`
- Avoid generic names like `rules.yml` or `policies.yml`
- Use lowercase with hyphens for multi-word names

### README Files
- Always name as `README.md` in policy directories
- Follow standard markdown conventions
- Use consistent formatting throughout

### Example Files
- Format: `[PREFIX]-[NUMBER]-[descriptive-title].md`
- Examples: `JAVA-SEC-001-input-validation.md`, `BASE-TEST-001-coverage.md`
- Use lowercase with hyphens for titles
- Match the rule identifiers from policy files

## Quality Checklist

### Before Creating New Policies
- [ ] Check if similar policies already exist
- [ ] Ensure rules are specific and actionable
- [ ] Verify RFC-2119 compliance
- [ ] Review for token-friendliness
- [ ] Test all links and navigation

### Before Publishing
- [ ] All placeholders replaced with actual content
- [ ] Navigation links work correctly
- [ ] Content follows established patterns
- [ ] Examples are relevant and helpful
- [ ] Documentation is clear and comprehensive

## Maintenance

- Review templates periodically for improvements
- Update based on feedback and usage patterns
- Ensure consistency with repository standards
- Keep examples current and relevant