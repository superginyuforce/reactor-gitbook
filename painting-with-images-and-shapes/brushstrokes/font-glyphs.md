---
description: Stroke the outline of font glyphs
---

# Font Glyphs

Stroke the outline of font glyphs.

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
Reactor auto-loads fonts in the top-level `fonts` directory. If you have a font called `my-font.ttf`, then you can reference this font by name, like `"my-font"`.
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

