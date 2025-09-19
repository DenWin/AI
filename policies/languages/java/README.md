<a id="top"></a>
# Java Development Policies

## Quick Description

These policies provide AI-friendly guidelines for Java development, covering coding style, security, testing, and performance. The policies are designed to be concise and precise for AI consumption, while this README will provide the rationale behind each policy. If further details are required additional examples can be found in the [docs folder](./docs/).

## Table of Contents

**Coding Style Policies:**
- [JAVA-STYLE-001 - Class Naming Convention](#java-style-001---class-naming-convention)
- [JAVA-STYLE-002 - Method Naming Convention](#java-style-002---method-naming-convention)
- [JAVA-STYLE-003 - Variable Naming Convention](#java-style-003---variable-naming-convention)
- [JAVA-STYLE-004 - Constant Naming Convention](#java-style-004---constant-naming-convention)
- [JAVA-STYLE-005 - Package Naming Convention](#java-style-005---package-naming-convention)
- [JAVA-STYLE-006 - Indentation Standards](#java-style-006---indentation-standards)
- [JAVA-STYLE-007 - Line Length Limits](#java-style-007---line-length-limits)
- [JAVA-STYLE-008 - Brace Placement](#java-style-008---brace-placement)

**Security Policies:**
- [JAVA-SEC-001 - Input Validation](#java-sec-001---input-validation)
- [JAVA-SEC-002 - SQL Injection Prevention](#java-sec-002---sql-injection-prevention)
- [JAVA-SEC-003 - Sensitive Data Handling](#java-sec-003---sensitive-data-handling)
- [JAVA-SEC-004 - Exception Information Disclosure](#java-sec-004---exception-information-disclosure)
- [JAVA-SEC-005 - Cryptographic Standards](#java-sec-005---cryptographic-standards)

**Testing Policies:**
- [JAVA-TEST-001 - Test Method Naming](#java-test-001---test-method-naming)
- [JAVA-TEST-002 - Test Coverage Requirements](#java-test-002---test-coverage-requirements)
- [JAVA-TEST-003 - Test Independence](#java-test-003---test-independence)
- [JAVA-TEST-004 - Assertion Usage](#java-test-004---assertion-usage)
- [JAVA-TEST-005 - Test Data Management](#java-test-005---test-data-management)

**Performance Policies:**
- [JAVA-PERF-001 - String Concatenation](#java-perf-001---string-concatenation)
- [JAVA-PERF-002 - Collection Sizing](#java-perf-002---collection-sizing)
- [JAVA-PERF-003 - Resource Management](#java-perf-003---resource-management)
- [JAVA-PERF-004 - Object Creation](#java-perf-004---object-creation)

---

## JAVA-STYLE-001 - Class Naming Convention

**Rule:**
- Class names **MUST** use PascalCase and **SHOULD** be nouns that clearly describe the purpose of the class.

**Rationale:**
- PascalCase is the established Java convention for class names
- Noun-based names clearly indicate what the class represents
- Descriptive names improve code readability and maintainability
- Consistent naming reduces cognitive load when reading code

**Examples:**
- See [docs/JAVA-STYLE-001-class-naming.md](./docs/JAVA-STYLE-001-class-naming.md) for detailed examples

[↑ Back to top](#top)

---

## JAVA-STYLE-002 - Method Naming Convention

**Rule:**
- Method names **MUST** use camelCase and **SHOULD** be verbs that clearly describe the action performed.

**Rationale:**
- camelCase is the established Java convention for method names
- Verb-based names clearly indicate what the method does
- Descriptive names make code self-documenting
- Consistent naming improves code comprehension

**Examples:**
- See [docs/JAVA-STYLE-002-method-naming.md](./docs/JAVA-STYLE-002-method-naming.md) for detailed examples

[↑ Back to top](#top)

---

## JAVA-SEC-001 - Input Validation

**Rule:**
- All user inputs **MUST** be validated and sanitized before processing.

**Rationale:**
- Input validation prevents injection attacks and data corruption
- Sanitization ensures data conforms to expected formats
- Proper validation improves application security and reliability
- Early validation provides better error messages to users

**Examples:**
- See [docs/JAVA-SEC-001-input-validation.md](./docs/JAVA-SEC-001-input-validation.md) for detailed examples

[↑ Back to top](#top)

---

## JAVA-TEST-001 - Test Method Naming

**Rule:**
- Test method names **SHOULD** clearly describe what is being tested using descriptive naming patterns.

**Rationale:**
- Descriptive test names serve as documentation for expected behavior
- Clear naming helps identify failing tests quickly
- Good test names make code reviews more effective
- Self-documenting tests reduce need for additional comments

**Examples:**
- See [docs/JAVA-TEST-001-test-naming.md](./docs/JAVA-TEST-001-test-naming.md) for detailed examples

[↑ Back to top](#top)

---

## JAVA-PERF-001 - String Concatenation

**Rule:**
- String concatenation in loops **MUST** use StringBuilder or StringBuffer.

**Rationale:**
- String objects are immutable in Java, creating new objects for each concatenation
- StringBuilder/StringBuffer use mutable buffers, avoiding object creation overhead
- Significant performance improvement in loops with many concatenations
- Reduces garbage collection pressure

**Examples:**
- See [docs/JAVA-PERF-001-string-concatenation.md](./docs/JAVA-PERF-001-string-concatenation.md) for detailed examples

[↑ Back to top](#top)

---

*Note: This README shows key examples. For complete policy details, see the respective policy files and docs folder.*