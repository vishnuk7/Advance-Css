```css
  display:grid;
```
above line of code create a grid container

```css
  grid-template-columns: repate(3, 1fr);
  /* 
  so it is all about defining grid columns
  create three columns with 1fr unit 
  */
```

To arranging the colmuns we have three different ways

1. 
```css
.box{
  grid-column: span 2;
}

```
2. 
```css
.box{
  grid-colum: 1/2;
}
```
3.
```css
.container{
  grid-template-areas:
  "a a b"
  "c c c"
  "d e f"
  "g h h"
}

.a{
  grid-area:a;
}
```