## Clearfix

The clearfix mixin currently takes no arguments, so it may be called as shown below:

Clearfixのミックスインは今のところ引数がありませんので、以下のように利用できます。

```stylus
.clearfix {
  clearfix();
}
```

yielding:

結果:

```css
.clearfix {
  zoom: 1;
}
.clearfix:before,
.clearfix:after {
  content: "";
  display: table;
}
.clearfix:after {
  clear: both;
}
```
