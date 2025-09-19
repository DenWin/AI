## BASE-002 - Error Handling Examples

### Good Error Handling Examples

#### Graceful Exception Handling
```java
public class FileProcessor {
    public ProcessResult processFile(String filename) {
        try {
            File file = new File(filename);
            if (!file.exists()) {
                return ProcessResult.error("File not found: " + filename);
            }
            
            // Process file content
            String content = Files.readString(file.toPath());
            return ProcessResult.success(processContent(content));
            
        } catch (IOException e) {
            logger.error("Failed to read file: " + filename, e);
            return ProcessResult.error("Unable to read file. Please check file permissions.");
        } catch (SecurityException e) {
            logger.error("Security error accessing file: " + filename, e);
            return ProcessResult.error("Access denied. Contact administrator.");
        }
    }
}
```

#### User-Friendly Error Messages
```java
public class UserRegistration {
    public RegistrationResult register(UserData userData) {
        try {
            validateUserData(userData);
            User user = createUser(userData);
            return RegistrationResult.success(user);
        } catch (ValidationException e) {
            // Return specific, actionable error message
            return RegistrationResult.error(
                "Registration failed: " + e.getMessage() + 
                ". Please correct the highlighted fields and try again."
            );
        } catch (DuplicateUserException e) {
            return RegistrationResult.error(
                "An account with this email already exists. Please use a different email or try to log in."
            );
        }
    }
}
```

### Bad Error Handling Examples

#### Poor Exception Handling
```java
// Bad: Swallowing exceptions
try {
    riskyOperation();
} catch (Exception e) {
    // Silent failure - error is lost
}

// Bad: Generic error messages
catch (Exception e) {
    throw new RuntimeException("Something went wrong");
}

// Bad: Exposing internal details
catch (SQLException e) {
    throw new RuntimeException("Database error: " + e.getMessage()); // Exposes DB structure
}
```