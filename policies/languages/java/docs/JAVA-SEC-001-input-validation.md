## JAVA-SEC-001 - Input Validation Examples

### Good Input Validation Examples

```java
import javax.validation.constraints.*;
import org.springframework.validation.annotation.Validated;

@RestController
@Validated
public class UserController {
    
    // Using Bean Validation annotations
    public ResponseEntity<User> createUser(
        @Valid @RequestBody CreateUserRequest request) {
        
        // Additional custom validation
        if (userService.existsByEmail(request.getEmail())) {
            throw new ValidationException("Email already exists");
        }
        
        User user = userService.createUser(request);
        return ResponseEntity.ok(user);
    }
}

// Request DTO with validation annotations
public class CreateUserRequest {
    @NotBlank(message = "Username is required")
    @Size(min = 3, max = 50, message = "Username must be 3-50 characters")
    @Pattern(regexp = "^[a-zA-Z0-9_]+$", message = "Username can only contain letters, numbers, and underscore")
    private String username;
    
    @NotBlank(message = "Email is required")
    @Email(message = "Please provide a valid email address")
    private String email;
    
    @NotBlank(message = "Password is required")
    @Size(min = 8, message = "Password must be at least 8 characters")
    private String password;
}
```

### Input Sanitization Examples

```java
public class InputSanitizer {
    
    public String sanitizeHtmlInput(String input) {
        if (input == null) return null;
        
        // Remove potentially dangerous HTML tags and scripts
        return Jsoup.clean(input, Whitelist.basic());
    }
    
    public String sanitizeFileName(String fileName) {
        if (fileName == null) return null;
        
        // Remove path traversal attempts and dangerous characters
        return fileName.replaceAll("[^a-zA-Z0-9._-]", "")
                      .replaceAll("\\.\\.", "");
    }
}
```

### Bad Input Validation Examples

```java
// Bad: No validation
public void createUser(String username, String email) {
    // Direct usage without validation - vulnerable to attacks
    userService.save(new User(username, email));
}

// Bad: Insufficient validation
public void updateProfile(String bio) {
    // No length check or content validation
    user.setBio(bio); // Could be XSS vector
}
```