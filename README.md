#Less Animate.css
A big thanks goes out to Animate.css for the start of all of these animations. 

# Animate.css [![GitHub release](https://img.shields.io/github/release/daneden/animate.css.svg)](https://github.com/daneden/animate.css/releases) [![CDNJS](https://img.shields.io/cdnjs/v/animate.css.svg)](https://cdnjs.com/libraries/animate.css) [![Build Status](https://travis-ci.com/daneden/animate.css.svg?branch=master)](https://travis-ci.com/daneden/animate.css) [![devDependencies Status](https://david-dm.org/daneden/animate.css/dev-status.svg)](https://david-dm.org/daneden/animate.css?type=dev) [![chat](https://img.shields.io/badge/chat-gitter-green.svg)](https://gitter.im/animate-css/Lobby) [![npm version](https://badge.fury.io/js/animate.css.svg)](https://www.npmjs.com/package/animate.css)

Less-imate is a less wrapper around the Animate.css library. Providing lazy loading and other tools from less to the animate.css library. Just include less-animate.less into your project and copy over all the source files.

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







[Check out all the animations here!](https://daneden.github.io/animate.css/)

It's possible to change the duration of your animations, add a delay or change the number of times that it plays:

```css
.yourElement {
  animation-duration: 3s;
  animation-delay: 2s;
  animation-iteration-count: infinite;
}
```

## Usage with Javascript

You can do a whole bunch of other stuff with animate.css when you combine it with Javascript. A simple example:

```javascript
const element =  document.querySelector('.my-element')
element.classList.add('animated', 'bounceOutLeft')
```

You can also detect when an animation ends:

```javascript
const element =  document.querySelector('.my-element')
element.classList.add('animated', 'bounceOutLeft')

element.addEventListener('animationend', function() { doSomething() })
```

You can use this simple function to add and remove the animations:

```javascript
function animateCss(element, animationName, callback) {
    const node = document.querySelector(element)
    node.classList.add('animated', animationName)

    function handleAnimationEnd() {
        node.classList.remove('animated', animationName)
        node.removeEventListener('animationend', handleAnimationEnd)

        if (typeof callback === 'function') callback()
    }

    node.addEventListener('animationend', handleAnimationEnd)
}
```

And use it like this:

```javascript
animateCSS('.my-element', 'bounce')

// or
animateCSS('.my-element', 'bounce', function() {
  // Do something after animation
})
```

Notice that the examples are using ES6's `const` declaration, dropping support for IE10 and some aging browsers. If you prefer, switch the `const` to `var` declarations and IE10 and some old browsers will get support (they still have to provide [classList](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList) support, so do your [research](https://caniuse.com/#feat=classlist)).

## Setting _Delay_ and _Speed_

### Delay Class

It's possible to add delays directly on the element's class attribute, just like this:

```html
<div class="animated bounce delay-2s">Example</div>
```

| Class Name | Delay Time |
| ---------- | ---------- |
| `delay-2s` | `2s`       |
| `delay-3s` | `3s`       |
| `delay-4s` | `4s`       |
| `delay-5s` | `5s`       |

> _**Note**: The default delays are from 1 second to 5 seconds only. If you need custom delays, add it directly to your own CSS code._

### Slow, Slower, Fast, and Faster Class

It's possible to control the speed of the animation by adding these classes, as a sample below:

```html
<div class="animated bounce faster">Example</div>
```

| Class Name | Speed Time |
| ---------- | ---------- |
| `slow`     | `2s`       |
| `slower`   | `3s`       |
| `fast`     | `800ms`    |
| `faster`   | `500ms`    |

> _**Note**: The `animated` class has a default speed of `1s`. If you need custom duration, add it directly to your own CSS code._

## Custom Builds

Animate.css is powered by [gulp.js](http://gulpjs.com/), which means you can create custom builds pretty easily. First of all, you’ll need Gulp and all other dependencies:

```sh
$ cd path/to/animate.css/
$ sudo npm install
```

Next, run `gulp` to compile your custom builds. For example, if you want only some of the “attention seekers”, simply edit the `animate-config.json` file to select only the animations you want to use.

```javascript
"attention_seekers": {
  "bounce": true,
  "flash": false,
  "pulse": false,
  "shake": true,
  "headShake": true,
  "swing": true,
  "tada": true,
  "wobble": true,
  "jello":true
}
```

## Accessibility

Animate.css supports the [`prefers-reduced-motion` media query](https://webkit.org/blog/7551/responsive-design-for-motion/) so that users with motion sensitivity can opt out of animations. On supported platforms (currently only OSX Safari and iOS Safari), users can select "reduce motion" on their operating system preferences and it will turn off CSS transitions for them without any further work required.

## License

Animate.css is licensed under the MIT license. (http://opensource.org/licenses/MIT)

## Contributing

Pull requests are the way to go here. We only have two rules for submitting a pull request: match the naming convention (camelCase, categorised [fades, bounces, etc]) and let us see a demo of submitted animations in a [pen](http://codepen.io). That **last one is important**.
