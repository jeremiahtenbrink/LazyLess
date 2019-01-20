# Lazy Animations
A big thank you goes out to [Animate.css](https://github.com/daneden/animate.css "Animate.css Github") for the start of all of these animations. 
Another thank you to [eltonmesquita](https://github.com/daneden/animate.css) for the updated keyframes.

Lazy Animationsis a less wrapper around the Animate.css library. Providing lazy loading and other tools from less to the animate.css library. Just include less-animate.less into your project and copy over all the source files.

## Usage

To use Lazy Animations in your project. Simply add a import for less-animate.less into your less files and when the less compiler runs the compiler will only load the required keyframs and mixins that you are using. All the others will not be included keeping your css files slim while still providing lots of functionality. 

```css  
@import 'less-animate.less';
```

Then in your css use the animations by calling the mixins. 

```css
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
I have separated the mixins into 4 main categories so its easy to find the animation you are looking for via intellisense. 

.entrance-MIXIN-NAME
.exit-MIXIN-NAME
.attention-MIXIN-NAME
.aesthetic-MIXIN-NAME
.button-MIXIN-NAME

# Mixins currently available

## Button Mixins
* .button-mixni (@color: black, @bg-color: @button-success, @border-radius: @button-border-radius)
* .button-scaleOutOnHover (@bg-color: @button-success, @border-radius: @button-border-radius)

## Aesthetic Mixins
* .aesthetic-shadow-inset-center (@color: black, @blur: 32px, @width: 9px, @opacity: .5, @x-offset: 0, @y-offset: 0) 
* .aesthetic-shadow-inset-top (@color: black, @blur: 14px, @width: -3px, @opacity: .5, @x-offset: 0, @y-offset: 6px) 
* .aesthetic-shadow-inset-right (@color: black, @blur: 14px, @width: -3px, @opacity: .5, @x-offset: -6px, @y-offset: 0)
* .aesthetic-shadow-inset-bottom (@color: black, @blur: 14px, @width: -3px, @opacity: .5, @x-offset: 0, @y-offset: -6px)
* .aesthetic-shadow-inset-left (@color: black, @blur: 14px, @width: -3px, @opacity: .5, @x-offset: 6px, @y-offset: 0 )
* .aesthetic-shadow-inset-left-right (@color: black, @blur: 14px, @width: -3px, @opacity: .5, @x-offset: -6px, @y-offset: 0 )
* .aesthetic-shadow-inset-top-bottom (@color: black, @blur: 14px, @width: -3px, @opacity: .5, @x-offset: 0, @y-offset: -6px ) 
* .aesthetic-box-shadow (@color: black, @blur: 20px, @width: 2px,  @opacity: .5, @x-offset: @default-box-shadow-offsetX, @y-offset: @default-box-shadow-offsetY) 

## Attention Mixins 
* .attention-bounce (@duration: @defaultDuration)
* .attention-flash (@duration: @defaultDuration)
* .attention-head-shake (@duration: @defaultDuration)
* .attention-hear-beat (@duration: @defaultDuration)
* .attention-jello (@duration: @defaultDuration)
* .attention-pulse (@duration: @defaultDuration)
* .attention-rubber-band (@duration: @defaultDuration)
* .attention-shake (@duration: @defaultDuration)
* .attention-swing (@duration: @defaultDuration)
* .attention-tada (@duration: @defaultDuration)
* .attention-wobble (@duration: @defaultDuration)
* .attention-flip (@duration: @defaultDuration)

## Entrance Mixins
* .entrance-bounceIn (@duration: @defaultDuration)
* .entrance-bounceInDown (@duration: @defaultDuration)
* .entrance-bounceInLeft (@duration: @defaultDuration)
* .entrance-bounceInRight (@duration: @defaultDuration)
* .entrance-bounceInUp (@duration: @defaultDuration)
* .entrance-fadeInLeft (@duration: @defaultDuration)
* .entrance-fadeInLeftBig (@duration: @defaultDuration)
* .entrance-fadeIn (@duration: @defaultDuration)
* .entrance-fadeInDown (@duration: @defaultDuration)
* .entrance-fadeInDownBig (@duration: @defaultDuration)
* .entrance-fadeInRight (@duration: @defaultDuration)
* .entrance-fadeInRightBig (@duration: @defaultDuration)
* .entrance-fadeInUp (@duration: @defaultDuration)
* .entrance-fadeInUpBig (@duration: @defaultDuration)
* .entrance-flipInX (@duration: @defaultDuration)
* .entrance-flipInY (@duration: @defaultDuration)
* .entrance-lightSpeedIn (@duration: @defaultDuration)
* .entrance-rotateIn (@duration: @defaultDuration)
* .entrance-rotateInDownLeft (@duration: @defaultDuration)
* .entrance-rotateInDownRight (@duration: @defaultDuration)
* .entrance-rotateInUpLeft (@duration: @defaultDuration)
* .entrance-rotateInUpRight (@duration: @defaultDuration)
* .entrance-slideInDown (@duration: @defaultDuration)
* .entrance-slideInLeft (@duration: @defaultDuration)
* .entrance-slideInRight (@duration: @defaultDuration)
* .entrance-slideInUp (@duration: @defaultDuration)
* .entrance-jackInTheBox (@duration: @defaultDuration)
* .entrance-rollIn (@duration: @defaultDuration)
* .entrance-zoomIn (@duration: @defaultDuration)
* .entrance-zoomInDown (@duration: @defaultDuration)
* .entrance-zoomInLeft (@duration: @defaultDuration)
* .entrance-zoomInRight (@duration: @defaultDuration)
* .entrance-zoomInUp (@duration: @defaultDuration)


## Exit Mixins
* .exit-bounceOut (@duration: @defaultDuration)
* .exit-bounceOutDown (@duration: @defaultDuration)
* .exit-bounceOutLeft (@duration: @defaultDuration)
* .exit-bounceOutRight (@duration: @defaultDuration)
* .exit-bounceOutUp (@duration: @defaultDuration)
* .exit-fadeOut (@duration: @defaultDuration)
* .exit-fadeOutDown (@duration: @defaultDuration)
* .exit-fadeOutDownBig (@duration: @defaultDuration)
* .exit-fadeOutLeft (@duration: @defaultDuration)
* .exit-fadeOutLeftBig (@duration: @defaultDuration)
* .exit-fadeOutRight (@duration: @defaultDuration)
* .exit-fadeOutRightBig (@duration: @defaultDuration)
* .exit-fadeOutUp (@duration: @defaultDuration)
* .exit-fadeOutUpBig (@duration: @defaultDuration)
* .exit-flipOutX (@duration: @defaultDuration)
* .exit-flipOutY (@duration: @defaultDuration)
* .exit-lightSpeedOut (@duration: @defaultDuration)
* .exit-rotateOut (@duration: @defaultDuration)
* .exit-rotateOutDownLeft (@duration: @defaultDuration)
* .exit-rotateOutDownRight (@duration: @defaultDuration)
* .exit-rotateOutOutUpLeft (@duration: @defaultDuration)
* .exit-rotateOutUpRight (@duration: @defaultDuration)
* .exit-rotateOutUpRight (@duration: @defaultDuration)
* .exit-slideOutDown (@duration: @defaultDuration)
* .exit-slideOutLeft (@duration: @defaultDuration)
* .exit-slideOutRight (@duration: @defaultDuration)
* .exit-slideOutUp (@duration: @defaultDuration)
* .exit-hinge (@duration: @defaultDuration)
* .exit-rollOut (@duration: @defaultDuration)
* .exit-zoomOut (@duration: @defaultDuration)
* .exit-zoomOutDown (@duration: @defaultDuration)
* .exit-zoomOut (@duration: @defaultDuration)
* .exit-zoomOutLeft (@duration: @defaultDuration)
* .exit-zoomOutRight (@duration: @defaultDuration)
* .exit-zoomOutUp (@duration: @defaultDuration)

## Documentation. 

## Default Variables
All default variables are located in base.less in the source folder. They can be overridden in your less files as long as 
your less files come after the @import 'less-animate.less'; 
### @defaultDuration: 1s;
### @default-box-shadow-offsetX: 0;
### @default-box-shadow-offsetY: 0;
### @button-success: lightgreen;   Light green color.
### @button-danger: #f59090;  Light red color.
### @button-info: #537ee8;   Light blue color.

### .animation-infinite ();
#### This sets the animation to run continuously.

### .animation-delay(@duration : 1s);
#### This mixin will take one argument the delay duration. Either in s or ms. Must include the s or the ms after the number. Or leave blank for the default 1s delay. 





