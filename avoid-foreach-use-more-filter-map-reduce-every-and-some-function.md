# Avoid ForEach, use more Filter, Map, Reduce, Every & Some function

[https://dev.to/codeozz/improve-your-js-skills-with-theses-tips-52ia](https://dev.to/codeozz/improve-your-js-skills-with-theses-tips-52ia)

## Avoid ForEach, use more Filter, Map, Reduce, Every & Some function

My best advice from this article, as beginner we use a lot of the forEach function, but JS offers you a lot of alternative, and moreover theses function are FP \(functional programming\).

### Filter

As named, it allow us to filter some value in your array depending on your condition.

Returns a new array.

```text
const toto = [1, 2, 3, 4]

const evenValue = toto.filter(currentValue => {
   return currentValue % 2 == 0 // remove all value that return false with this condition
}) // [2, 4]
```

### Map

Use map when you need to transform all items in your item into another item, for exemple if you want to transform all of your number and multiply them by 2

```text
const toto = [1, 2, 3, 4]

const valueMultiplied = toto.map(currentValue => {
   return currentValue * 2 // remove all value that return false with this condition
}) // [2, 4, 6, 8]
```

### Reduce

The most difficult to understand, unliked other function, reduce has another thing, the `accumulator`, wtf is this and when use it ?

A good rules to know if you need to use `reduce` :

Do you need to get a single value from your array ?

For exemple if I want to sum all number in your array into one value, you will need `reduce` and the `accumulator` is the sum ! And as any value, you need to initialise it !

```text
const toto = [1, 2, 3, 4]

const sum = toto.reduce((accumulator, currentValue) => {
   return accumulator += currentValue // you always need to return the accumulator
}, 0) // 10
```

### Some & Every

`some` will check all of your item and when one of the item `match your condition`, it will return `true`, else it will return `false`.

`every` will check all of your item and when one of the item `don't match your condition`, it will return `false`, else it will return `true`.

```text
const toto = [ 2, 4 ]

if (toto.every(val => val % 2 === 0)) { } // You are sure that your array contains only even value

const falsyToto = [ 2, 4, 5 ]

falsyToto.every(val => val % 2 === 0) // return false since array contain a odd value !

```

You can use `some` in the contrary context, for exemple if you want to be sure that your array contain `at least` one odd value

```text
const toto = [ 2, 4, 5 ]

toto.some(val => val % 2 !== 0) // return true
```

