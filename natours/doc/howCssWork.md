#### How Css Work
```css
selector{
  property:declared-value; /* <- Declaration */
}/* <- Declaration Block */

```

First Step of CSS parsing

**Cascade**
Process of combining different stylesheets and resolving conflicts between different CSS rules and 
declarations, when more than one rule applies to a certain element.

>There are three types of declarations
1. Author (declared by developer)
2. User (changing the browser font)
3. Browser (user agent) (default declarations)

So, How cascade resolve the conflicts 😕
It check below three things according to precedence

`importance > specificity > source order`\

How the importance work according precdence
* importance
 1. User !important declarations
 2. Author !important declarations
 3. Author declarations
 4. User declarations
 5. Default Browser declarations

>When there is same importance 😕? it check for specificty

 * specificty
  1. Inline style 
  2. IDs
  3. Classes, pseudo-classes, attribute
  4. Elements, pseudo-elements

>When there is same specificity 😕? it check source order

* source order
  > The last declaration in the code will override all other declaration and will be applied.

>💡 CSS declarations marked with `!important` haev the highest priority.
>💡 But, only use `!important` as a last resoures. It's better to use correct specificities - **more maintainable code!**
>💡 Inline style will always have priority over style in external stylesheets.
>💡 A selector that contains **1** ID is more specific than one with **1000** classes.
>💡 A selector that contains **1** class is more specific than one with **1000** elements.
>💡 The universal selector * has no specificity value(0,0,0,0) `value(inline style,ID,classes,elements)`
>💡 Rely more on **specificity** that on the **order**   of selectors.
>💡 But, rely on order when using 3rd-party stylesheets - always put your author stylesheet last *so here order is important* 

Second Step of CSS parsing
 
> How  unit are converted from relative to absolute (px)
`%fonts`% is not an unit if you use `%` then the final output is on `px`it is computed `x% * parent's computed font-size` 
`% lenght` if use % in padding then it computed with parent's width example `x% * parent's width`

**font-based units**
1. em(font) => `3em = x * parent computed font-size`
2. em(lenght) => `x * current element computed font-size`
3. rem it work for both font and lenght => `x * root computed font-size`
4. vh => `x * 1% of viewport height`
5. vw => `x * 1% of viewport width`

>💡 Each property has an initial value, used if nothing is declared (and if there is no inheritance )
>💡 Browsers specify a **root font-size** for each page(usually 16px)
>💡 Percentages and relative values are always converted into pixels
>💡 Percentages are measured relative to their parent's **font-size**, if used to specify `font-size`
>💡 Percentages are measured relative to their parent's width, if used to specify lenghts.
>💡 em are meaured relative to their **parent** font-size, if used to specify font-size
>💡 em are meaured relative to their **current** font-size, if used to specify lenghts
>💡 rem are always measured relative to the `document's root` font-size

CSS Inheritance

>Every CSS property must have a value

`if is there a cascade value?` then `Specified value = cascade value`;
`eles there is no cascade value` them `is the property inherited?(specific to each property)` then `specified value = computed value of parent element ` 
else `specified value = initial value (specific to each property)`

>💡 Inheritance passes the value for some specific properties from parents to children - **more maintainable code**
>💡 Properties related to text are inherited: font-family,font-size,color,etc
>💡 The computed value of a property is what gets inherited, not the declared value.
>💡 Inheritance of a property only works if no one declares a value fot that property
>💡 The `inherit` keyword forces inheritance on a certain propery
>💡 The `initial` keyword resets a property to its initial value