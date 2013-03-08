## Border radius

Nibの `border-radius` は通常の構文に加えて、値をもっと分かりやすくする拡張構文もサポートしています。

```stylus
button {
  border-radius: 1px 2px / 3px 4px;
}

button {
  border-radius: 5px;
}

button {
  border-radius: bottom 10px;
}
```

結果:

```css
button {
  -webkit-border-radius: 1px 2px/3px 4px;
  -moz-border-radius: 1px 2px/3px 4px;
  border-radius: 1px 2px/3px 4px;
}
button {
  -webkit-border-radius: 5px;
  -moz-border-radius: 5px;
  border-radius: 5px;
}
button {
  -moz-border-radius-topleft: 10px;
  -webkit-border-top-left-radius: 10px;
  border-top-left-radius: 10px;
  -moz-border-radius-bottomright: 10px;
  -webkit-border-bottom-right-radius: 10px;
  border-bottom-right-radius: 10px;
}
```
