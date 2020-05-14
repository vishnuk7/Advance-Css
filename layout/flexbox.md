If you really want to learn flexbox 😀. You just need to take care only one thing which is understand child partent relationship.

Flexbox is all about parent child relationship.

```css
  display:flex
```

Above line of code define the flex container 

```css
  flex-flow: row wrap;
```

>💡 if you define `wrap` proprty then items are not going to overflow
>💡 `nowrap` means there no wrap then is only one line 

`flex-flow` is a shorthand for the `flex-direction` and `flex-wrap` 


`justify-content:space-between`

The CSS `justify-content` property defines how the browser distributes space between and around content items along the `main-axis` of a flex container, and the inline axis of a grid container.

`align-content: stretch`

The CSS align-content property sets the distribution of space between and around content items along a flexbox's cross-axis or a grid's block axis.

> Distribute items evenly Stretch 'auto'-sized items to fit the container 

```css
  flex-basis: 32%
```
It specifies the initial size of the flex item, before any available space is distributed according to the flex factors. When omitted from the flex shorthand, its specified value is the length zero.

A flex-basis value set to auto sizes the element according to its size property (which can itself be the keyword auto, which sizes the element based on its contents).