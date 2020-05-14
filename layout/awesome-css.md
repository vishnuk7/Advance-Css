```css
  nav li:not(:last-child)::after{
    content:"";
    border:1px solid #000;
  } 
```
So line of code tell that add border li::after elements not in last child

```html
  <a href="#menu-main"></a>
```
 below css code going to apply when it os clicked

```css
  .main-menu:target{
    /* when main-menu apply these styles */
  }
```

Adjacent sibling selectors

```css
  .main-menu + .sibling-class{
    /* apply these classes */
  }

```

#### CSS CALC()
1. Ability to do math in CSS
2. Compatible with length, frequency, angle, time, number and integer
* Addition +
* Subtraction +
* Multiplication +
* Division / 

```css
  /* cool part of css calc 😘 you can use different units */
  width: calc(100% - 80px) 
```
#### Advantages
* Can mix units when performing calculations(not possible in Sass)

```css
  .selector{
    width: calc(100 - 2rem)
  }
```

accessing scss variable 
```scss
  width:calc(100% - ${a});
```

#### CSS CUSTOM PROPERTIES
* Kind of like variables, but with "weird quirks" (due to inheritance)

* Must declare custom field within a CSS property -  just like other CSS declarations

* Values inherit - just lile eleswhere in CSS

* Can be used in Javascript

```css
:root{
  --primary: blue;
}

body{
  color:var(--primary);
}

```

##### When should I use sass Vs css custom proprties
* Use sass for global values that don't typocally change: color, font family, etc;
* Use custom properties for values that will change in the media queries: font size, margin, padding, width, flex basic, etc
* Outside the media query, in the mobile CSS layout, establish the logic for layout, then change the values of the custom properties inside the media query.


attribute selector

```css
  [class*="col-"]{
    --width:4;
    --initbasis:calc(var(--width) / var(--columns) * 100);
    --gap:calc((var(--column) - var(--width)) * 1% );
    flex-basis: calc(var(--initbasis) - var(--gap));
  }
```
