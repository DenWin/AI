## BASE-001 - Code Documentation Examples

### Good Documentation Examples

#### API Method Documentation
```java
/**
 * Validates user credentials and returns authentication token.
 * 
 * @param username The username for authentication (required, non-empty)
 * @param password The password for authentication (required, min 8 characters)
 * @return AuthToken containing access token and expiration time
 * @throws AuthenticationException if credentials are invalid
 * @throws ValidationException if username/password format is invalid
 * 
 * @example
 * try {
 *   AuthToken token = authenticateUser("john_doe", "secretPassword");
 *   System.out.println("Token expires at: " + token.getExpirationTime());
 * } catch (AuthenticationException e) {
 *   System.err.println("Login failed: " + e.getMessage());
 * }
 */
public AuthToken authenticateUser(String username, String password) throws AuthenticationException {
    // Implementation details
}
```

#### Class Documentation
```java
/**
 * Manages user session data and provides session-related operations.
 * 
 * This class handles session creation, validation, and cleanup. Sessions
 * are automatically expired after 30 minutes of inactivity.
 * 
 * Thread-safe: This class uses synchronized methods for concurrent access.
 * 
 * @example
 * SessionManager manager = new SessionManager();
 * Session session = manager.createSession(userId);
 * if (manager.isValid(session.getId())) {
 *   // Proceed with authenticated operations
 * }
 */
public class SessionManager {
    // Implementation
}
```

### Bad Documentation Examples

#### Insufficient Documentation
```java
// Bad: No parameter/return documentation
public AuthToken login(String user, String pass) {
    // Implementation
}

// Bad: Vague description
/**
 * Does user stuff.
 */
public void processUser(User user) {
    // Implementation  
}
```