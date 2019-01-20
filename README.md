# Lazy Animations
A big thanks goes out to Animate.css for the start of all of these animations. 


Lazy Animationsis a less wrapper around the Animate.css library. Providing lazy loading and other tools from less to the animate.css library. Just include less-animate.less into your project and copy over all the source files.

## Usage

To use Less-imate in your project. Simply add a import for less-animate.less into your less files and when the less compiler compiles the css it will only load the required keyframs and mixins that you are using. All the other will not be included keeping your css files slim while still providing lots of functionality. 

```css  
@import 'less-animate.less';
```
I have seperated the mixins into 3 main catagories for so its easy to find the animation you are looking for via intellisense. 

.entrance-ANIMATION-NAME 
.exit-ANIMATION-NAME
.attention-ANIMATION-NAME

# Animations currently available

.attention-bounce
.attention-flash
.attention-head-shake
.attention-hear-beat
.attention-jello
.attention-pulse
.attention-rubber-band
.attention-shake
.attention-swing
.attention-tada
.attention-wobble
.attention-flip

.entrance-bounceIn
.entrance-bounceInDown
.entrance-bounceInLeft
.entrance-bounceInRight
.entrance-bounceInUp
.entrance-fadeInLeft
.entrance-fadeInLeftBig
.entrance-fadeIn
.entrance-fadeInDown
.entrance-fadeInDownBig
.entrance-fadeInRight
.entrance-fadeInRightBig
.entrance-fadeInUp
.entrance-fadeInUpBig
.entrance-flipInX
.entrance-flipInY
.entrance-lightSpeedIn
.entrance-rotateIn
.entrance-rotateInDownLeft
.entrance-rotateInDownRight
.entrance-rotateInUpLeft
.entrance-rotateInUpRight
.entrance-slideInDown
.entrance-slideInLeft
.entrance-slideInRight
.entrance-slideInUp
.entrance-jackInTheBox
.entrance-rollIn
.entrance-zoomIn
.entrance-zoomInDown
.entrance-zoomInLeft
.entrance-zoomInRight
.entrance-zoomInUp


.exit-bounceOut
.exit-bounceOutDown
.exit-bounceOutLeft
.exit-bounceOutRight
.exit-bounceOutUp
.exit-fadeOut
.exit-fadeOutDown
.exit-fadeOutDownBig
.exit-fadeOutLeft
.exit-fadeOutLeftBig
.exit-fadeOutRight
.exit-fadeOutRightBig
.exit-fadeOutUp
.exit-fadeOutUpBig
.exit-flipOutX
.exit-flipOutY
.exit-lightSpeedOut
.exit-rotateOut
.exit-rotateOutDownLeft
.exit-rotateOutDownRight
.exit-rotateOutOutUpLeft
.exit-rotateOutUpRight
.exit-rotateOutUpRight
.exit-slideOutDown
.exit-slideOutLeft
.exit-slideOutRight
.exit-slideOutUp
.exit-hinge
.exit-rollOut
.exit-zoomOut
.exit-zoomOutDown
.exit-zoomOut
.exit-zoomOutLeft
.exit-zoomOutRight
.exit-zoomOutUp

