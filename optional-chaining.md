# Optional chaining

In `javascript` you will need to often check if some property of your object exist before handle it. So many dev use this :

```text
const toto = { a: { b: { c: 5 } } }

if (!!toto.a && !!toto.a.b && !!toto.a.b.c) { ... } // toto.a.b.c exist
```

You can use `optional chaining` in order to avoid to use a multiple checker like above.

```text
const toto = { a: { b: { c: 5 } } }

if (!!toto.a?.b?.c) { ... } // toto.a.b.c exist

// If the key doesn't exist, it will return undefined
const test = toto.a?.b?.c?.d // undefined
```



