# AI Prompts

This directory contains reusable AI prompts for various tasks related to code analysis, documentation evaluation, and policy compliance checking.

## Available Prompts

### 🔍 Policy Analysis
**File:** [use-policies.md](./use-policies.md)  
**Alias:** `/use-policy for [Language]`  
**Purpose:** Comprehensive policy compliance analysis for code

**Features:**
- Loads language-specific and common policies automatically
- Policy-by-policy evaluation with detailed reporting
- Line-specific violation identification
- Git-style conflict markers for suggested fixes
- Compliance scoring and priority recommendations

**Usage Examples:**
- `/use-policy for Java` - Analyze Java code against all Java policies
- `/use-policy for Python` - Analyze Python code (when policies exist)

### 📝 Text Analysis
**File:** [evaluate-text.md](./evaluate-text.md)  
**Alias:** `/evaluate-text`  
**Purpose:** Comprehensive text analysis for quality and clarity

**Analysis Dimensions:**
- Redundancy detection
- Consistency checking (content and structure)
- Completeness assessment
- Clarity evaluation
- Actionable improvement suggestions

**Usage Modes:**
- `/evaluate-text` - Full comprehensive analysis
- `/evaluate-text --focus=clarity` - Clarity-focused analysis
- `/evaluate-text --focus=structure` - Structure-focused analysis

### 📄 Document Analysis  
**File:** [evaluate-doc.md](./evaluate-doc.md)  
**Alias:** `/evaluate-doc`  
**Purpose:** Specialized analysis for structured documents and formal documentation

**Enhanced Features:**
- Document structure and organization analysis
- Navigation and cross-reference validation
- Professional standards compliance checking
- Documentation-specific quality metrics
- Implementation roadmap with prioritized improvements

**Specialized Modes:**
- `/evaluate-doc --policy` - Policy document standards
- `/evaluate-doc --technical` - Technical documentation review
- `/evaluate-doc --api` - API documentation analysis
- `/evaluate-doc --user` - User guide evaluation

### 📋 Template Prompt
**File:** [template.md](./template.md)  
**Purpose:** Comprehensive template for creating structured, reusable AI prompts

## Usage Guidelines

### 1. Accessing Prompts
Reference prompts using the alias system defined in [aliases.yml](../aliases.yml):
```yaml
aliases:
  use-policies: prompts/use-policies.md
  evaluate-text: prompts/evaluate-text.md
  evaluate-doc: prompts/evaluate-doc.md
```

### 2. Integration with AI Systems
These prompts are designed to work with:
- ChatGPT and GPT-based systems
- Claude and Anthropic AI systems  
- Custom AI implementations
- AI development environments

### 3. Customization
Each prompt can be customized for specific:
- Organizational standards
- Industry requirements
- Language-specific needs
- Project-specific criteria

## Quality Checklist

**Content Verification**
- [ ] All prompts have clear purpose and usage instructions
- [ ] Examples are provided for complex prompts
- [ ] Output formats are clearly defined
- [ ] Error handling scenarios are covered
- [ ] Prompts are tested with target AI systems

**Structure Verification**
- [ ] Consistent formatting across all prompts
- [ ] Clear section headers and organization
- [ ] Proper markdown formatting
- [ ] Logical flow from instruction to output
- [ ] Complete usage documentation

**Integration Verification**
- [ ] All prompts are referenced in aliases.yml
- [ ] File paths in aliases are correct
- [ ] Prompts work with intended AI systems
- [ ] Cross-references to policies/templates are accurate
- [ ] Examples match repository structure

**Maintenance Verification**
- [ ] Prompts are updated when policies change
- [ ] References to repository structure are current
- [ ] Examples use current file naming conventions
- [ ] Documentation reflects current capabilities
- [ ] Version compatibility is maintained

## Prompt Development Guidelines

### Creating New Prompts
1. **Define Clear Purpose**: Specify exact use case and expected outcomes
2. **Structure Instructions**: Use clear sections and step-by-step guidance
3. **Provide Examples**: Include input/output examples for complex prompts
4. **Test Thoroughly**: Verify with multiple AI systems and scenarios
5. **Document Usage**: Include clear usage instructions and limitations

### Best Practices
- Use clear, unambiguous language
- Provide specific output format requirements
- Include error handling instructions
- Consider edge cases and variations
- Make prompts modular and reusable

### Maintenance
- Review prompts when policies change
- Update examples to reflect current repository structure
- Test prompts periodically with AI systems
- Gather feedback and iterate improvements
- Keep documentation current and accurate