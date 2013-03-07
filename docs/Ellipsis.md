## Ellipsis

The `overflow` property is augmented with a "ellipsis" value, expanding to what you see below.

`overflow` のプロパティは"ellipsis"を引数に指定された場合、以下のように出力します。


```stylus
.description {
  overflow: ellipsis;
}
```

yielding:

結果:

```css
button {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```
