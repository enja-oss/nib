## Gradients

Nib's gradient support is by far the largest feature it provides, 
not only is the syntax extremely similar to what you would normally write, 
it's more forgiving, expands to vendor equivalents, 
and can even produce a PNG for older browsers with [node-canvas](http://github.com/learnboost/node-canvas).

````
body {
  background: linear-gradient(top, white, black);
}
````

yields:

````
body {
  background: -webkit-gradient(linear, left top, left bottom, color-stop(0, #fff), color-stop(1, #000));
  background: -webkit-linear-gradient(top, #fff 0%, #000 100%);
  background: -moz-linear-gradient(top, #fff 0%, #000 100%);
  background: linear-gradient(top, #fff 0%, #000 100%);
}
````

Any number of color stops may be provided:

````
body {
  background: linear-gradient(bottom left, white, red, blue, black);
}
````

Units may be placed before, or after the color:

````
body {
  background: linear-gradient(left, 80% red, #000);
  background: linear-gradient(top, #eee, 90% white, 10% black);
}
````
