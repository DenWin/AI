# 📝 Evaluate

## 📌 Purpose

Ensure that any text, document, or external reference is checked for quality, completeness, and clarity.
This enables consistent and reliable results without requiring the user to manually re-check.

## 📐 Dimensions

### 1) Executive Summary

* **Understanding**: State in 2–4 sentences what the document is about. Identify type/genre and intent (e.g., SQL vs Java code, policy vs satire).
* **Overall quality score**: Assign a numeric score (0–100).
* **Primary issues**: List the main issues found.
* **Strengths**: List the main strengths.
* **Placement**: Render this block at the very top of the report, before all other sections.

### 2) Redundancy

* **Check redundancy**: Flag repeated words, phrases, sentences, or overlapping passages that do not add clarity or value.
* **Check structure**: Flag sections or stanzas/paragraphs that could be merged without loss of meaning.
* **Action**: Highlight redundant passages with `<!-- REDUNDANT: ... -->` and suggest removal or consolidation.

### 3) Grammar & Orthography

* **Check agreement**: Subject–verb and pronoun–antecedent.
* **Check tense**: Use consistent present tense for main text; past only in historical notes.
* **Check parallelism**: Ensure list items share the same grammatical form.
* **Check fragments & run-ons**: Correct comma splices and incomplete sentences.
* **Check prepositions & articles**: Apply standard usage.
* **Check spelling**: Use one dictionary variant (e.g., American or British).
* **Check capitalization**: Use Title Case for headings if required; capitalize proper nouns.
* **Check punctuation**: Apply consistent comma use; ensure spaces around punctuation.
* **Check numbers**: Follow numerals vs words policy (e.g., one–nine as words).
* **Check hyphenation**: Hyphenate compound adjectives per style.
* **Action**: Annotate or auto-correct if unambiguous.

### 4) Clarity & Ambiguity

* **Check ambiguity**: Remove vague terms ("some", "often", "generally") unless quantified.
* **Check sentence length**: Prefer ≤ 25 words; split long instructions.
* **Check pronoun references**: Replace unclear "it/this/that" with explicit subjects.
* **Check hedging & double negatives**: Replace with direct statements.
* **Check acronyms & jargon**: Define on first use; link to glossary.
* **Check order**: Put directives before rationale when possible.
* **Check examples**: Ensure each example ties explicitly back to the rule.
* **Action**: Insert `<!-- UNCLEAR: propose › ... -->` with a concrete rewrite.

### 5) Consistency & Tone

* **Check terminology**: Ensure terms and concepts are consistent across the document.
* **Check tone**: Ensure the overall style and register remain steady (e.g., formal vs informal, neutral vs persuasive).
* **Check formatting**: Ensure headings, lists, and other structural elements follow a uniform style.
* **Check logical flow**: Confirm statements do not contradict each other and maintain coherence.
* **Action**: Mark inconsistent usage or tone shifts with `<!-- INCONSISTENT: ... -->` and suggest a correction.

### 6) Cross-language Clarity

* **Check terminology mapping**: Flag if important terms appear in multiple languages and may require clarification.
* **Check false friends**: Note potential misunderstandings when similar words have different meanings across languages.
* **Check idioms**: Flag idiomatic expressions that may not translate directly.
* **Add informational notes**: When dates or times appear, add a note with the equivalent in German time (informational only).
* **Action**: Insert `<!-- CROSS-LANG: clarify ... -->` for unclear multilingual passages.

### 7) Token Efficiency

* **Check conciseness**: Flag unnecessary words or verbose passages.
* **Check focus**: Ensure the content stays on topic and does not drift.
* **Check density**: Ensure a high ratio of meaningful information to filler.
* **Check clarity vs brevity**: Flag if brevity harms understanding.
* **Action**: Highlight inefficient passages with `<!-- TOKEN-EFFICIENCY: ... -->` and suggest a concise form.

### 8) UTF Character Analysis

* **Check invisible characters**: Identify ZWSP, NBSP, BOM.
* **Check normalization**: Verify consistent Unicode normalization form (e.g., NFC).
* **Check homoglyphs**: Identify look-alike characters (O/0, l/1, –/—/-).
* **Check punctuation**: Ensure consistent use of quotes and dashes.
* **Check non-ASCII characters**: Identify any non-ASCII characters (e.g., invisible marks, homoglyphs, or AI-watermarks) and note whether harmless or risky.
* **Check AI watermark artifacts**: Flag AI watermark artifacts.
* **Action**: Report exact code points and positions; propose safe replacements.

## ⌨️ Input

* **Command**: `Evaluate`
* **Modes / Flags**:

  * `append <url>` → Fetch content from URL and add to evaluation target.
  * `diff` → Compare two versions and highlight changes with evaluation comments.
  * `summary` → Produce only a high-level evaluation report.
* **Target**:

  * Inline text or document, or
  * External content via URL.

## ⚙️ Behavior

1. Parse the `Evaluate` command.
2. Collect input (inline or via URL if `append`).
3. Apply all dimensions systematically.
4. Insert inline comments `<!-- REVIEW: ... -->` for detected issues.
5. Preserve formatting of unaffected parts.
6. Add a `## Evaluation Report` section with structured findings per dimension.
7. Confirm understanding with a short subject description.

## 📤 Output

* Annotated content highlighting issues.
* `## Evaluation Report` summarizing findings across all dimensions.
* Confirmation of understanding with a short subject description.
* Optional summary mode with condensed notes only.

## 🛑 Action Scope

* Do not rewrite or correct the document.
* Do not merge, modify, or restructure content unless explicitly instructed.
* Focus on issue identification only — reporting, not fixing.
* Do not use memory, prior chat context, or external assumptions during evaluation.
* Only reference the given input text. The sole exception is in the **Executive Summary**, where an interpretation of the document’s content is required.

## 🔁 Usage

* Use this prompt to evaluate prompt templates, instructional text, YAML specs, or general technical writing.
* This version is AI-executable and intended to be embedded in alias workflows (e.g., @evaluate-text).
