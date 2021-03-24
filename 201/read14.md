# Transforms:
-  Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property.

- Transform property comes in two different settings:
- first one is two-dimensional, and the second one is three-dimensional. Each of these come with their own individual properties and values.


### Transform syntax:
- The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.


### 2D transforms:
- Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane.
- Two-dimentional transforms work on the X & Y axes.

- 2D scale:
- Using the scale value within the transform property allows you to change the appeared size of an element.

- 2D translate:
- The translate value works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow of the document.

- 2D skew:
- The last transform value in the group, skew, is used to distort elements on the horizontal axis, vertical axis, or both.


### Combining transforms:
- It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time.

### Transform origin:
- The transform-origin property can accept one or two values.When only one value is specified, that value is used for both the horizontal and vertical axes. If two values are specified, the first is used for the horizontal axis and the second is used for the vertical axis.


### 3D transforms:
- Working with two-dimensional transforms we are able to alter elements on the horizontal and vertical axes, however there is another axis along which we can transform elements. Using three-dimensional transforms we can change elements on the z axis, giving us control of depth as well as length and width.


### 3D translate:
- Elements may also be translated on the z axis using the translateZ value. A negative value here will push an element further away on the z axis, resulting in a smaller element.


- 3D skew:
-  Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale.



# Transitions & animations:
- Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. 

- Transitions:
- An element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

- Transition duration:
- The duration in which a transition takes place is set using the transition-duration property.

- Transition timing:
- The transition-timing-function property is used to set the speed in which a transition will move. Knowing the duration from the transition-duration property a transition can have multiple speeds within a single duration.

- Transition delay:
- On top of declaring the transition property, duration, and timing function, you can also set a delay with the transition-delay property.

### Shorthand animations:
-  This is accomplished with one animation property, rather than multiple declarations.


- Fade in:
- Having things fade in is a fairly common request from clients. It’s a great way to emphasize functionality or draw attention to a call to action.

- Change color:
- Animating a change of color used to be unbelievably complex, with all kinds of math involved in calculating separate RGB values and then recombining them. Now, we just set the div’s class to “color” and specify the color we want in our CSS.

- Grow & shrink:
- To grow an element, you used to have to use its width and height, or its padding. But now we can use CSS3’s transform to enlarge.

- Rotate elements:
- CSS transforms have a number of different uses, and one of the best is transforming the rotation of an element. 

- Square to circle:
- A really popular effect at the moment is transitioning a square element into a round one, and vice versa. With CSS, it’s a simple effect to achieve, we just transition the border-radius property.

- 3D shadow:
- This effect is achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen.

- Swing:
- It move the elment to thr right and left.

- Inset border:
- One of the hottest button styles right now is the ghost button; a button with no background and a heavy border. 