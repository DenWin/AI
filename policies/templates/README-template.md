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

## Quality Checklist

**Content**
- [ ] All placeholders in brackets `[...]` have been replaced with actual content
- [ ] All rule statements use RFC-2119 keywords (**MUST**, **SHOULD**, etc.) in bold
- [ ] Each rule has clear rationale explaining the "why"
- [ ] Best practices are actionable and specific
- [ ] Common pitfalls help readers avoid mistakes
- [ ] Writing is concise and unambiguous; avoids vague terms
- [ ] Examples, if referenced, exist in `docs/`
- [ ] Every file in `docs/` is referenced or linked from the README

**Metadata**
- [ ] "Back to top" anchor `#top` exists at file start
- [ ] Top-level heading is `# <Category> Policies` with real category name
- [ ] Section `## Quick Description` exists with descriptive paragraph
- [ ] Section `## Policies` exists
- [ ] Subsection **Table of Contents** is present under Policies
- [ ] Horizontal rule (`---`) after TOC exists
- [ ] Each policy group starts with `### <Policy Category Name>`
- [ ] Each rule has a `#### <PREFIX>-NNN - <Rule Title>` heading with actual values
- [ ] Each rule section begins with `**Rule:**` line

**Structure**
- [ ] Use heading 3 (###) for policy category sections
- [ ] Use heading 4 (####) for individual rules
- [ ] Bold text for file references in TOC
- [ ] Always include "Back to top" links after each rule
- [ ] All TOC links point to correct anchors using (#prefix-001---rule-title) format
- [ ] Consistent anchor format throughout document

**Policy File Verification**
- [ ] All rules referenced in README exist in corresponding YAML files
- [ ] Policy file names match file references in TOC
- [ ] Rule identifiers match between README and YAML files
- [ ] All RFC-2119 keywords are consistently formatted in bold

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
