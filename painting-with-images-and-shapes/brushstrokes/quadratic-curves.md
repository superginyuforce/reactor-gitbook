---
description: Stroke a quadratic curve with one control point
---

# Quadratic Curves

Draw a quadratic Bezier curve between two points, using a single control points.

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
const start = {x: 10, y: 10}
const end = {x: 200, y: 50}
const cp = {x: 20, y: 30}

brush.paintQuadraticCurve(layer, start, cp, end)
```



