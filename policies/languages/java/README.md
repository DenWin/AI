<a id="top"></a>

# Java Development Policies

These policies are designed to be concise and precise for AI consumption, while this README will provide the rationale behind each policy. If further details are required additional examples can be found in the [docs folder](./docs/).

## Policies

**Table of Contents**
- **Coding Style Policies** ([java-style.yml](./java-style.yml))
  - [JAVA-STYLE-001 - Class Naming](#java-style-001---class-naming)
  - [JAVA-STYLE-002 - Method Naming](#java-style-002---method-naming)
  - [JAVA-STYLE-003 - Variable Naming](#java-style-003---variable-naming)
  - [JAVA-STYLE-004 - Package Naming](#java-style-004---package-naming)
  - [JAVA-STYLE-005 - Constant Naming](#java-style-005---constant-naming)
  - [JAVA-STYLE-006 - Indentation](#java-style-006---indentation)
  - [JAVA-STYLE-007 - Line Length](#java-style-007---line-length)
  - [JAVA-STYLE-008 - Import Organization](#java-style-008---import-organization)
- **Security Policies** ([java-security.yml](./java-security.yml))
  - [JAVA-SEC-001 - Input Validation](#java-sec-001---input-validation)
  - [JAVA-SEC-002 - SQL Injection Prevention](#java-sec-002---sql-injection-prevention)
  - [JAVA-SEC-003 - Cryptographic Operations](#java-sec-003---cryptographic-operations)
  - [JAVA-SEC-004 - Secure Random Generation](#java-sec-004---secure-random-generation)
  - [JAVA-SEC-005 - File Operations](#java-sec-005---file-operations)
- **Testing Policies** ([java-testing.yml](./java-testing.yml))
  - [JAVA-TEST-001 - Test Method Naming](#java-test-001---test-method-naming)
  - [JAVA-TEST-002 - Test Coverage](#java-test-002---test-coverage)
  - [JAVA-TEST-003 - Test Independence](#java-test-003---test-independence)
  - [JAVA-TEST-004 - Assertion Usage](#java-test-004---assertion-usage)
  - [JAVA-TEST-005 - Mock Usage](#java-test-005---mock-usage)
- **Performance Policies** ([java-performance.yml](./java-performance.yml))
  - [JAVA-PERF-001 - String Concatenation](#java-perf-001---string-concatenation)
  - [JAVA-PERF-002 - Collection Usage](#java-perf-002---collection-usage)
  - [JAVA-PERF-003 - Resource Management](#java-perf-003---resource-management)
  - [JAVA-PERF-004 - Object Creation](#java-perf-004---object-creation)

### Coding Style Policies

#### JAVA-STYLE-001 - Class Naming

*Rule:*
- All class names **MUST** use PascalCase and be descriptive nouns

*Rationale:*
- Follows Java naming conventions and community standards
- Improves code readability and maintainability
- Facilitates team collaboration and code reviews

*Best Practices:*
- Use clear, descriptive names that indicate class purpose
- Avoid abbreviations unless they are widely understood
- Use singular nouns for classes (e.g., User, not Users)
- Consider domain-specific terminology for business classes

*Common Pitfalls:*
- Using vague names like Manager, Helper, or Utility
- Mixing naming conventions within the same codebase
- Using abbreviations that aren't commonly understood

[Back to top](#top)

#### JAVA-STYLE-002 - Method Naming

*Rule:*
- All method names **MUST** use camelCase and start with verbs

*Rationale:*
- Follows Java naming conventions
- Clearly indicates what the method does
- Improves code readability and self-documentation

*Best Practices:*
- Start with action verbs (get, set, calculate, validate)
- Use descriptive names that explain the method's purpose
- Boolean methods should start with is, has, can, or should
- Avoid overlong method names but prioritize clarity

*Common Pitfalls:*
- Using noun-based method names
- Inconsistent naming patterns for similar operations
- Method names that don't reflect actual functionality

[Back to top](#top)

#### JAVA-STYLE-003 - Variable Naming

*Rule:*
- All variable names **MUST** use camelCase and be descriptive

*Rationale:*
- Follows Java naming conventions
- Improves code readability and maintainability
- Reduces need for excessive comments

*Best Practices:*
- Use meaningful names that indicate variable purpose
- Avoid single-letter variables except for loop counters
- Use full words rather than abbreviations
- Consider scope when choosing name length

*Common Pitfalls:*
- Using cryptic abbreviations or single letters
- Names that don't reflect the variable's actual purpose
- Inconsistent naming patterns across methods

[Back to top](#top)

#### JAVA-STYLE-004 - Package Naming

*Rule:*
- All package names **MUST** use lowercase and follow reverse domain naming

*Rationale:*
- Follows Java naming conventions and community standards
- Prevents naming conflicts in large projects
- Provides logical organization of classes

*Best Practices:*
- Use reverse domain notation (com.company.project)
- Keep package names short but descriptive
- Group related functionality logically
- Avoid using Java reserved words

*Common Pitfalls:*
- Using uppercase letters in package names
- Creating overly deep package hierarchies
- Mixing different naming conventions

[Back to top](#top)

#### JAVA-STYLE-005 - Constant Naming

*Rule:*
- All constants **MUST** use UPPER_SNAKE_CASE naming

*Rationale:*
- Follows Java naming conventions
- Makes constants easily identifiable in code
- Distinguishes constants from variables

*Best Practices:*
- Use descriptive names that indicate constant purpose
- Group related constants in interfaces or classes
- Use public static final for true constants
- Consider using enums for related constant groups

*Common Pitfalls:*
- Using camelCase for constants
- Creating mutable "constants"
- Poor grouping of related constants

[Back to top](#top)

#### JAVA-STYLE-006 - Indentation

*Rule:*
- All code **MUST** use consistent indentation of 4 spaces

*Rationale:*
- Ensures consistent code formatting across team
- Improves code readability and structure visibility
- Facilitates code reviews and maintenance

*Best Practices:*
- Configure IDE to use 4 spaces for indentation
- Use spaces instead of tabs for consistency
- Apply consistent indentation to all code structures
- Use automated formatting tools

*Common Pitfalls:*
- Mixing tabs and spaces
- Inconsistent indentation levels
- Manual formatting leading to inconsistencies

[Back to top](#top)

#### JAVA-STYLE-007 - Line Length

*Rule:*
- All lines **MUST** not exceed 120 characters

*Rationale:*
- Ensures code readability on various screen sizes
- Facilitates code reviews and side-by-side comparisons
- Prevents horizontal scrolling in most environments

*Best Practices:*
- Break long lines at logical points
- Use proper indentation for continuation lines
- Consider extracting complex expressions to variables
- Configure IDE to show line length indicators

*Common Pitfalls:*
- Breaking lines at arbitrary points
- Poor indentation of continuation lines
- Ignoring line length limits for readability

[Back to top](#top)

#### JAVA-STYLE-008 - Import Organization

*Rule:*
- All imports **MUST** be organized alphabetically with proper grouping

*Rationale:*
- Improves code organization and readability
- Reduces merge conflicts in version control
- Makes it easier to identify unused imports

*Best Practices:*
- Group imports by package hierarchy
- Remove unused imports regularly
- Use IDE auto-import features with proper configuration
- Avoid wildcard imports except for static imports

*Common Pitfalls:*
- Using wildcard imports unnecessarily
- Disorganized import statements
- Leaving unused imports in code

[Back to top](#top)

### Security Policies

#### JAVA-SEC-001 - Input Validation

*Rule:*
- All external input **MUST** be validated before processing

*Rationale:*
- Prevents injection attacks and data corruption
- Ensures data quality and system stability
- Protects against malicious input and edge cases

*Best Practices:*
- Validate at system boundaries (controllers, APIs)
- Use whitelisting instead of blacklisting when possible
- Implement proper error handling for invalid input
- Use Bean Validation annotations where appropriate

*Common Pitfalls:*
- Trusting client-side validation only
- Incomplete validation leading to vulnerabilities
- Poor error messages that expose system internals

[Back to top](#top)

#### JAVA-SEC-002 - SQL Injection Prevention

*Rule:*
- All database queries **MUST** use prepared statements or parameterized queries

*Rationale:*
- Prevents SQL injection attacks
- Improves query performance through prepared statement caching
- Ensures proper data type handling

*Best Practices:*
- Use PreparedStatement for all dynamic queries
- Never concatenate user input directly into SQL strings
- Use JPA/Hibernate query parameters
- Validate and sanitize input before database operations

*Common Pitfalls:*
- String concatenation for building SQL queries
- Using dynamic query building without proper escaping
- Trusting input validation at application layer only

[Back to top](#top)

#### JAVA-SEC-003 - Cryptographic Operations

*Rule:*
- All cryptographic operations **MUST** use approved algorithms and secure implementations

*Rationale:*
- Ensures data confidentiality and integrity
- Prevents use of weak or deprecated cryptographic methods
- Meets security compliance requirements

*Best Practices:*
- Use AES-256 for symmetric encryption
- Use RSA-2048 or higher for asymmetric encryption
- Use SecureRandom for cryptographic random number generation
- Implement proper key management practices

*Common Pitfalls:*
- Using deprecated algorithms like DES or MD5
- Poor key management and storage
- Using predictable random number generators

[Back to top](#top)

#### JAVA-SEC-004 - Secure Random Generation

*Rule:*
- All random number generation for security purposes **MUST** use SecureRandom

*Rationale:*
- Ensures cryptographically strong random numbers
- Prevents predictable random sequences
- Meets security requirements for tokens and keys

*Best Practices:*
- Use SecureRandom for security-critical random generation
- Properly seed SecureRandom instances
- Use appropriate random number generation for different use cases
- Consider performance implications of SecureRandom

*Common Pitfalls:*
- Using Math.random() for security purposes
- Poor seeding of random number generators
- Using predictable algorithms for security tokens

[Back to top](#top)

#### JAVA-SEC-005 - File Operations

*Rule:*
- All file operations **MUST** validate file paths and implement proper access controls

*Rationale:*
- Prevents path traversal attacks
- Ensures proper file access permissions
- Protects against unauthorized file system access

*Best Practices:*
- Validate and sanitize file paths
- Use canonical paths to prevent directory traversal
- Implement proper file access permissions
- Limit file operation scope to designated directories

*Common Pitfalls:*
- Accepting user-provided file paths without validation
- Missing canonicalization of file paths
- Overly broad file system access permissions

[Back to top](#top)

### Testing Policies

#### JAVA-TEST-001 - Test Method Naming

*Rule:*
- All test methods **MUST** use descriptive names that indicate the test scenario

*Rationale:*
- Improves test maintainability and understanding
- Facilitates debugging when tests fail
- Serves as living documentation of system behavior

*Best Practices:*
- Use should/when/then naming patterns
- Include expected behavior in method names
- Use underscores for readability in test names
- Group related test methods logically

*Common Pitfalls:*
- Generic test names like test1, testMethod
- Names that don't describe the test scenario
- Inconsistent naming conventions across test classes

[Back to top](#top)

#### JAVA-TEST-002 - Test Coverage

*Rule:*
- All code **MUST** achieve minimum 80% line coverage with meaningful tests

*Rationale:*
- Ensures code quality and reduces bugs
- Facilitates safe refactoring and changes
- Provides confidence in system behavior

*Best Practices:*
- Focus on testing business logic and edge cases
- Include both positive and negative test scenarios
- Use code coverage tools to identify gaps
- Prioritize testing critical system components

*Common Pitfalls:*
- Pursuing coverage metrics without meaningful tests
- Missing tests for error conditions
- Over-reliance on unit tests without integration testing

[Back to top](#top)

#### JAVA-TEST-003 - Test Independence

*Rule:*
- All tests **MUST** be independent and able to run in any order

*Rationale:*
- Ensures reliable and consistent test results
- Facilitates parallel test execution
- Reduces test maintenance overhead

*Best Practices:*
- Use @BeforeEach and @AfterEach for setup/cleanup
- Avoid shared mutable state between tests
- Use test fixtures and factory methods for test data
- Clean up resources after each test execution

*Common Pitfalls:*
- Tests that depend on execution order
- Shared static variables between test methods
- Incomplete cleanup leading to test pollution

[Back to top](#top)

#### JAVA-TEST-004 - Assertion Usage

*Rule:*
- All tests **MUST** include specific assertions that verify expected behavior

*Rationale:*
- Ensures tests actually validate system behavior
- Provides clear failure messages when tests fail
- Documents expected system behavior

*Best Practices:*
- Use appropriate assertion methods (assertEquals, assertTrue, etc.)
- Include meaningful assertion messages
- Assert on multiple aspects of results when appropriate
- Use assertThrows for exception testing

*Common Pitfalls:*
- Tests without any assertions
- Using assertTrue for everything instead of specific assertions
- Generic assertion messages that don't help with debugging

[Back to top](#top)

#### JAVA-TEST-005 - Mock Usage

*Rule:*
- All external dependencies in unit tests **MUST** be mocked appropriately

*Rationale:*
- Ensures tests are fast and reliable
- Isolates unit under test from external dependencies
- Enables testing of error scenarios

*Best Practices:*
- Mock external services and databases
- Use Mockito or similar mocking frameworks
- Verify mock interactions when appropriate
- Keep mocks simple and focused on test scenarios

*Common Pitfalls:*
- Over-mocking leading to tests that don't reflect reality
- Complex mock setups that are hard to maintain
- Missing verification of important mock interactions

[Back to top](#top)

### Performance Policies

#### JAVA-PERF-001 - String Concatenation

*Rule:*
- String concatenation in loops **MUST** use StringBuilder or StringBuffer

*Rationale:*
- Prevents performance degradation from repeated string creation
- Reduces memory allocation and garbage collection pressure
- Improves application performance for string-heavy operations

*Best Practices:*
- Use StringBuilder for single-threaded scenarios
- Use StringBuffer for multi-threaded scenarios
- Pre-size StringBuilder when final length is known
- Consider String.join() for simple concatenations

*Common Pitfalls:*
- Using + operator in loops for string concatenation
- Creating unnecessary intermediate string objects
- Not considering thread safety requirements

[Back to top](#top)

#### JAVA-PERF-002 - Collection Usage

*Rule:*
- All collections **MUST** be sized appropriately and use the most efficient implementation

*Rationale:*
- Prevents unnecessary memory allocation and copying
- Improves performance through appropriate data structure selection
- Reduces garbage collection overhead

*Best Practices:*
- Pre-size collections when final size is known
- Choose appropriate collection types for use case
- Use ArrayList for indexed access, LinkedList for frequent insertions
- Consider using Arrays for fixed-size collections

*Common Pitfalls:*
- Using default collection sizes for large datasets
- Choosing inefficient collection types for access patterns
- Unnecessary boxing/unboxing of primitives

[Back to top](#top)

#### JAVA-PERF-003 - Resource Management

*Rule:*
- All resources **MUST** be properly closed using try-with-resources

*Rationale:*
- Prevents resource leaks and memory issues
- Ensures proper cleanup even when exceptions occur
- Improves application stability and performance

*Best Practices:*
- Use try-with-resources for all AutoCloseable resources
- Implement AutoCloseable in custom resource classes
- Handle multiple resources properly in try-with-resources
- Consider resource pooling for expensive objects

*Common Pitfalls:*
- Forgetting to close resources in finally blocks
- Resource leaks in exception scenarios
- Not implementing proper resource cleanup in custom classes

[Back to top](#top)

#### JAVA-PERF-004 - Object Creation

*Rule:*
- Unnecessary object creation **MUST** be avoided in performance-critical code

*Rationale:*
- Reduces garbage collection pressure and memory usage
- Improves application performance and responsiveness
- Prevents memory allocation bottlenecks

*Best Practices:*
- Reuse objects when possible (StringBuilder, collections)
- Use object pools for expensive object creation
- Consider primitive alternatives to wrapper classes
- Use lazy initialization for expensive computations

*Common Pitfalls:*
- Creating objects unnecessarily in loops
- Autoboxing primitives unnecessarily
- Not considering object lifecycle and reuse opportunities

[Back to top](#top)

## Quality Gate

> Evaluate with each adjustment

### Content Verification
- [x] All policies have clear identifiers (JAVA-XXX-001 format)
- [x] Each policy includes rule, rationale, best practices, and common pitfalls
- [x] All RFC-2119 keywords are used appropriately and consistently
- [x] All links and references are valid and accessible
- [x] Content is appropriate for Java development and AI consumption

### Metadata and Structure
- [x] All headings follow proper hierarchy (###, ####)
- [x] Table of Contents matches actual content structure
- [x] All sections include "Back to top" navigation links
- [x] HTML anchor at top of document is present
- [x] Document follows the established template format

### Policy Index File (all_java.yml)
- [x] all_java.yml file exists
- [x] Lists all policies in java directory
- [x] No dead links in index file
- [x] Format follows "last_updated;URL" specification
- [x] URLs point to correct policy files
- [x] All Java policy files are included in index
- [x] HTML anchor at top of document is present
- [x] Document follows the established template format

### Policy File Integration
- [x] All referenced policy files exist and are accessible
- [x] Policy file links in TOC are correct and functional
- [x] Content matches the policies defined in YAML files
- [x] No orphaned or missing policy references
- [x] Version consistency between README and policy files

### Documentation Quality
- [x] Writing is clear, concise, and free of grammatical errors
- [x] Technical terminology is used correctly and consistently
- [x] Java-specific examples and explanations are relevant and helpful
- [x] No redundant or contradictory information
- [x] Professional tone maintained throughout document