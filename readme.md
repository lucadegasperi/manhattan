##What's this?
Manhattan is a highly opinionated SASS library for easing the pain of big CSS development. It has two primary purposes: Prototyping page elements by using classes to abstract the element's behaviour at different resolutions. After prototyping, generate clean and lightweight CSS by using SASS silent classes.

Use Manhattan if:
- You need css prototyping and abstractions.
- You understand/need scalability and reusable code.
- You are a confident/competent developer SASS.
Do not use Manhattan if:
- You need a framework that supplies design (Use Bootstrap for that).

##Browser Support
Manhattan is intended to work only in modern browsers. It takes advantage of normalize.css and global box-sizing:border-box;. As such, Manhattan is intended for IE8 and above only.

##What's inside
Manhattan comes with some lovely features
- Media Queries abstraction
- Spacing Units
- Percentage Widths
- Grid System
- Color Fillings
- Font Sizes
- Debug Options

Everything is easily extensible and customizable. 

##Getting started

Let's say you want to creare the header of your website. With Manhattan simply add some classes to your tag until it looks fine at different viewports.

```html
<div class="gw">
	<div class="g one-whole m-one-half pad-2 m-pad-3"></div>
</div>
```
In the example above the div will behave differently depending on the screen size, on a small screen, it will fit the whole container and have a padding of 2 units all around. When the screen gets bigger the m- classes will trigger and the padding increases to 3 units and the div will occupy only half of the container. Pretty easy, just add classes until your element behaves as you want it.
**But that's ugly!**
You're right indeed, that's where Manhattan comes to help again.
Once you finished prototyping your element it's time to make it real.
```html
<div class="gw">
	<div class="header"></div>
</div>
```
```sass
.header {
	%g;
	%one-whole;
	%pad-2;
	%m-one-half;
	%m-pad-3:
}
```
Simple and beautiful, you don't even have to worry about media queries, just tell how your element should behave and Manhattan will do the rest.


##The developer


##Credits
A lot of the code in Manhattan and its philosophy is inspired by [Harry Roberts](http://csswizardry.com "Harry Robert's Website") work on [inuit.css](https://github.com/csswizardry/inuit.css/ "inuit.css"). Thanks for your precious hard work!

##MIT Licence
Copyright (C) 2013 Luca Degasperi

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.