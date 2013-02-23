## ポジションミックスイン

`absolute`、 `fixed`、 `relative` ポジションミックスインはそれぞれ、異なる3つののCSSプロパティへ展開される短縮記法を提供します。
構文は次の通りです。

````
fixed|absolute|relative: top|bottom [n] left|right [n]
````

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

また、単位も指定することもできます。

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
