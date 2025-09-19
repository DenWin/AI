# Java Development Policies

## Quick Description

These policies provide AI-friendly guidelines for Java development, covering coding style, security, testing, and performance. The policies are designed to be concise and precise for AI consumption, with detailed explanations available in the [docs folder](./docs/).

## Table of Contents - All Policies in This Folder

### 2.1) [java-style.yml](./java-style.yml) - Coding Style Policies

#### 2.1.1) JAVA-STYLE-001 - Class Naming Convention
Class names must use PascalCase (e.g., `UserService`, `PaymentProcessor`) and should be nouns that clearly describe the class purpose. This ensures consistent naming across the codebase and improves readability.

[↑ Back to top](#java-development-policies)

#### 2.1.2) JAVA-STYLE-002 - Method Naming Convention  
Method names must use camelCase (e.g., `calculateTotal()`, `processPayment()`) and should be verbs describing the action. This makes code self-documenting and follows Java conventions.

[↑ Back to top](#java-development-policies)

#### 2.1.3) JAVA-STYLE-003 - Variable Naming Convention
Variable names must use camelCase (e.g., `userName`, `totalAmount`) and should be descriptive nouns. Avoid abbreviations and single-letter names except for loop counters.

[↑ Back to top](#java-development-policies)

#### 2.1.4) JAVA-STYLE-004 - Constant Naming Convention
Constants must use UPPER_SNAKE_CASE (e.g., `MAX_RETRY_COUNT`, `DEFAULT_TIMEOUT`) and should be declared as `static final`. This distinguishes constants from variables.

[↑ Back to top](#java-development-policies)

#### 2.1.5) JAVA-STYLE-005 - Package Naming Convention
Package names must use lowercase and should follow reverse domain naming (e.g., `com.company.project.module`). This prevents naming conflicts and organizes code logically.

[↑ Back to top](#java-development-policies)

#### 2.1.6) JAVA-STYLE-006 - Indentation Standards
Code must use 4 spaces for indentation and must not use tabs. This ensures consistent formatting across different editors and environments.

[↑ Back to top](#java-development-policies)

#### 2.1.7) JAVA-STYLE-007 - Line Length Limits
Lines should not exceed 120 characters and must not exceed 150 characters. This improves code readability and prevents horizontal scrolling.

[↑ Back to top](#java-development-policies)

#### 2.1.8) JAVA-STYLE-008 - Brace Placement
Opening braces must be placed on the same line as the declaration (K&R style). This follows Java conventions and saves vertical space.

[↑ Back to top](#java-development-policies)

### 2.2) [java-security.yml](./java-security.yml) - Security Policies

#### 2.2.1) JAVA-SEC-001 - Input Validation
All user inputs must be validated and sanitized to prevent injection attacks and ensure data integrity. Use validation frameworks and never trust user input.

[↑ Back to top](#java-development-policies)

#### 2.2.2) JAVA-SEC-002 - SQL Injection Prevention
Database queries must use parameterized statements or prepared statements to prevent SQL injection attacks. Never concatenate user input directly into SQL strings.

[↑ Back to top](#java-development-policies)

#### 2.2.3) JAVA-SEC-003 - Sensitive Data Handling
Sensitive data (passwords, tokens, personal information) must not be logged and should be encrypted when stored. Use appropriate encryption and masking techniques.

[↑ Back to top](#java-development-policies)

#### 2.2.4) JAVA-SEC-004 - Exception Information Disclosure
Exception messages must not expose sensitive system information to end users. Log detailed errors internally but show generic messages to users.

[↑ Back to top](#java-development-policies)

#### 2.2.5) JAVA-SEC-005 - Cryptographic Standards
Cryptographic operations must use industry-standard algorithms (AES, RSA, etc.) and should follow current best practices. Avoid deprecated algorithms.

[↑ Back to top](#java-development-policies)

### 2.3) [java-testing.yml](./java-testing.yml) - Testing Policies

#### 2.3.1) JAVA-TEST-001 - Test Method Naming
Test method names should clearly describe what is being tested using patterns like `should_ReturnResult_When_Condition()` or `testMethodName_Scenario_ExpectedResult()`.

[↑ Back to top](#java-development-policies)

#### 2.3.2) JAVA-TEST-002 - Test Coverage Requirements
Unit tests should achieve at least 80% code coverage for business logic. Focus on testing critical paths and edge cases.

[↑ Back to top](#java-development-policies)

#### 2.3.3) JAVA-TEST-003 - Test Independence
Tests must be independent and must not rely on execution order. Each test should set up its own data and clean up afterward.

[↑ Back to top](#java-development-policies)

#### 2.3.4) JAVA-TEST-004 - Assertion Usage
Tests must include meaningful assertions with descriptive messages. Use `assertThat()` with clear descriptions of what is expected.

[↑ Back to top](#java-development-policies)

#### 2.3.5) JAVA-TEST-005 - Test Data Management
Test data should be isolated per test and must be cleaned up after execution. Use test databases or in-memory data stores when possible.

[↑ Back to top](#java-development-policies)

### 2.4) [java-performance.yml](./java-performance.yml) - Performance Policies

#### 2.4.1) JAVA-PERF-001 - String Concatenation
String concatenation in loops must use `StringBuilder` or `StringBuffer` to avoid creating multiple string objects and improve performance.

[↑ Back to top](#java-development-policies)

#### 2.4.2) JAVA-PERF-002 - Collection Sizing
Collections should be initialized with appropriate initial capacity when size is known to avoid unnecessary resizing operations.

[↑ Back to top](#java-development-policies)

#### 2.4.3) JAVA-PERF-003 - Resource Management
Resources (files, connections, streams) must be properly closed using try-with-resources or finally blocks to prevent memory leaks.

[↑ Back to top](#java-development-policies)

#### 2.4.4) JAVA-PERF-004 - Object Creation
Unnecessary object creation should be avoided in performance-critical code paths. Consider object pooling or reuse when appropriate.

[↑ Back to top](#java-development-policies)