## BASE-002 - Error Handling Examples

### General Error Handling Principles

#### Graceful Error Handling Pattern
```
function processData(input) {
    try {
        // Validate input
        if (!isValid(input)) {
            return ErrorResult("Invalid input: " + getValidationMessage(input))
        }
        
        // Process data
        result = performOperation(input)
        return SuccessResult(result)
        
    } catch (ValidationError e) {
        logError("Validation failed", e)
        return ErrorResult("Please check your input and try again")
    } catch (SystemError e) {
        logError("System error occurred", e)
        return ErrorResult("Service temporarily unavailable. Please try again later")
    }
}
```

#### User-Friendly Error Messages
```
Good Examples:
- "Email address is required"
- "Password must be at least 8 characters"
- "File upload failed. Please try again or contact support"
- "Connection timeout. Please check your internet connection"

Bad Examples:
- "Error 500" (no context)
- "Something went wrong" (too vague)
- "NullPointerException at line 42" (technical details exposed)
- "Database constraint violation" (internal details exposed)
```

### Language-Agnostic Error Handling Practices

#### Error Response Structure
```
{
    "success": false,
    "error": {
        "code": "VALIDATION_ERROR",
        "message": "The provided data is invalid",
        "details": "Email field is required"
    }
}
```

#### Error Logging Best Practices
- Log detailed technical errors internally
- Provide user-friendly messages to end users
- Include context and timestamps in logs
- Use appropriate log levels (ERROR, WARN, INFO)
- Never log sensitive information like passwords