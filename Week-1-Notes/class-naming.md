# Class Naming Conventions

An important part of writing maintainable code is the concept of decoupling - 
 making the various parts of your code as independent of each other
as possible.

In CSS, a component's styling should not depend on where it is relative to the
DOM or to other components, and it should not be linked to any Javascript
functionality.

## An Overview of Philip Walton's Guide to Decoupling the Front-End
> The mark of maintainable HTML, CSS, and JavaScript is when individual
> developers can easily and confidently edit parts of the code base without
> those changes inadvertently affecting other, unrelated parts.
> -- <cite>[Philip Walton](https://philipwalton.com/articles/decoupling-html-css-and-javascript/)</cite>

* Style components based on _what_ they are, not _where_ they are.
* Rather than traversing the DOM with complex selectors, better to add more
  clases to the HTML - stick to using single classes and IDs as CSS selectors
  (unless the class is for an altered visual state - see next point).
* Use an "is-" prefix for classes which alter the visual state of a component
  (e.g. "is-visible", "is-inactive").  
  These state classes should _always_ be used in conjunction with the default
  styling classes (e.g. in CSS: .navbar.is-visible {}, _not_ .is-visible {})
* Use a "js-" prefix for _all_ Javascript hooks, even if it seems repetitive
  (e.g. you might have a "js-send" class for functionality and a "send" class for
  styling).
* You may also need a series of base rules which use element
  selectors, e.g. for default link or paragraph styling, or for giving
  a background colour to the body.

## More Structure - BEM (Block Element Modifier)
According to the BEM naming scheme, class names should have the format:
```
block__element--modifier-value
```
or
```
block--modifier-value
```
Spaces are replaced by a dash. Every class name must consist of 
a block, followed by an optional element and/or modifier. Class names should be
short.

### 1. Block
>A standalone entity that is meaningful on its own.  

e.g. `button`, `header`, `menu`, `checkbox`...

### 2. Element
>A part of a block that has no meaning outside of the context of the block.  

e.g. `menu item`, `header title`, `checkbox caption`...  
Only one block or element class name should be used in CSS rules - no tags or
  IDs, and no selectors depending on multiple blocks:

  GOOD CSS selector:  
  ```
  .navbar__item {}
  ```
  BAD CSS Selector:  
  ```
  .navbar .navbar__item {}
  ```

### 3. Modifier
>A flag for changing appearance or behaviour

e.g. `disabled`, `hidden`,
  `checked`, `size big`, `color yellow`...

In the HTML, the modifier is an _extra_ class name to add to a block or
element:  
```
<div class="block block--modifier"></div>
```
The 'value' part of the format is omitted if the modifier is a boolean, e.g
`block__element--hidden` vs `block__element--size-big`. The 'is-' prefix isn't
used in this system.


## Resources
* [Decoupling Your HTML, CSS, and JavaScript](https://philipwalton.com/articles/decoupling-html-css-and-javascript/) _by Philip Walton_
* [BEM naming](http://getbem.com/naming/)
* [Improved
  BEM](http://nicolasgallagher.com/about-html-semantics-front-end-architecture/)
  _by Nicolas Gallagher_
* [BEM for Small
  Projects](https://www.smashingmagazine.com/2014/07/bem-methodology-for-small-projects/)
