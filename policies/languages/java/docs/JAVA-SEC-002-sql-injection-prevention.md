## JAVA-SEC-002 - SQL Injection Prevention Examples

### Good SQL Query Examples

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
    
    @Query("SELECT u FROM User u WHERE u.email = :email")
    Optional<User> findByEmail(@Param("email") String email);
}

// Good: Using Criteria API for dynamic queries
public List<User> searchUsers(UserSearchCriteria criteria) {
    CriteriaBuilder cb = entityManager.getCriteriaBuilder();
    CriteriaQuery<User> query = cb.createQuery(User.class);
    Root<User> user = query.from(User.class);
    
    List<Predicate> predicates = new ArrayList<>();
    
    if (criteria.getName() != null) {
        predicates.add(cb.like(user.get("name"), "%" + criteria.getName() + "%"));
    }
    
    if (criteria.getRole() != null) {
        predicates.add(cb.equal(user.get("role"), criteria.getRole()));
    }
    
    query.where(predicates.toArray(new Predicate[0]));
    return entityManager.createQuery(query).getResultList();
}
```

### Bad SQL Query Examples

```java
// Bad: String concatenation (SQL Injection vulnerable)
public User findUserByEmail(String email) {
    String sql = "SELECT * FROM users WHERE email = '" + email + "'";
    // Vulnerable to SQL injection: email could be "'; DROP TABLE users; --"
    return jdbcTemplate.queryForObject(sql, User.class);
}

// Bad: String formatting (still vulnerable)
public List<User> findUsersByName(String name) {
    String sql = String.format("SELECT * FROM users WHERE name LIKE '%%%s%%'", name);
    // Still vulnerable to injection attacks
    return jdbcTemplate.query(sql, userRowMapper);
}

// Bad: Direct concatenation in JPA queries
public List<User> searchByDynamicCriteria(String field, String value) {
    String jpql = "SELECT u FROM User u WHERE u." + field + " = '" + value + "'";
    // Vulnerable to both SQL injection and field injection
    return entityManager.createQuery(jpql, User.class).getResultList();
}
```

### Prevention Best Practices

1. **Always use parameterized queries** - PreparedStatement, JPA parameters, Criteria API
2. **Validate and sanitize inputs** - Even with parameterized queries, validate expected formats
3. **Use ORM frameworks** - JPA, Hibernate provide built-in protection
4. **Avoid dynamic SQL construction** - Use Criteria API for dynamic queries
5. **Apply principle of least privilege** - Database users should have minimal required permissions