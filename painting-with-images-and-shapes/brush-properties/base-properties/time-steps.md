---
description: >-
  Number of iterations with which a brush image or shape is drawn at each point
  along a path
---

# Time Steps

At each point in a brushstroke, brushes executes a subroutine, which results in a shape or image being dawn for one or more iterations. The `steps` parameter allows you to control how many iterations there are. Putting this into pseudocode, we have something like this:

```javascript
// NOTE: this is pseudocode

let n = brushStrokePath.length
let m = brush.steps

// for each point in stroke...
for (let i = 0; i < n; i++) {
    let p = brushStrokePath[i]
    
    // for each time step...
    for (let j = 0; j < m; j++) {
        drawBrushShapeOrImage(brush, p, i, j, n, m);
    }
}
```

### Datatype

* **Units**: Angle in radians
* **Range**: `[1, inf)`
* **Type**: `float`

### Example

```javascript
const brush = new Brush()

// set to constant number of three steps
brush.angle = 3

// ...or set to random, between 1 and 3
brush.radius = {min: 1, max: 3}
```

