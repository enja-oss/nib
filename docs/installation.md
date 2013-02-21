## Installation

To get started you'll first want to add nib to your package.
json file, along with stylus. Once installed you can use Stylus and Nib with your [Connect](http://senchalabs.github.com/connect) or [Express](http://expressjs.com/) application as shown in the following snippet. 
The simple `.use(nib())' call is all that is required to expose itself to Stylus

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

````
@import 'nib'
@import 'nib/gradients'
@import 'nib/buttons'
````

Rather than manually **@import** -ing nib within your Stylus source you can import it via the JavaScript API as well:

````
return stylus(str)
  .set('filename', path)
  .set('compress', true)
  .use(nib())
  .import('nib');
````
