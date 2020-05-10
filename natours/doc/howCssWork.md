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