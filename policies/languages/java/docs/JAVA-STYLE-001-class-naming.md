## JAVA-STYLE-001 - Class Naming Convention Examples

### Good Class Naming Examples

```java
// Good: PascalCase, descriptive nouns
public class UserService { ... }
public class PaymentProcessor { ... }
public class OrderValidator { ... }
public class EmailNotificationSender { ... }
public class CustomerRepository { ... }
```

### Bad Class Naming Examples

```java
// Bad: Should be PascalCase
public class userService { ... }

// Bad: Too abbreviated, not descriptive
public class PP { ... }
public class USR { ... }

// Bad: Should be noun, not verb
public class ProcessPayments { ... }
public class ValidateOrders { ... }

// Bad: Generic naming
public class Manager { ... }
public class Handler { ... }
public class Helper { ... }
```

### Best Practices

1. **Use PascalCase**: Start with uppercase letter, capitalize each word
2. **Use descriptive nouns**: Class should represent a thing or concept
3. **Be specific**: Avoid generic terms like Manager, Handler, Utils
4. **Avoid abbreviations**: Write full words for clarity
5. **Consider context**: Include domain-specific terminology when appropriate