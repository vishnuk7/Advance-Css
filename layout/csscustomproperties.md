#### CSS CUSTOM PROPERTIES
[smash](https://www.smashingmagazine.com/2018/05/css-custom-properties-strategy-guide/)


Variables in preprocssors hav a kind of "block scope"

```scss
$background: red;
.example {
  $background: blue;
  background: $background;
}

.example {
  background: $background;
}
```
This will be result in:
```css
.example {
  background: blue;
}
.example {
  background: red;
}
```

>🤯 Custom properties work differently. Where custom properties are concerned, dynamically scoped means they are subject to `inheritance` and the `cascade`.

This is great because you can change the value of a custom property inside a media query, with a pseudo selector such as hover, or even with JavaScript.

```css
a {
  --link-color: black;
}
a:hover,
a:focus {
  --link-color: tomato;
}
@media screen and (min-width: 600px) {
  a {
    --link-color: blue;
  }
}

a {
  color: var(--link-color);
}

```

#### Global vs. Local
 We have some things that are applied globally and some things that are more local. Brand colors, vertical spacing, and typography are all examples of things you might want to be applied globally and consistently across your website or application. We also have local things. For example, a button component might have a small and large variant. You wouldn’t want the sizes from these buttons to be applied to all input elements or even every element on the page.

>💡 Use preprocessor variables for global values which going to be `static` and which is not going not change.
>💡 Use css custom properties for local variables
 

##### When To Use Custom Properties
**When should we use custom properties?**
Converting existing preprocessor variables to custom properties usually makes little sense. After all, the reason for custom properties is completely different. Custom properties make sense when we have CSS properties that change relative to a condition in the DOM — especially a dynamic condition such as `:focus`, `:hover`, media queries or with JavaScript.

*I think in most situations we are going to be working with a combination of preprocessor variables and custom properties.*

```scss
$button-sml: 1em;
$button-med: 1.5em;
$button-lrg: 2em;

.btn {
  --button-size: #{$button-sml};
}

@media screen and (min-width: 600px) {
  .btn-med {
    --button-size: #{$button-med};
  }
  .btn-lrg {
    --button-size: #{$button-lrg};
  }
}

.btn {
  font-size: var(--button-size);
}

```

Just try it!
It make life easier😎 