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
3. Replace all placeholders with actual content:
   - [Category] with the policy category (e.g., "Java Security", "Common Testing")
   - [PREFIX] with appropriate prefix (e.g., JAVA-SEC, BASE-TEST, PYTHON-STYLE)
   - [Descriptive Rule Title] with clear, concise rule titles
   - [Rule statement...] with specific, actionable rules using RFC-2119 keywords
4. Add more policies as needed following the same pattern
5. Ensure all rules are token-friendly, concise, and precise
6. Use **bold** formatting for RFC-2119 keywords (MUST, SHOULD, etc.)

### Step 3: Create README
1. Copy `README-template.md` to your policy directory
2. Replace all placeholders in brackets with actual content:
   - [Category] - Policy category (e.g., "Java Security", "Common Testing")
   - [PREFIX] - Rule prefix (e.g., JAVA-SEC, BASE-TEST)
   - [Rule Title] - Descriptive rule titles
   - [rule-title-lowercase] - Lowercase with hyphens for anchor links
   - [Policy File Name] - Name of the policy file
   - [Policy Category Name] - Section header for the category
3. Follow structure guidelines:
   - Use heading 3 (###) for policy category sections
   - Use heading 4 (####) for individual rules
   - Bold text for file references in TOC
   - Always include "Back to top" links after each rule
4. Ensure all links and anchors work correctly
5. Complete the quality checklist at the end

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

## Maintenance

- Review templates periodically for improvements
- Update based on feedback and usage patterns
- Ensure consistency with repository standards
- Keep examples current and relevant