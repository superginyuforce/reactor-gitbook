---
description: Painting individual points
---

# Single Points

Paint at a specific location.

![Individually painted points, using a scaling, rotating multicolored brush](../../.gitbook/assets/1a773a.png)

### Brush Method <a id="overview"></a>

**`paintPoint(layer, point)`**

### ‌Parameters‌

1. **point** - point at which the brushstroke is drawn

| Name | Type/s | Example/s |
| :--- | :--- | :--- |
| point | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |

### Example

#### Paint One Point

```javascript
const point = {x: 100, y: 250}

brush.paintPoint(layer, point)
```

