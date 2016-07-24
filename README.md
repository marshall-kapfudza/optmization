## Website Performance Optimization portfolio project
My approatch to archive `93/100` on desktop and `95/100` on mobile
### How to run
To get started, download the entire directory, and open it in a browser locally. You can also open the directory using terminal and and run the following command if you are using a mac `python -m SimpleHTTPServer 8080` then open your browser and type in `http://localhost:8080`

#### Part 1: Optimize PageSpeed Insights score for index.html

##### _CSS_ _files_
First I opened my print.css and style.css and compine both on the online css minify [http://csscompressor.com/](http://csscompressor.com/) then load my script using js function as below
`
var cb=function(){var e=document.createElement("link");e.rel="stylesheet";e.href="css/style.min.css";var t=document.getElementsByTagName("head")[0];t.parentNode.insertBefore(e,t)};var raf=requestAnimationFrame||mozRequestAnimationFrame||webkitRequestAnimationFrame||msRequestAnimationFrame;if(raf)raf(cb);else window.addEventListener("load",cb)
`

##### _js_ _files_
I use the same approach as above, I minify all my js files online [http://jscompress.com/](http://jscompress.com/) and load it on the page using asynchronus html atrribute  ``async``
```bash
<script src="js/perfmaters.min.js" async></script>
```

##### Images
I openned up my images ``(pizzeria.jpg)`` and resized it using ``photoshop`` and optimize it again using ``image optim``.

#### Part 2: Getting Rid of Jank
Before I minify my code as above I jump into the code, on ``css file`` I add some css property on mover class ``transform: translateZ(0);`` then compine my css files and minify them and also load them using my ``js`` as above.

Unnecessary JS operations were pulled out of `for` loops where possible, in `views/js/main.js` and scroll events were 'debounced' to decouple the animations and only repainted when needed

### Resources
- [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)
- [Optimize CSS Delivery](https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery)
- [README.md](http://dillinger.io/)

