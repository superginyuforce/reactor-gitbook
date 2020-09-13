---
description: 'Stroking a continuous curve, made up of cubic polynomials'
---

# Cubic Splines

Connect a sequence of points using cubic polynomials

![](../../.gitbook/assets/2dedab.png)

### Brush Method <a id="overview"></a>

**`paintCubicSplines(layer, points, tension = 0.2, closed?)`**‌

{% hint style="info" %}
While you can achieve something similar by manually painting a sequence of line segments, the splines method flattens the all splines into a _single_ array of points, which the brush paints in a single stroke.
{% endhint %}

### ‌Parameters‌‌ <a id="parameters"></a>

1. **points** - sequence of points to stroke
2. **tension** - 0.0 tension means maximum curvaceousness. 1.0 means completely rigid
3. **closed** - if `true`, the last point will be connected to the first point

| Name | Type/s | Example/s |
| :--- | :--- | :--- |
| points | `Array<Vector|Array|Object>` | `[new Vector(x, y)]`, `[[x, y]]`, `[{x, y}]` |
| tension | `float?` | `0`, `0.2`, `1.0` |
| closed | `boolean?` | `true`, `null` |

### Example

#### Paint a horizontal zigzag

```javascript
const n = 4
const dx = layer.width / n
const points = []

// create sequence of endpoints from left to right,
// alternating from top to bottom....
for (let i = 0; i < n + 1; i++) {
    points.push({
        x: i * dx, 
        y: (i % 2) * layer.height
    })
}

brush.paintCubicSplines(layer, points)
```

