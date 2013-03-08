## Clearfix

Clearfixのミックスインは今のところ引数がありませんので、以下のように利用できます。

```stylus
.clearfix {
  clearfix();
}
```

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
