## BASE-003 - Logging Standards Examples

### Good Logging Examples

#### Structured Logging with JSON
```java
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import net.logstash.logback.argument.StructuredArguments;

public class OrderService {
    private static final Logger logger = LoggerFactory.getLogger(OrderService.class);
    
    public void processOrder(Order order) {
        logger.info("Processing order",
            StructuredArguments.kv("orderId", order.getId()),
            StructuredArguments.kv("customerId", order.getCustomerId()),
            StructuredArguments.kv("amount", order.getTotal()),
            StructuredArguments.kv("status", "processing")
        );
        
        try {
            // Process order logic
            logger.debug("Order validation completed",
                StructuredArguments.kv("orderId", order.getId()),
                StructuredArguments.kv("validationTime", System.currentTimeMillis())
            );
        } catch (Exception e) {
            logger.error("Order processing failed",
                StructuredArguments.kv("orderId", order.getId()),
                StructuredArguments.kv("error", e.getMessage()),
                e
            );
        }
    }
}
```

#### Appropriate Log Levels
```java
public class UserService {
    private static final Logger logger = LoggerFactory.getLogger(UserService.class);
    
    public User authenticateUser(String username, String password) {
        logger.debug("Authentication attempt for user: {}", username);
        
        User user = userRepository.findByUsername(username);
        if (user == null) {
            logger.warn("Authentication failed - user not found: {}", username);
            throw new AuthenticationException("Invalid credentials");
        }
        
        if (!passwordEncoder.matches(password, user.getPasswordHash())) {
            logger.warn("Authentication failed - invalid password for user: {}", username);
            throw new AuthenticationException("Invalid credentials");
        }
        
        logger.info("User successfully authenticated: {}", username);
        return user;
    }
}
```