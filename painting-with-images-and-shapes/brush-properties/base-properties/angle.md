---
description: The angle by which the brush shape or image is rotated around its center
---

# Angle

![](../../../.gitbook/assets/angle.png)

The angle of a brush defines the amount by which the brush is rotated, relative to its center at each point in a path. In the diagram above, the angle value was incremented in each successive vertical stroke.

### Datatype

* **Units**: Angle in radians
* **Range**: `(-inf, inf)`
* **Type**: `float`

### Example

```javascript
const brush = new Brush()

// set to constant radiants value
brush.angle = 2/3 * Math.PI

// ...or set to random value in range
brush.radius = {min: -1/2 * Math.PI, max: 1/2 * Math.PI}
```

