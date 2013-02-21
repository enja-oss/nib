## インストール

To get started you'll first want to add nib to your _package.json_ file, along with stylus. 
Once installed you can use Stylus and Nib with your [Connect](http://senchalabs.github.com/connect) or [Express](http://expressjs.com/) application as shown in the following snippet. 
The simple `.use(nib())' call is all that is required to expose itself to Stylus

まず始めるに当たって、nibとstylusを一緒に _package.json_　ファイルに追加したくなるかもしれません。
しかし、あなたの[Connect](http://senchalabs.github.com/connect)や[Express](http://expressjs.com/)アプリケーションに、
下のスニペットコードを追加する事で、Stylusとnibを使用することができます。
Stylusがnibを使うために必要なことは、ただシンプルに `.use(nib())` を呼び出すことがすべてです。

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

From within a .styl file you can then **@import** nib, or a portion of nib:

_.styl_ ファイル内部からは **@import** でnibかnibの場所を指定することで使用することができます。

````
@import 'nib'
@import 'nib/gradients'
@import 'nib/buttons'
````

Rather than manually **@import** -ing nib within your Stylus source you can import it via the JavaScript API as well:

そうではなく、手動でStylusの中にnibを **@import** したい場合は、JavaScript APIと同様にインポートすることでこれを実現できます。

````
return stylus(str)
  .set('filename', path)
  .set('compress', true)
  .use(nib())
  .import('nib');
````
