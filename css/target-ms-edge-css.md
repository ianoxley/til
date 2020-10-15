# Targeting Microsoft Edge Only via CSS

``` css
_:-ms-lang(x),
_:-webkit-full-screen,
.selector {
  property: value;
}

```

It works because:

> if one selector is invalid, the whole rule group gets ignored
-- see
[https://stackoverflow.com/questions/32201586/how-to-identify-microsoft-edge-browser-via-css#comment98113535_45589031](https://stackoverflow.com/questions/32201586/how-to-identify-microsoft-edge-browser-via-css#comment98113535_45589031)

Only Microsoft Edge understands the first 2 selectors, so the CSS only getes
applied to the `.selector` element in Microsoft Edge.
