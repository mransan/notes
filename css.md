
Online Resources
----------------

* Flex positionnig: http://flexboxfroggy.com/
* Selection rule: http://flukeout.github.io/
* Trying things out: https://jsfiddle.net/
* Tutorial: http://learn.shayhowe.com/html-css/
* Classes: https://bento.io/track/front-end
* HackerNews: https://news.ycombinator.com/item?id=11048409

Selection
---------

**type** 

An element type is that tag name of the element (ie div for <div>, p for <p>).

```css
div {
  /* rules */
}
```

**id**

HTML elements can have a special attribute `id`. css has a shortcut for 
selection based on `id` attribute using the `#` prefix.

```css 
#blah { 
  /* rules */
}
```

Above rule will apply to element with `id` `blah` 

**class**

HTML elements can have a special attribute `class`, unlike `id` it can 
be used on multiple elements. css has a shortcut for selection based on `class`
attribute using the `.` prefix.

```css 
.blah { 
  /* rules */
}
```

Above rule will apply to element with `class` `blah`. You can limit the 
rule to a specific combination of type and class by appending a type with
a class:

```css
p.blah { /* rules */ } 
```

In this case, the rule will only apply to the `p` element with class `blah`.

**Descendent**

`A B`: 2 rules separate by a space means `inside`. `A B` means `B` selection only in
`A` selection. A/B could be a type/id/class selection.

**Combination**

`A, B`: Rules separated with commas are combined selector, ie the rules will apply
to all the selector.

```css
p, a { /* rules */ } 
```
In this case the rules will apply to all element with type `p` and `a`.

> see [here](https://jsfiddle.net/4900dpg4/3/i) for an example

**Universal selector**

`*`

```css 
p * { /* rules */ } 
```
In this case the rules will apply to all elements within `p` but not `p` 
itself.

**First/Adjacent Sibling selector**

`A+B`: First element matching `B` that comes after any element matching `A`.

**All Siblings selector**

`A~B`: All elements matching `B` that comes after any element matching `A`.

> see [here](https://jsfiddle.net/h2s1vknp/) for an example.


Positioning using Flex
---------------------

> To enable add the property `display:  flex;`

**justify-content**

Justification of element 
* `flex-start` (align to the left)
* `flex-end` (align to the right) 
* `center` (align in the center) 
* `space-between` (maximize equal space in between child element, 
   it will push first element to the left and last to the right) 
* `space-around` (equal space around element).

**align-items**

Alignment: same values as justify-content

**flex-direction**

Defines the direction of items:
* `row` : all items inside of a singel row in the order of HTML declaration
* `row-reverse': same as row but in reverse order of HTML declaration
* `column` : all items inside of a single column in the order of 
   HTML declaration
* `column-reverse': same as column but in reverse order

**order**

Positive/Negative number, by default order are 0. 

**align-self**

Same as `align-items` but for the element that it applies too. (align-items 
are for all the containing element).

**flex-wrap**

Controls wrapping of elements:
* `nowrap`
* `wrap`
* `wrap-reverse`

**flex-flow**

2-value attribute combining flex-direction and flex-wrap.

**align-content** 

Controls alignement for when elements are wrapped.
