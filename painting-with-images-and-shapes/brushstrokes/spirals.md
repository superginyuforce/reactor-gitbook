---
description: Overview of spiral brushstrokes
---

# Spirals

![spiral stroke with triangular brush](../../.gitbook/assets/spiral-example.png)

### Overview

* **Type Name**: `"spiral"`
* **Call Convention**: `brush.paintSpiral(layer, center, radius, angle, coils)`

### Parameters

1. **center** - center point of ring
2. **radius** - radius of ring, expressed in percentage of layer radius \(0.2 means 20% of layer radius\)
3. **angle** - angle, rotated from 0 , at which initial point in ring path is drawn
4. **coils** - the number of levels or coils in the spiral

| Name | Type/s | Example/s |
| :--- | :--- | :--- |
| center | `Vector`, `Array`, `Object` | `new Vector(x, y)`, `[x, y]`, `{x, y}` |
| radius | `float` | `0.5  (% layer width)` |
| angle | `float` | `2/3 * Math.PI  (radians)` |
| coils | `float` | `2.5` |

