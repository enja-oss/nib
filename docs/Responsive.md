## Responsive

The `image` mixin allows you to define a `background-image` for both the normal image, and a doubled image for devices with a higher pixel ratio such as retina displays. This works by using a @media query to serve an "@2x" version of the file.

`image` ミックスインは、通常の画像と、Retinaディスプレイのような高解像度のデバイス向けの倍角画像の両方を `background-image` に定義できます。このミックスインは、画像ファイルの "@2x" バージョンを提供するために、メディアクエリーを利用します。

```stylus
#logo {
  image: '/images/branding/logo.main.png'
}

#logo {
  image: '/images/branding/logo.main.png' 50px 100px
}
```

yields:

結果:

```css
#logo {
  background-image: url("/images/branding/logo.main.png");
}
@media all and (-webkit-min-device-pixel-ratio: 1.5) {
  #logo {
    background-image: url("/images/branding/logo.main@2x.png");
    background-size: auto auto;
  }
}
#logo {
  background-image: url("/images/branding/logo.main.png");
}
@media all and (-webkit-min-device-pixel-ratio: 1.5) {
  #logo {
    background-image: url("/images/branding/logo.main@2x.png");
    background-size: 50px 100px;
  }
}
```
