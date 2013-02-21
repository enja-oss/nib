## グラデーション

Nib's gradient support is by far the largest feature it provides, 
not only is the syntax extremely similar to what you would normally write, 
it's more forgiving, expands to vendor equivalents, 
and can even produce a PNG for older browsers with [node-canvas](http://github.com/learnboost/node-canvas).

nibのグラデーションサポート機能は、nibが提供する機能の中でも最も特徴的な機能です。
それはあなたが普段書くCSS構文と非常に似通っているということだけに留まらず、
ベンダーへの対応、さらに[node-canvas](http://github.com/learnboost/node-canvas)を使用して、
古いブラウザ向けにPNGを生成することまでも気前良く提供します。

````
body {
  background: linear-gradient(top, white, black);
}
````

結果:

````
body {
  background: -webkit-gradient(linear, left top, left bottom, color-stop(0, #fff), color-stop(1, #000));
  background: -webkit-linear-gradient(top, #fff 0%, #000 100%);
  background: -moz-linear-gradient(top, #fff 0%, #000 100%);
  background: linear-gradient(top, #fff 0%, #000 100%);
}
````

Any number of color stops may be provided:

任意の数のcoler-stopを扱うことができます。

````
body {
  background: linear-gradient(bottom left, white, red, blue, black);
}
````

Units may be placed before, or after the color:

単位の場所は、色の前でも後ろでも良い。

````
body {
  background: linear-gradient(left, 80% red, #000);
  background: linear-gradient(top, #eee, 90% white, 10% black);
}
````
