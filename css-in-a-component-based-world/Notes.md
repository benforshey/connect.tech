# CSS in a Component Based World

## Common Tool to Solve Global Scope in CSS

### Sass & Less

* more sophisticated syntax, with mixins, functions, logic, variables, etc.
* does not enforce a naming convention, so namespace collision is still possible

### BEM

* [BEM Getting Started](https://en.bem.info/methodology/quick-start/)
* less dry?

### Styling Inside Components (CSS in JS)

* Christopher Chedeau's talk from 2015 (Facebook)
* We must realize that although we can isolate the scope of CSS through unique styles or inlined styles, CSS Properties still inherit from parent components.
* Losing inheritance from a global scope means that you'll be repeating yourself often: how many times do we use a button reset, uniquely?
* Radium, Aphrodite, Styled-Components
* Pros: unified source for reusable pieces; scoped selectors
* Cons: size of over-the-wire bundle increases, because you're not using global inheritance

### Modular CSS

* It lets you write CSS, embrace the global inheritance when needed, and isolate when best.
* It's the way to go, period. 😊

## Refactoring CSS

* Try to avoid the need to refactor by choosing a good architecture pattern beforehand (I would say even with Modular CSS).
