## Ellipsis

The `overflow` property is augmented with a "ellipsis" value, expanding to what you see below.

```stylus
.description {
  overflow: ellipsis;
}
```

yielding:

```css
button {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```
