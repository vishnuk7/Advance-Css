#### CSS Transition
A transition describes how a property should display change when given a different value

```css
transition:scale 2s;
```

Anatomy of a transition
* **transition-property** the property you want to transition
* **teansition-duration** in seconds or milliseconds: 4s or 4000ms (best choice is use `ms` if you are using with javascript)

* **transition-timing-functions** "cushioning" for the transition, **optional** default to `ease`

* **transition-delay** the number of milli/seconds to delay the transition before firing it, **optional**

```css
transition-property:all;
```
this not so much performent, by doing this it use lot of resoures

Nice and best way to write a CSS transition 😎

```css
.selector{
  transition: color 2s, transform 300ms 1s;
  }
```

Duration
Three timeframes for user attention
* 100ms, instantaneous
* 1 second, still connected
 
Sweet 🍬 point is between 100ms to 1s

#### Studio animation rule of thumb
However long your pre-production animation, have its duration... then halve it again...

In UI animation sweet 🍬 spot is between 250~350ms

> faster != better

#### Timing function
*Easing*
Easing, also know as "cushioning" in studio animation, desctibes an animation's rate of change over time.

Timing function values
- linear
- ease-in
- ease-out
- ease-in-out
- steps

**cubic-bezier** custom timing function