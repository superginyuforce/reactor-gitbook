---
description: Painting individual points
---

# Points

Dab the brush at a specific location.

![](../../.gitbook/assets/6167ae.png)

### Brush Method <a id="overview"></a>

**`brush.paintPoint(layer, point)`**

{% hint style="warning" %}
If you have a large set of points, use the`paintPoints` method. See: [Arrays of Points](arrays-of-points.md) 
{% endhint %}

### ‌Parameters‌

1. **point** - point at which the brushstroke is drawn

| Name | Type/s | Examples |
| :--- | :--- | :--- |
| point | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |

### Example

#### Paint a grid of off-center points

```javascript
class PointExample extends Design {
    async draw(layer) {
        let brush = new PolygonBrush()
        let colors = this.random.colors(2)

        brush.density = 1
        brush.radius = 0.015
        brush.tip.fill.color = this.random.colors(2, 10)
        brush.tip.scattering.x = {min: 0, max: 0.025}
        brush.tip.scattering.y = {min: 0, max: 0.025}
        brush.tip.angle = (i, j, n, m) => 2 * PI * sin(2 * PI * (i/n))
        brush.tip.stroke.width = this.random.real(0.002, 0.003)
        brush.tip.stroke.alpha = 0.5
        brush.tip.fill.color = (i) => colors[i % colors.length]
        brush.tip.fill.alpha = {min: 0.75, max: 1.0}
        
        let n = 15
        let dx = layer.width / n
        let dy = layer.height * 0.4
        
        let n = Math.round(layer.height / (layer.height * brush.radius))
        let m = Math.round(layer.width / (layer.width * brush.radius))
        let dx = layer.width / m
        let dy = layer.height / n
        
        for (let i = 4; i < n; i += 4) {
          for (let j = 4; j < m; j += 4) {
            brush.angle = this.random.radians()
            brush.paintPoint(layer, { x: j * dx, y: i * dy })
          }
        }
    }
}
```

![Example Output](../../.gitbook/assets/af62a3.png)



