---
description: Stroke the outline of font glyphs
---

# Font Glyphs

Trace an SVG path, i.e. the "d" value of a `<path d="M....">` SVG element.

![](../../.gitbook/assets/screenshot-from-2020-09-11-11-05-28.png)

### Brush Method <a id="overview"></a>

**`brush.paintGlyphs(layer, text, fontName, fontSize, center)`**

### ‌Parameters‌

1. **text** - One or more characters \(font glyphs\) to stroke
2. **fontName** - Base file name of a font file contained in the top-level `fonts` directory
3. **fontSize** - Size of the font in pixels, which corresponds to the font height.
4. **center** - center position at which the path is drawn

| Name | Type/s | Examples |
| :--- | :--- | :--- |
| text | `string` | `"quantum"`, `"浮"`  |
| fontName | `string` | `"umeboshi"` |
| fontSize | `integer` | `22`, `50` |
| center | `Vector`, `Array`, `Object` | `[new Vector(x, y)]`, `[[x, y]]`, `[{x, y}]` |

{% hint style="info" %}
Reactor is aware of path text files located in `svg/paths` directory. If you have a path file called "foo", then you'll be able to load this file at runtime via `reactor.svgManager.getPath("foo")`.
{% endhint %}

### Example

#### Paint an Array of Points

```javascript
const reactor = Reactor.getInstance()
const text = "spam"
const center = layer.center
const fontName = "barlow-light"
const fontSize = 64

brush.paintGlyphs(layer, text, fontName, fontSize, center)
```

