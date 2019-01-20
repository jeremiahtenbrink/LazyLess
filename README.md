# Lazy Animations
A big thank you goes out to [Animate.css](https://github.com/daneden/animate.css "Animate.css Github") for the start of all of these animations. 


Lazy Animationsis a less wrapper around the Animate.css library. Providing lazy loading and other tools from less to the animate.css library. Just include less-animate.less into your project and copy over all the source files.

## Usage

To use Lazy Animations in your project. Simply add a import for less-animate.less into your less files and when the less compiler runs the compiler will only load the required keyframs and mixins that you are using. All the others will not be included keeping your css files slim while still providing lots of functionality. 

```css  
@import 'less-animate.less';
```

Then in your css use the animations by calling the mixins. 

```$less
.someClass{

    
  .animation-infinite;    /*make the animation infinite*/
  
  .animation-delay(.4s);  /*delay the aniimation for x time*/
  
  .attention-bounce(2s);    /*call the animation and set a duration for the animation to take place*/
  
  &:hover {   /*set up animations on hover*/
    
    .exit-fadeOut();   /*call animation with default duration*/
  }
  
  :active {   /*call animation on active pseudo class*/
  
    .attention-flash;   /*call animation with default duration*/
  }
  
}
```
I have seperated the mixins into 3 main catagories for so its easy to find the animation you are looking for via intellisense. 

.entrance-ANIMATION-NAME 
.exit-ANIMATION-NAME
.attention-ANIMATION-NAME

# Animations currently available

## Attention Animation 
* .attention-bounce
* .attention-flash
* .attention-head-shake
* .attention-hear-beat
* .attention-jello
* .attention-pulse
* .attention-rubber-band
* .attention-shake
* .attention-swing
* .attention-tada
* .attention-wobble
* .attention-flip

## Entrance Animations
* .entrance-bounceIn
* .entrance-bounceInDown
* .entrance-bounceInLeft
* .entrance-bounceInRight
* .entrance-bounceInUp
* .entrance-fadeInLeft
* .entrance-fadeInLeftBig
* .entrance-fadeIn
* .entrance-fadeInDown
* .entrance-fadeInDownBig
* .entrance-fadeInRight
* .entrance-fadeInRightBig
* .entrance-fadeInUp
* .entrance-fadeInUpBig
* .entrance-flipInX
* .entrance-flipInY
* .entrance-lightSpeedIn
* .entrance-rotateIn
* .entrance-rotateInDownLeft
* .entrance-rotateInDownRight
* .entrance-rotateInUpLeft
* .entrance-rotateInUpRight
* .entrance-slideInDown
* .entrance-slideInLeft
* .entrance-slideInRight
* .entrance-slideInUp
* .entrance-jackInTheBox
* .entrance-rollIn
* .entrance-zoomIn
* .entrance-zoomInDown
* .entrance-zoomInLeft
* .entrance-zoomInRight
* .entrance-zoomInUp


## Exit Animations
* .exit-bounceOut
* .exit-bounceOutDown
* .exit-bounceOutLeft
* .exit-bounceOutRight
* .exit-bounceOutUp
* .exit-fadeOut
* .exit-fadeOutDown
* .exit-fadeOutDownBig
* .exit-fadeOutLeft
* .exit-fadeOutLeftBig
* .exit-fadeOutRight
* .exit-fadeOutRightBig
* .exit-fadeOutUp
* .exit-fadeOutUpBig
* .exit-flipOutX
* .exit-flipOutY
* .exit-lightSpeedOut
* .exit-rotateOut
* .exit-rotateOutDownLeft
* .exit-rotateOutDownRight
* .exit-rotateOutOutUpLeft
* .exit-rotateOutUpRight
* .exit-rotateOutUpRight
* .exit-slideOutDown
* .exit-slideOutLeft
* .exit-slideOutRight
* .exit-slideOutUp
* .exit-hinge
* .exit-rollOut
* .exit-zoomOut
* .exit-zoomOutDown
* .exit-zoomOut
* .exit-zoomOutLeft
* .exit-zoomOutRight
* .exit-zoomOutUp


