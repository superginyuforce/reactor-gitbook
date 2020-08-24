---
description: Overview of spiral brushstrokes
---

# Spirals

Draw a spiral, according to its desired position, radius, and coils, i.e. number full rotations.

![Spirals drawn with rotating triangular brush](../../.gitbook/assets/e3df00.png)

### Brush Method

**`paintSpiral(layer, center, radius, coils, angle?)`**

### Parameters

1. **center** - center point of ring
2. **radius** - radius of ring, expressed in percentage of layer radius \(0.2 means 20% of layer radius\)
3. **coils** - the number of levels or coils in the spiral
4. **angle** - angle, rotated from 0 , at which initial point in ring path is drawn **\(not yet implemented\)**

| Name | Type/s | Example/s |
| :--- | :--- | :--- |
| center | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |
| radius | `float` | `0.5  (% layer width)` |
| coils | `float` | `2.5` |
| angle | `float` | `2/3 * Math.PI  (radians)` |

