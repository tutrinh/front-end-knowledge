# Multiple Checking

### Includes method to avoid multiples checking

```text
if (value === 'a' || value === 'b' || value === 'c') { ... }
```

Do this instead

```text
if (['a', 'b', 'c'].includes(value)) { ... }
```

