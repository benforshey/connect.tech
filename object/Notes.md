# The JavaScript Object Model

Everything in JS is Object, except `null` and `undefined`, and every object has a prototype.

## Ways to make an Object

Object Literal
Object.create
`new` Operator
Reflect.construct

### Object Literals

```js
const someObject = {
    //...
}
```

Linked to `Object.prototype`

### Object.create

Links to object from which it was created as its prototype (still inherits the prototype chain).

### `new` Operator

It is an abomination unto the Lord, and shall never be used. But look it up in DevDocs to see how it differs from Object Literals.

### Reflect.construct

I'm not sure about the use case for this.

```js
function Wedge () {}

Wedge.prototype = Object.create(String.prototype)

Wedge.prototype.toUpperCase = function () {
    return 'nope'
}

let someString = Reflect.construct(String, ['Foo Bar'], Wedge)
someString.toUpperCase() // 'nope'
someString.toLowerCase() // 'foo bar'
```

## Object Properties

`Object.defineProperty()` vs method literal will instantiate properties with different descriptors. Check this out in DevDocs, it seems pretty useful.

## The Object Prototype

Needs a picture.

## Property Resolution

Resolved at the lowest level on the chain. Runs up the chain until it hits `null` as the prototype of Object.prototype. You can shadow properties (parent and child both share the same property name).

## Inheritance

### Class-based Inheritance

Calling `super()` in the `constructor()` gives me access to prototype's methods.

### Prototypal Inheritance
