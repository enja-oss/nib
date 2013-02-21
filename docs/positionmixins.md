## ポジションミックスイン

The position mixins `absolute`, `fixed`, and `relative` provide a shorthand variant to what is otherwise three CSS properties. The syntax is as follows:

`absolute`、 `fixed`、 `relative` ポジションミックスインは、それぞれに異なる3つのCSSプロパティへ展開される短縮記法を提供します。
構文は次の通りです。

````
fixed|absolute|relative: top|bottom [n] left|right [n]
````

The following example will default to (0,0):

次の例では、デフォルトの(0,0)が出力されます。

````      
#back-to-top {
  fixed: bottom right;
}
````

結果:

````
#back-to-top {
  position: fixed;
  bottom: 0;
  right: 0;
}
````

You may also specify the units:

また、単位を指定することもできます。

````
#back-to-top {
  fixed: bottom 10px right 5px;
}
````

結果:
      
````
#back-to-top {
  position: fixed;
  bottom: 10px;
  right: 5px;
}
````    
