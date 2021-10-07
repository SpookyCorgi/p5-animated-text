# p5-animated-text

A library that add text animation to the p5.js

Current animations. More to come!

| slideInLeft  | slideInRight  | slideInUp  | slideInLeft  |
| ------------ | ------------- | ---------- | ------------ |
|              |               |            |              |
| slideOutLeft | slideOutRight | slideOutUp | slideOutLeft |
|              |               |            |              |
| zoomIn       | zoomOut       | rotateIn   | rotateOut    |
|              |               |            |              |

# How to use it?

First initialize the object somewhere

```javascript
let t = new AnimatedText(string, x1, y1, color, animationType, [length], [autostart])
```

- string : the word that you want to show, in a string format like "hello there"
- x1, y1 : the bottom left position of the text
- color : the color of the text, must be a p5 color object such as color(0), color('#ff0000') etc.
- animationType : the type of animation you want to use, also in a string format like "slideInLeft", you can see the full list on the top of the page
- length : the total time of the animation, default is 1000(millisecond)
- autostart : (optional parameter), by default the animation will start the moment you initialize the object, enter false if you don't want to

Then put this line in the p5 draw function whenever you want to draw it

```javascript
t.render()
```

Whenever you want to start the animation again call. Remember don't put this in a loop unintentionally or it will keeps restarting.

```javascript
t.start()
```

For changing the text

```javascript
t.setText("Your new text!")
```

For changing the animation

```javascript
t.setAnimation("enter animation name here")
```

# Important stuff

This library is build to be compatible with p5 as much as possible so normally all functions like textSize(), rotate(), scale() etc will effect the animation text except fill() since we are passing the color manually.

At this moment the animation text don't support the x2, y2 parameters that you can find in the p5 library text function.

The library also don't really works with multiline text since it can't detect the total height of it.

# How to add it to your project?

### Own project

Download the animatedText.js file and put it in your desire folder.

Link the animatedText.js file **after** the p5.js script tags

```html
<!--p5.js-->
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/p5.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/addons/p5.sound.min.js"></script>
<!--enter this line-->
<script src="location of the animatedText.js file"></script>
```

### p5 editor

Download the animatedText.js file. Open up your p5 editor project. Click the arrow next to sketch.js

![](./assets/p5-guide-1.png)

Click the down arrow and upload the animatedText.js file

![](./assets/p5-guide-2.png)

Go to the index.html file and enter the script tag of the animatedText.js file after the p5.js tags

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/p5.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/addons/p5.sound.min.js"></script>
<!--enter this line-->
<script src="animatedText.js"></script>
```

