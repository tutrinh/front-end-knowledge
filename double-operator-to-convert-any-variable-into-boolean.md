# Double ! operator to convert any variable into boolean

The `!` \(NOT\) operator can be use two times `!!` in order to convert any variable into boolean \(like Boolean function\), very convenient when you need to check some value before handle it.

```text
const toto = null

!!toto // false
Boolean(toto) // false

if (!!toto) { } // toto is not null or undefined
```



