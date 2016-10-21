# blurLoad
##jQuery plugin for loading images/background images Medium style.

Small image thumbnail is drawn on to the canvas and added blur, if the image comes in the viewport, full image is loaded. After loading full image, loaded class is added to the element, which can be used to hide the canvas and show full image via css.

> Used Stack blur algorithm https://github.com/flozz/StackBlur for blurring the canvas.

- For loading image as <img> tag
``` HTML
  <div class="blur-load" >
        <img class="bg-small" data-url="big-image.jpg" src="small-image.jpg">
        <canvas class="bg-blur"></canvas>
  </div>
```

- For loading image as background-image
``` HTML
    <div class="blur-load">
        <span class="bg-small" data-url="big-image.jpg" style="background-image: url('small-image.jpg')"></span>
        <div class="bg-lg"></div>
        <canvas class="bg-blur"></canvas>
    </div>
```

- Call the script on Dom Ready
```javascript
  $('.blur load').blurLoad(blur);
```
If you dont pass the blur value, default value will be 50
