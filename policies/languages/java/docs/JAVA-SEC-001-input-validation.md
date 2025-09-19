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

### SQL Injection Prevention Examples

```java
// Good: Using PreparedStatement
public List<User> findUsersByRole(String role) {
    String sql = "SELECT * FROM users WHERE role = ?";
    try (PreparedStatement stmt = connection.prepareStatement(sql)) {
        stmt.setString(1, role);  // Parameterized query
        ResultSet rs = stmt.executeQuery();
        return mapResultsToUsers(rs);
    }
}

// Good: Using JPA with named parameters
@Repository
public class UserRepository {
    
    @Query("SELECT u FROM User u WHERE u.role = :role AND u.active = true")
    List<User> findByRole(@Param("role") String role);
}
```

### Bad Input Validation Examples

```java
// Bad: No validation
public void createUser(String username, String email) {
    // Direct usage without validation - vulnerable to attacks
    userService.save(new User(username, email));
}

// Bad: String concatenation in SQL (SQL Injection vulnerable)
public User findUserByEmail(String email) {
    String sql = "SELECT * FROM users WHERE email = '" + email + "'";
    // Vulnerable to SQL injection attacks
    return jdbcTemplate.queryForObject(sql, User.class);
}
```