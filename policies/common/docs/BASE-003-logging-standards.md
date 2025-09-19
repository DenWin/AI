## BASE-003 - Logging Standards Examples

### General Logging Principles

#### Structured Logging Format
```
{
    "timestamp": "2024-01-15T10:30:00Z",
    "level": "INFO",
    "message": "User authentication successful",
    "context": {
        "userId": "12345",
        "action": "login",
        "ipAddress": "192.168.1.100",
        "userAgent": "Mozilla/5.0..."
    }
}
```

#### Log Levels and Usage
```
ERROR: System errors, exceptions, failures
WARN:  Potential issues, deprecated features
INFO:  General application flow, business events
DEBUG: Detailed diagnostic information

Examples:
ERROR: "Database connection failed"
WARN:  "API response time exceeded threshold"
INFO:  "User created account successfully" 
DEBUG: "Processing user input: {data}"
```

### Language-Agnostic Logging Patterns

#### Good Logging Practices
```
// Include relevant context
log.info("Order processed", {orderId: "12345", amount: 99.99, userId: "user123"})

// Use appropriate log levels
log.error("Payment processing failed", {error: errorDetails, orderId: "12345"})
log.debug("Validating input parameters", {params: inputData})

// Structured format for parsing
log.info("user_action", {
    action: "purchase",
    user_id: "123",
    product_id: "456", 
    amount: 29.99
})
```

#### Bad Logging Examples
```
// Too vague
log.info("Something happened")

// Sensitive data exposed  
log.info("User login: username=john, password=secret123")

// Inconsistent format
log.info("User 123 bought item 456 for $29.99")
log.info("Purchase: {user: 123, item: 456, price: 29.99}")
```