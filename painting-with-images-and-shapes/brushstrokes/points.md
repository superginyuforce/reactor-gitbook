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

#### Paint One Point

```javascript
const point = {x: 100, y: 250}

brush.paintPoint(layer, point)
```

