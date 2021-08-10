# CSS Transforms, Transitions, and Animations
The transform CSS property lets you rotate, scale, skew, or translate an element. It modifies the coordinate space of the CSS visual formatting model.
## CSS Demo: transformReset
transform: matrix(1, 2, 3, 4, 5, 6);
transform: translate(120px, 50%);
transform: scale(2, 0.5);
transform: rotate(0.5turn);
Copy to Clipboard
transform: skew(30deg, 20deg);
transform: scale(0.5) translate(-100%, -100%);
If the property has a value different than none, a stacking context will be created. In that case, the element will act as a containing block for any position: fixed; or position: absolute; elements that it contains.

Syntax
/* Keyword values */
transform: none;

/* Function values */
transform: matrix(1.0, 2.0, 3.0, 4.0, 5.0, 6.0);
transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
transform: perspective(17px);
transform: rotate(0.5turn);
transform: rotate3d(1, 2.0, 3.0, 10deg);
transform: rotateX(10deg);
transform: rotateY(10deg);
transform: rotateZ(10deg);
transform: translate(12px, 50%);
transform: translate3d(12px, 50%, 3em);
transform: translateX(2em);
transform: translateY(3in);
transform: translateZ(2px);
transform: scale(2, 0.5);
transform: scale3d(2.5, 1.2, 0.3);
transform: scaleX(2);
transform: scaleY(0.5);
transform: scaleZ(0.3);
transform: skew(30deg, 20deg);
transform: skewX(30deg);
transform: skewY(1.07rad);

/* Multiple function values */
transform: translateX(10px) rotate(10deg) translateY(5px);
transform: perspective(500px) translate(10px, 0, 20px) rotateY(3deg);

/* Global values */
transform: inherit;
transform: initial;
transform: revert;
transform: unset;
Copy to Clipboard
The transform property may be specified as either the keyword value none or as one or more <transform-function> values.

If perspective() is one of multiple function values, it must be listed first.
  Values
One or more of the CSS transform functions to be applied. The transform functions are multiplied in order from left to right, meaning that composite transforms are effectively applied in order from right to left.
none
Specifies that no transform should be applied.
Accessibility concerns
Scaling/zooming animations are problematic for accessibility, as they are a common trigger for certain types of migraine. If you need to include such animations on your website, you should provide a control to allow users to turn off animations, preferably site-wide.

Also, consider making use of the prefers-reduced-motion media feature — use it to write a media query that will turn off animations if the user has reduced animation specified in their system preferences.
  *****************************************************************************
  # CSS transitions 
  CSS transitions allows you to change property values smoothly, over a given duration.

 Mouse over the element below to see a CSS transition effect:
  How to Use CSS Transitions?
To create a transition effect, you must specify two things:

the CSS property you want to add an effect to
the duration of the effect
Note: If the duration part is not specified, the transition will have no effect, because the default value is 0.

The following example shows a 100px * 100px red <div> element. The <div> element has also specified a transition effect for the width property, with a duration of 2 seconds:

Example
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s;
}

The transition effect will start when the specified CSS property (width) changes value.

Now, let us specify a new value for the width property when a user mouses over the <div> element:

Example
div:hover {
  width: 300px;
}
Notice that when the cursor mouses out of the element, it will gradually change back to its original style.

  Change Several Property Values
The following example adds a transition effect for both the width and height property, with a duration of 2 seconds for the width and 4 seconds for the height:

Example
div {
  transition: width 2s, height 4s;
}
  Specify the Speed Curve of the Transition
The transition-timing-function property specifies the speed curve of the transition effect.

The transition-timing-function property can have the following values:

ease - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
linear - specifies a transition effect with the same speed from start to end
ease-in - specifies a transition effect with a slow start
ease-out - specifies a transition effect with a slow end
ease-in-out - specifies a transition effect with a slow start and end
cubic-bezier(n,n,n,n) - lets you define your own values in a cubic-bezier function
The following example shows some of the different speed curves that can be used:

Example
#div1 {transition-timing-function: linear;}
#div2 {transition-timing-function: ease;}
#div3 {transition-timing-function: ease-in;}
#div4 {transition-timing-function: ease-out;}
#div5 {transition-timing-function: ease-in-out;}
**********************************************************************************************************8
# Css Animation
  CSS allows animation of HTML elements without using JavaScript or Flash!

## What are CSS Animations?
An animation lets an element gradually change from one style to another.

You can change as many CSS properties you want, as many times as you want.

To use CSS animation, you must first specify some keyframes for the animation.

Keyframes hold what styles the element will have at certain times.
  The @keyframes Rule
When you specify CSS styles inside the @keyframes rule, the animation will gradually change from the current style to the new style at certain times.

To get an animation to work, you must bind the animation to an element.

The following example binds the "example" animation to the <div> element. The animation will last for 4 seconds, and it will gradually change the background-color of the <div> element from "red" to "yellow":

Example
/* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
Note: The animation-duration property defines how long an animation should take to complete. If the animation-duration property is not specified, no animation will occur, because the default value is 0s (0 seconds). 

In the example above we have specified when the style will change by using the keywords "from" and "to" (which represents 0% (start) and 100% (complete)).

It is also possible to use percent. By using percent, you can add as many style changes as you like.

The following example will change the background-color of the <div> element when the animation is 25% complete, 50% complete, and again when the animation is 100% complete:

Example
/* The animation code */
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
The following example will change both the background-color and the position of the <div> element when the animation is 25% complete, 50% complete, and again when the animation is 100% complete:

Example
/* The animation code */
@keyframes example {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
  Delay an Animation
The animation-delay property specifies a delay for the start of an animation.

The following example has a 2 seconds delay before starting the animation:

Example
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: 2s;
}
Negative values are also allowed. If using negative values, the animation will start as if it had already been playing for N seconds.

In the following example, the animation will start as if it had already been playing for 2 seconds:

Example
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: -2s;
}
Set How Many Times an Animation Should Run
The animation-iteration-count property specifies the number of times an animation should run.

The following example will run the animation 3 times before it stops:

Example
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 3;
}
The following example uses the value "infinite" to make the animation continue for ever:

Example
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: infinite;
}
Run Animation in Reverse Direction or Alternate Cycles
The animation-direction property specifies whether an animation should be played forwards, backwards or in alternate cycles.

The animation-direction property can have the following values:

normal - The animation is played as normal (forwards). This is default
reverse - The animation is played in reverse direction (backwards)
alternate - The animation is played forwards first, then backwards
alternate-reverse - The animation is played backwards first, then forwards
The following example will run the animation in reverse direction (backwards):

Example
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-direction: reverse;
}
The following example uses the value "alternate" to make the animation run forwards first, then backwards:

Example
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate;
}
The following example uses the value "alternate-reverse" to make the animation run backwards first, then forwards:

Example
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate-reverse;
}


  
