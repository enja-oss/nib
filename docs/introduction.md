Nib is a small and powerful library for [the Stylus CSS language](http://learnboost.github.com/stylus/), 
providing robust cross-browser CSS3 mixins to make your life as a designer easier.

````  
body {
  background: linear-gradient(top, white, black);
}
````

````
body {
  background: -webkit-gradient(linear,
    left top,
    left bottom,
    color-stop(0, #fff),
    color-stop(1, #000));
  background: -webkit-linear-gradient(top, #fff 0%, #000 100%);
  background: -moz-linear-gradient(top, #fff 0%, #000 100%);
  background: linear-gradient(top, #fff 0%, #000 100%);
}
````
