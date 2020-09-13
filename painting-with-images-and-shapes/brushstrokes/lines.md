---
description: Painting individual line segments
---

# Lines

Stroke a straight line between start and end points.

![](../../.gitbook/assets/a02e10.png)

### Brush Method

**`brush.paintLine(layer, start, end)`**

### Parameters

* **start** - starting point of line segment
* **end** - end point of line segment

| Name | Type/s | Examples |
| :--- | :--- | :--- |
| start | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |
| end | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |

### Example

#### Paint a single line segment

```javascript
class LineExample extends Design {
    async draw(layer) {
        let brush = new PolygonBrush()
        let colors = this.random.colors(2)
        
        brush.radius = 0.035
        brush.density = 10
        brush.tip.angle = (i, j, n, m) => (2 * PI) * sin(2 * PI * (i/(n-1)))
        brush.tip.stroke.width = this.random.real(0.002, 0.003)
        brush.tip.stroke.alpha = 0.5
        brush.tip.fill.color = (i) => colors[i % colors.length]
        brush.tip.fill.alpha = {min: 0.75, max: 1.0}
        
        let start = {x: 50, y: 50}
        let end = {x: layer.width - 50, y: layer.height - 50}
        
        brush.paintLine(layer, start, end)
    }
}
```

![Example Output](../../.gitbook/assets/8dbf66.png)



