# Evaluate Content — Human-Friendly Guide

**Version:** 1.0.0
**Last Updated:** 2025-09-22
**Maintainer:** [DenWin/AI](https://github.com/DenWin/AI)

> This document explains the purpose, usage, and structure of the `Evaluate Content — AI-Optimized Prompt`. It is intended for collaborators or maintainers who wish to understand or extend the evaluation process used with ChatGPT or other AI systems.

---

## 🎯 Purpose

This evaluation prompt is designed to audit text-based documents (e.g., instructions, YAML, Markdown specs, policy files, README files) for clarity, consistency, conciseness, correctness, and formatting discipline.

It is intended to:

* Help refine and maintain high-quality content before publication
* Detect subtle issues AI may struggle to follow (contradictions, ambiguity)
* Act as a review checklist for documentation and configuration artifacts

---

## 🛠️ Usage

### AI Invocation

Use this prompt directly (or via alias, e.g., `@evaluate-text`) inside ChatGPT to analyze a text block.

Paste your target text, then say:

```txt
Evaluate this using @evaluate-text.
```

Or:

```txt
Use the evaluate-text prompt to audit this document for correctness, redundancy, formatting, and clarity.
```

You can also link back to this documentation:

```md
For full prompt rationale, see:
https://github.com/DenWin/AI/blob/main/prompts/evaluate-content.md
```

---

## 📐 Evaluation Sections Explained

### 🔁 Redundancy

* Detect repetition across sections
* Flag duplicated or overlapping logic
* Identify contradiction or mirrored phrasing that can potentially be merged (but do not merge automatically)

### 🔤 Grammar & Orthography

* Spelling/grammar issues in English or German
* Consistent punctuation and capitalization

### 🧠 Clarity & Ambiguity

* Unclear phrases, passive constructions, and logic gaps
* Check if instructions or sentences could be interpreted multiple ways

### 📏 Consistency & Tone

* Indentation, bullet formatting, list punctuation
* Consistent tone (e.g., neutral, assertive, professional)
* Naming conventions and header capitalization

### 🌍 Cross-language Clarity

* Detect Denglisch or phrases that mix structure awkwardly
* Improve accessibility for readers not fluent in both languages

### 💬 Token Efficiency

* Eliminate bloat — reduce verbosity without losing meaning
* Favor clarity over word count when applicable

### 🧬 UTF Character Check

* Detect AI-specific or foreign-language punctuation (— “ ” ´ ‘ etc.)
* Flag characters with UTF-8 sizes > 1 byte

### 🔗 Link & Reference Validation

* Check if all referenced anchors, alias calls, or markdown links resolve correctly
* Identify broken or circular references

### 🧱 Structural Integrity

* Validate numbering, section hierarchy, and formatting consistency
* Confirm section headings match contents (especially in README, YAML, .md files)

---

## 📄 Output Format

The AI will return a markdown file with this structure:

### ✅ Executive Summary

* **Understood Purpose**: \[Brief description of the content’s intent and what it seems to cover]
* **Overall Quality Score**: X/10
* **Primary Issues**: \[Concise list of the most significant issues]
* **Strengths**: \[Key positive aspects]

### ✅ Passed Checks

* List of sections or checks that had no issues

### ⚠️ Partial or Problematic Checks

* Category → Quoted example → Issue → Suggested fix

### ❌ Critical Issues

* Contradictions, broken structure, or unreadable logic

> 📌 **Note:** The AI will not apply or merge changes unless explicitly asked to. It only flags what *can* be merged or changed.

---

## ✅ Best Practices for Use

* Provide **context**: Explain what the document is for and who it’s for.
* Specify **focus areas**: e.g., “Just check for grammar and tone.”
* Clarify **depth level**: e.g., “Quick overview” vs. “Deep dive.”
* Ask for **recommendations**, not rewrites.
* If needed, follow up with: “Now apply these changes.”

---

## 📜 Version History

| Version | Date       | Notes                                                          |
| ------- | ---------- | -------------------------------------------------------------- |
| 1.0.0   | 2025-09-22 | Initial version of human-facing guide, executive summary added |
