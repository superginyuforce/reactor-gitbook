---
description: Overview of linear splines
---

# Linear Splines

Connect a sequence of points using lines, like a line graph.

![zigzagging linear splines with rotating triangular brushes with various radii](../../.gitbook/assets/93c6ee.png)

### Overview‌ <a id="overview"></a>

* **Type Name**: `"linear-splines"`
* **Call Convention**: `brush.paintLinearSplines(layer, points)`‌

### ‌Parameters‌‌ <a id="parameters"></a>

1. **points** - sequence of points to stroke
2. **closed** - if `true`, the last point will be connected to the first point

| Name | Type/s | Example/s |
| :--- | :--- | :--- |
| points | `Array<Vector|Array|Object>` | `[new Vector(x, y)]`, `[[x, y]]`, `[{x, y}]` |

