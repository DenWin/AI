<a id="top"></a>
# [Category] Policies

**Last updated**: YYYY-MM-DD

## Quick Description

These policies provide [brief description of what the policies cover]. The policies are designed to be concise and precise for AI consumption, while this README will provide the rationale behind each policy. If further details are required additional examples can be found in the [docs folder](./docs/).

## Policies

**Table of Contents**
- **[Policy File Name]** ([policy-file.yml](./policy-file.yml))
  - [[PREFIX]-001 - [Rule Title]](#[prefix]-001---[rule-title-lowercase])
  - [[PREFIX]-002 - [Rule Title]](#[prefix]-002---[rule-title-lowercase])
  - [[PREFIX]-003 - [Rule Title]](#[prefix]-003---[rule-title-lowercase])

---

### [Policy Category Name]

#### [PREFIX]-001 - [Rule Title]

**Rule:**
- [Copy the rule statement from the YAML file]

**Rationale:**
- [Explain why this rule exists]
- [Describe the benefits of following this rule]
- [Mention potential problems it prevents]
- [Add context about best practices]

**Best Practices:** (optional)
- [List specific recommendations]
- [Include actionable guidance]
- [Provide implementation tips]
- [Add relevant considerations]

**Common Pitfalls:** (optional)
- [List things to avoid]
- [Mention common mistakes]
- [Include anti-patterns]

**Quick Examples:** (optional)
- [Small examples]
- [bigger once belong into the docs folder].

[↑ Back to top](#top)

---

#### [PREFIX]-002 - [Rule Title]

**Rule:**
- [Copy the rule statement from the YAML file]

**Rationale:**
- [Explain why this rule exists]
- [Describe the benefits of following this rule]
- [Mention potential problems it prevents]

**Best Practices:**
- [List specific recommendations]
- [Include actionable guidance]

[↑ Back to top](#top)

---

#### [PREFIX]-003 - [Rule Title]

**Rule:**
- [Copy the rule statement from the YAML file]

**Rationale:**
- [Explain why this rule exists]
- [Describe the benefits of following this rule]

**Best Practices:** (optional)
- [List specific recommendations]

[↑ Back to top](#top)

---

<!-- Template Instructions:

1. Replace all placeholders in brackets with actual content:
   - [Category] - Policy category (e.g., "Java Security", "Common Testing")
   - [PREFIX] - Rule prefix (e.g., JAVA-SEC, BASE-TEST)
   - [Rule Title] - Descriptive rule titles
   - [rule-title-lowercase] - Lowercase with hyphens for anchor links
   - [Policy File Name] - Name of the policy file
   - [Policy Category Name] - Section header for the category

2. Structure Guidelines:
   - Use heading 3 (###) for policy category sections
   - Use heading 4 (####) for individual rules
   - Bold text for file references in TOC
   - Always include "Back to top" links after each rule

3. Content Guidelines:
   - Keep descriptions concise but informative
   - Focus on practical guidance in best practices
   - Include rationale that explains the "why"
   - List common pitfalls to help avoid mistakes
   - Make content language-agnostic for common policies

4. Navigation:
   - Ensure all TOC links point to correct anchors
   - Use consistent anchor format (#prefix-001---rule-title)
   - Include HTML anchor at top for "Back to top" links

-->

## Validation Checklist
Evaluate with each adjustment

**Basics**
- [ ] Title present and matches folder category.
- [ ] “Quick Description” filled with real text (no placeholders like “[...]”).
- [ ] `docs/` folder exists and link `./docs/` resolves.
- [ ] Referenced policy file exists (e.g., `./policy-file.yml`).

**Table of Contents**
- [ ] TOC lists every rule in the policy file.
- [ ] TOC links use correct anchors: `#[prefix]-NNN---kebab-case-rule-title`.
- [ ] No dead TOC links.

**Per-Rule Sections**
_For each rule in YAML:_
- [ ] Section header `#### [PREFIX]-NNN - [Rule Title]` exists.
- [ ] **Rule** block present and matches YAML `rule` exactly.
- [ ] **Rationale** block has at least one bullet with non-placeholder text.
- [ ] “[↑ Back to top](#top)” present after section.

**YAML ↔ README sync**
- [ ] Every YAML rule appears once in README.
- [ ] No README rule absent from YAML.
- [ ] Prefix format `[PREFIX]-NNN` consistent and sequential where intended.
- [ ] Rule statements use RFC-2119 keywords in **bold**.

**Links and anchors**
- [ ] All relative links resolve (`./policy-file.yml`, `./docs/...`).
- [ ] All internal anchors render and navigate correctly.

**Quality gates**
- [ ] No placeholder tokens remain: `[Category]`, `[Rule Title]`, `[PREFIX]`, `[...]`.
- [ ] No empty lists or empty headings.
- [ ] Writing is concise and unambiguous; avoids vague terms.
- [ ] Examples, if referenced, exist in `docs/`.
- [ ] Every file in `docs/` is referenced or linked from the README.

**Metadata**
- [ ] “Back to top” anchor `#top` exists at file start.
- [ ] Top-level heading is `# <Category> Policies` with real category name.
- [ ] Next line contains `**Last updated**: YYYY-MM-DD` and has a current date.
- [ ] Section `## Quick Description` exists with descriptive paragraph.
- [ ] Section `## Policies` exists.
- [ ] Subsection **Table of Contents** is present under Policies.
- [ ] Horizontal rule (`---`) after TOC exists.
- [ ] Each policy group starts with `### <Policy Category Name>`.
- [ ] Each rule has a `#### <PREFIX>-NNN - <Rule Title>` heading with actual values.
- [ ] Each rule section begins with `**Rule:**` line.
