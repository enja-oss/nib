## Ellipsis

`overflow` のプロパティは"ellipsis"を引数に指定された場合、以下のように出力します。


```stylus
.description {
  overflow: ellipsis;
}
```

結果:

```css
button {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```
