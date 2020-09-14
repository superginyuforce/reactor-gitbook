---
description: Paint a quadratic curve with one control point
---

# Quadratic Curves

![](../../.gitbook/assets/af753f.png)

### Brush Method

**`brush.paintQuadraticCurve(layer, start, cp, end)`**

### Parameters

* **start** - starting point of line segment
* **cp** - control point
* **end** - end point of line segment

| Name | Type/s | Examples |
| :--- | :--- | :--- |
| start | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |
| cp | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |
| end | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |

### Example

#### Paint a single quadratic curve

```javascript
class QuadraticCurveExample extends Design {
    async draw(layer) {
        let brush = new EllipseBrush()
        let colors = this.random.colors(2)
        
        brush.radius = 0.035
        brush.density = this.random.real(4, 16)
        brush.tip.eccentricity.x = 0.5
        brush.tip.angle = (i, j, n, m) => 2 * PI * sin(2 * PI * (i/n))
        brush.tip.stroke.width = this.random.real(0.002, 0.003)
        brush.tip.stroke.alpha = 0.5
        brush.tip.fill.color = (i) => colors[i % colors.length]
        brush.tip.fill.alpha = {min: 0.75, max: 1.0}
        
        let start = {x: 50, y: 50}
        let end = {x: layer.width - 50, y: layer.height - 50}
        let cp = {x: layer.center.x, y: 0}
        
        brush.paintQuadraticCurve(layer, start, cp, end)
    }
}
```

![Example Output](../../.gitbook/assets/986ee4.png)

