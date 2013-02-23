## インストール

nibを始めるにあたって、まず nibとstylusを一緒に _package.json_ ファイルに追加します。
インストールが完了したら、[Connect](http://senchalabs.github.com/connect)や[Express](http://expressjs.com/)アプリケーションで、
下に紹介するスニペットを使いstylusとnibを利用できます。
Stylusがnibを使うために必要なことは、ただ `.use(nib())` を呼び出すことです。

````
var connect = require('connect')
  , stylus = require('stylus')
  , nib = require('nib');

var app = connect();

function compile(str, path) {
  return stylus(str)
    .set('filename', path)
    .set('compress', true)
    .use(nib());
}

app.use(stylus.middleware({
    src: __dirname
  , compile: compile
}));

app.listen(3000);
````
_.styl_ ファイルからnibを利用するには、 **@import** でnibもしくはnibの一部を指定します。

````
@import 'nib'
@import 'nib/gradients'
@import 'nib/buttons'
````

stylusソースに手入力でnibを **@import** する方法だけではなく、JavaScript APIを使いインポートするという方法もあります。

````
return stylus(str)
  .set('filename', path)
  .set('compress', true)
  .use(nib())
  .import('nib');
````
