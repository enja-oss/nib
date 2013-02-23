## グラデーション

nibのグラデーションサポートは、nibの中でも最も大きな機能です。
あなたが普段書くCSSの構文にとても似通っていることに留まらず、
もっと寛容で、ベンダー接頭辞への対応もするどころか、さらに[node-canvas](http://github.com/learnboost/node-canvas)を使用し古いブラウザ向けにPNGまでも生成してくれます。

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

任意の数のcoler-stopを扱えます。

````
body {
  background: linear-gradient(bottom left, white, red, blue, black);
}
````

単位は色の前と後、どちらにつけても構いません。

````
body {
  background: linear-gradient(left, 80% red, #000);
  background: linear-gradient(top, #eee, 90% white, 10% black);
}
````
