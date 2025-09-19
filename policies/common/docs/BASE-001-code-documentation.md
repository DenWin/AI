## BASE-001 - Code Documentation Examples

### General Documentation Principles

#### Function/Method Documentation Template
```
/**
 * Brief description of what the function does
 * 
 * @param paramName Description of parameter (type, constraints)
 * @param anotherParam Description of another parameter  
 * @return Description of return value (type, possible values)
 * @throws ExceptionType Description of when this exception occurs
 * 
 * @example
 * exampleUsage(value1, value2);
 * // Expected result: description
 */
```

#### API Documentation Structure
```
Name: authenticateUser
Purpose: Validates user credentials and returns authentication status
Input: username (string, required), password (string, min 8 chars)  
Output: AuthResult object containing success status and token
Errors: AuthenticationError if invalid credentials
Example: authResult = authenticateUser("john", "password123")
```

### Language-Agnostic Documentation Patterns

#### Good Documentation Practices
- Include purpose and behavior description
- Document all parameters with types and constraints
- Specify return values and possible outcomes
- List exceptions or error conditions
- Provide usage examples
- Keep descriptions concise but complete

#### Bad Documentation Examples
- Missing parameter descriptions
- Vague or unclear purpose statements
- No examples or usage guidance
- Outdated information that doesn't match implementation