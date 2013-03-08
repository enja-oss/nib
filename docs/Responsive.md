## Responsive

`image` ミックスインは、通常の画像と、Retinaディスプレイのような高解像度のデバイス向けの倍角画像の両方を `background-image` に定義できます。このミックスインは、画像ファイルの "@2x" バージョンを提供するために、メディアクエリーを利用します。

```stylus
#logo {
  image: '/images/branding/logo.main.png'
}

#logo {
  image: '/images/branding/logo.main.png' 50px 100px
}
```

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
