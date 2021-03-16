# Avoid Else when you return value in your if



```text
if (...) { // the condition is not important in this example
  return 'toto'
} else {
  return 'tutu'
}
```

If your if return value you can just replace the code above by :

```text
if (...) { // the condition is not important in this example
  return 'toto'
}

return 'tutu'
```



