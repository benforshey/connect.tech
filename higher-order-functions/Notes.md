# Dr Iterate or: How I Learned to Stop Worrying and Love Higher-Order Functions

## Read

_The Tao of Programming_
Joe Armstrong _Coders at Work_


## Definitions

* Higher-Order Function: a function that takes a function as an argument or returns a function as a value
  * addEventListener is a classic example
* Scope: the values that our worker has access to at any given time
  * you have outer and inner scope
* Closure: The code in brackets and its accompanying scope

```js
const closure = () => {
  const a = 'some value'

  return () => a
}

const getA = closure()

console.log(getA) // 'some value'
```

## Higher-Order Functions

Abstracted means testable. Separate the what from the how. If the how changes, the what doesn't have to.

Feel scared anytime you use `this`, because you're carrying around the implicit environment (Joe Armstrong).

### Lego Architecture

Inject explicit state (dependency injection), passing in the values that you're going to iterate. HOF allow you to create the idea of something, the underlying algorithm.
