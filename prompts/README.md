# AI Prompts

This directory contains reusable AI prompts for various tasks related to code analysis, documentation evaluation, and policy compliance checking.

## How Prompts Work

The prompts in this directory are designed to be self-explanatory and work with various AI systems. Each prompt provides:

1. **Clear Instructions**: Step-by-step guidance for the AI system
2. **Input Specifications**: What type of content to analyze
3. **Output Format**: How results should be structured
4. **Usage Examples**: Practical applications and scenarios

## Available Prompts

### 🔍 Policy Compliance Analysis
**File:** [apply-policy.md](./apply-policy.md)  
**Aliases:** `/apply-policy`, `/use-policy`  
**Purpose:** Comprehensive policy compliance analysis for code

The prompt automatically:
- Loads language-specific and common policies using index files
- Performs policy-by-policy evaluation with detailed reporting
- Identifies line-specific violations
- Provides Git-style conflict markers for suggested fixes
- Generates compliance scoring and priority recommendations

### 📝 Content Quality Analysis
**File:** [evaluate-content.md](./evaluate-content.md)  
**Aliases:** `/evaluate-text`, `/evaluate-doc`  
**Purpose:** Unified analysis for text and document quality

The prompt analyzes:
- Redundancy and unnecessary repetition
- Content and structural consistency
- Completeness and missing elements
- Clarity and comprehension issues
- Professional standards compliance

### 📋 Prompt Template
**File:** [template.md](./template.md)  
**Purpose:** Template for creating new structured AI prompts

## Alias System

Prompts are accessible through aliases defined in [aliases.yml](../aliases.yml):
```yaml
aliases:
  apply-policy: prompts/apply-policy.md
  use-policy: prompts/apply-policy.md  # Alternative name
  evaluate-text: prompts/evaluate-content.md
  evaluate-doc: prompts/evaluate-content.md
```

## AI System Integration

These prompts work with:
- ChatGPT and GPT-based systems
- Claude and Anthropic AI systems  
- Custom AI implementations
- AI development environments

## Quality Gate

> Evaluate with each adjustment

**Content Verification**
- [x] All prompts have clear purpose and usage instructions
- [x] Examples are provided for complex prompts
- [x] Output formats are clearly defined
- [x] Error handling scenarios are covered
- [x] Prompts are tested with target AI systems

**Structure Verification**
- [x] Consistent formatting across all prompts
- [x] Clear section headers and organization
- [x] Proper markdown formatting
- [x] Logical flow from instruction to output
- [x] Complete usage documentation

**Integration Verification**
- [x] All prompts are referenced in aliases.yml
- [x] File paths in aliases are correct
- [x] Prompts work with intended AI systems
- [x] Cross-references to policies/templates are accurate
- [x] Examples match repository structure

**Alias-File Consistency**
- [x] All aliases point to existing files
- [x] All prompt files are present in aliases (README exempt)
- [x] Multiple aliases can point to same file (evaluate-text/doc → evaluate-content.md)
- [x] No orphaned prompt files without aliases
- [x] Alias names match intended functionality
- [x] File paths in aliases.yml are correct