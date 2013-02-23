Nibは[Stylus](http://learnboost.github.com/stylus/)のためのシンプルかつパワフルなライブラリです。
クロスブラウザ対応のための強力なCSSミックスインを提供し、あなたのデザイナーライフをより良いものとします。

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
