# Java Style Policy Examples

This directory contains detailed examples and documentation for Java coding style policies.

## Class Naming Examples

### Good Examples
```java
public class UserService { ... }
public class PaymentProcessor { ... }
public class OrderValidator { ... }
```

### Bad Examples
```java
public class userService { ... }    // Should be PascalCase
public class PP { ... }             // Too abbreviated
public class ProcessPayments { ... } // Should be noun, not verb
```

## Method Naming Examples

### Good Examples
```java
public void calculateTotal() { ... }
public boolean isValid() { ... }
public String formatCurrency(double amount) { ... }
```

### Bad Examples
```java
public void CalculateTotal() { ... }  // Should be camelCase
public void calc() { ... }           // Too abbreviated
public void data() { ... }           // Not descriptive
```

## More detailed examples and rationales for each policy rule can be found in the corresponding policy files.