# Common Policy Examples

This directory contains detailed examples and documentation for common development policies.

## Documentation Examples

### Good API Documentation
```java
/**
 * Calculates the total price including tax for a given order.
 * 
 * @param order The order to calculate total for (must not be null)
 * @param taxRate The tax rate to apply (0.0 to 1.0)
 * @return The total price including tax
 * @throws IllegalArgumentException if order is null or taxRate is invalid
 * 
 * @example
 * Order order = new Order(items);
 * double total = calculateTotal(order, 0.08); // 8% tax
 */
public double calculateTotal(Order order, double taxRate) { ... }
```

### Good Commit Messages
```
feat: add user authentication with JWT tokens

- Implement JWT token generation and validation
- Add login/logout endpoints
- Include token refresh mechanism
- Update user model with authentication fields

Closes #123
```

## More detailed examples and rationales for each policy rule can be found in the corresponding policy files.