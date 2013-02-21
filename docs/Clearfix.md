## Clearfix

The clearfix mixin currently takes no arguments, so it may be called as shown below:

```stylus
.clearfix {
  clearfix();
}
```

yielding:
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
