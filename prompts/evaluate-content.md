# Evaluate Text — AI-Optimized Prompt

## 🎯 Purpose

Evaluate structured or semi-structured content (Markdown, YAML, plaintext, etc.) with a focus on clarity, consistency, and execution-readiness.

---

## ✅ Evaluation Criteria

### 1. Executive Summary

Include this section in all output:

* **Content Understood As**: A short description of what the evaluator believes the content is about
* **Overall Quality Score**: X/10
* **Primary Issues**: \[Brief list of major problems]
* **Strengths**: \[Key positive aspects]

---

### 2. Redundancy

* Identify overlapping, duplicated, or contradictory sections or logic
* Highlight repeated rationale, phrasing, or structure

### 3. Grammar & Orthography

* Detect grammar and spelling issues (English or German)
* Flag inconsistent punctuation or capitalization

### 4. Clarity & Ambiguity

* Detect vague, ambiguous, or overly complex wording
* Flag unclear references, especially in multilingual or technical phrasing

### 5. Consistency & Tone

* Identify tone inconsistencies (formal/informal/conflicting intent)
* Check structure and formatting alignment (e.g., indentation, punctuation)
* Highlight contradictions between rules or logic blocks

### 6. Cross-language Clarity

* Flag hybrid phrases that combine English and German improperly
* Ensure clarity regardless of language context or phrasing mix

### 7. Token Efficiency

* Detect unnecessarily verbose or overly qualified language
* Highlight opportunities for cleaner, more efficient expression

### 8. UTF Character Analysis

* List unusual characters (e.g. —, “, ”, …) used in the content
* Highlight those likely from auto-formatting or copy-paste artifacts

---

## 📄 Output Format

Return a markdown report with these sections:

### ✅ Passed Checks

* Sections fully meeting expectations

### ⚠️ Partial or Problematic Checks

* Grouped by evaluation category (e.g. Redundancy, Clarity, etc.)
* For each issue: quote or describe the content, explain the problem, and suggest a concise fix

### ❌ Critical Issues

* Blocking issues (e.g., structural contradiction, severe formatting errors)

---

## 🛑 Action Scope

* Do **not** rewrite or correct the document
* Do **not** merge, modify, or restructure content unless explicitly instructed
* Focus on **issue identification only** — reporting, not fixing

---

## 🔁 Usage

Use this prompt to evaluate prompt templates, instructional text, YAML specs, or general technical writing.

This version is AI-executable and intended to be embedded in alias workflows (e.g., `@evaluate-text`).
