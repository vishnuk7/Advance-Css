#### The Visual Formatting Model
Algorithm that calculates boxes and determines the layout of these boxes, 
for each element in the render tree, in order to determine the final
layout of the page

>CSS visual formatting model is an algorithm that calculates boxes and determines the layout 
>of these boxes for each element in the render tree , in order to determine the final layout 
>of the page.This model is one of the fundamental concepts of CSS

>The algorithm takes into account factors like
1. **Dimensions of the boxes**: the box model
2. **Box type**: inline, block and inline-block
3. **Poitioning scheme**: floats and positioning
4. **Stacking contexts**
5. Other elements in the render tree
6. Viewport size, dimensions of images, etc.

##### Box Model
![boxmodel](/screenshot/boxmodel.png)

**Content:** text, images, etc
**Padding** transparent area around the content, inside of the box
**Border** goes around the padding and the content
**Margin** space between boxes
**Fill area** area that gets filled with background color and background image

###### The Box Model: Heights and Widths
**total width** = right border + right padding + specified width + left padding + left border

**total height** = top border + top paddoing + specified height + bottom padding + bottom border

In total height and total width border is also adding and that behaviour we don't want to solve this problem we have 🎭 simple trick that we can use by setting `box-sizing:border-box` now border is not adding up.
>💡 Note that it also not going add padding into total width and total height so final result is **total width** = specified width  and **total height** = specified height

###### Box types: Inline, Blocl-Level and Inline-Block
<span style="background:pink;color:#333;padding:10px">Block Level Boxes</span>

* Elements formatted visually as blocks
* 100% of parent's width
* Vertically one after another
* **<span style="color:palevioletred;">Box-model applies as showed</span>**

```css
  display:block;
  display:flex;
  display:list-item;
  display:table
``` 

<span style="background:palevioletred;color:#fff;padding:10px">Inline Boxes</span>
* Content is distributed in lines
*  **<span style="color:palevioletred;">Occupies only content's space</span>**
* **<span style="color:palevioletred;">No line-breaks</span>**
* No heights and widths
* Padding and margins only horizontal (left and right)

```css
  display:inline
```

<span style="background:maroon;color:#fff;padding:10px">Inline-Block Boxes</span>
* A mix of block and inline
* **<span style="color:palevioletred;">Occupies only content's space</span>**
* **<span style="color:palevioletred;">No line-breaks</span>**
**<span style="color:palevioletred;">Box-model applies as showed</span>**

###### Positioning Schemes: Normal Flow, Absolute Positioning And Floats 

<span style="background:maroon;color:#fff;padding:10px">Normal Flow</span>
* Default positioning scheme
* **Not** floated
* **Not** absolutely positioned
* Elements laid out according to their source order.

```css
  Default
  postion:relative;
```

<span style="background:palevioletred;color:#fff;padding:10px">Floats</span>
* **Element is removed form the normal flow**
* Text and inline elements will wrap around the floated element
* The container will not adjust its height to the elment

```css
  float: left;
  float: right;
```

<span style="background:pink;color:#333;padding:10px">Absolute positioning</span>
* **Element is removed from the normal flow**
* No impact on surrounding content or elements
* We use top, bottom, `left` and `right` to offset the element
  from its relatively positioned container

```css
  positon: absolute;
  position: fixed;
```