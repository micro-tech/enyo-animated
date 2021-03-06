# Enyo-Animated: animated Controls for the Enyo framework

These Controls are designed to
* help the user mentally model the application UI
* not make the user wait
* animate at 60 fps on modern mobile & desktop devices
* be easy for developers to incorporate in apps
* work with Onyx, Mochi or Moonstone widgets (the default styling is usually Onyx).

They are not designed to be showy.  Fallbacks for older browsers have not yet been added.

They are designed around the properties that GPUs can readily animate:
* position: transform: translate(x,y)
* scale: transform: scale(n)
* rotation: transform: rotate(n)
* opacity: opacity: 0..1


## References

[Animation for Attention and Comprehension](http://www.nngroup.com/articles/animation-usability/)

[Motion & Meaning podcast, episode 3](http://motionandmeaning.io/episode03.html)

[High Performance Animations](http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/)

[Cubic-Bezier design tool](http://cubic-bezier.com/)


## Using

1. Clone this repo to a directory in the lib directory of an Enyo app (alongside layout).
2. To source/package.js, add the line `"$lib/enyo-animated",`
3. Add one or more of the Controls to your app.


## animated.Toast

A toast, which moves like a CD tray in a straight line.
Set the `locationV` property to `top`, `middle` or `bottom`.
Set the `locationH` property to `left`, `middle` or `right`.
It is not modal.
Show and hide it with the usual `.show()`, `.hide()` and `.set('showing', boolean)`.

Corner toasts are sized to contain their content, unless you style their height or width.

Top and bottom edge toasts are as wide as their parent, by default.
If you set a width, they are centered.

Left and right edge toasts are as tall as their parent, by default.  
If you set a height, they are centered.

Default styling is white text on a dark background.


## animated.ToastCurve

A toast, which moves on a curved path, as if mounted on a mechanical linkage, actuated by servo motors.
Set the `locationV` property to `top`, `middle` or `bottom`.
Set the `locationH` property to `left`, `middle` or `right`.
It is not modal.
Show and hide it with the usual `.show()`, `.hide()` and `.set('showing', boolean)`.

By default, it's sized to contain its children.
Corner toasts don't require a width or height in their style property. 
Top middle and bottom middle toasts will be full width, unless you set a width.
You must set a height for left middle and right middle toasts.
 
Default styling is white text on a dark background.


## Unwritten widgets

Feel free to implement and contribute these.

### Expand-from-control-popup

This Control would expand from a visible control, and contract back into it, like a Menu and its button.


## Other Enyo controls that are animated

Not all of these are optimized to animate smoothly.

* [SvgSpinner](https://github.com/infusionsoft/enyo-svg-spinner) (SVG animation)
* [moon.Spinner](http://enyojs.com/docs/latest/index.html#/kind/moon.Spinner) (CSS keyframe animation)
* [enyo.Panels](http://enyojs.com/docs/latest/developer-guide/building-apps/layout/panels.html) 
and its descendants such as enyo.ImageCarousel
* trees using [enyo.Node](http://enyojs.com/docs/latest/index.html#/kind/enyo.Node)
* [enyo.Slidable](http://enyojs.com/docs/latest/index.html#/kind/enyo.Slideable) can be configured as toast.
* [enyo.PulldownList](http://enyojs.com/docs/latest/index.html#/kind/enyo.PulldownList)


## How to contribute

* Develop on a git branch or fork.
* Submit changes as a GitHub pull request to the master branch, that merges cleanly and doesn't break any tests (enyo-animated/test/SpecRunner.html) when running in current versions of Firefox or Chrome.
* Include the following line in the pull request comments, substituting your real name and email address, 
to assert your compliance with [Open webOS Developer Grant and Certificate of Origin 1.0](http://www.openwebosproject.org/community/governance/dco/)
 
	Open-WebOS-DCO-1.0-Signed-Off-By: Joe Smith <joe@myco.com>


## Copyright and License Information

("The MIT License (MIT)")

Copyright © 2015 Hominid Software

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
