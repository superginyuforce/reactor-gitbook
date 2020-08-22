---
description: Brush Density Property
---

# Density

As density increases, so does the number of points between the start and end points of a brushstroke. Lines, rings, and other paths are calibrated so that a density of `1.0` results in each point being spaced out by an amount equal to the brush's radius.

![](../../../.gitbook/assets/density.png)

### Units

Percentage of brush radius

### Type

`float`

### Examples

```javascript
const brush = new Brush()

// set to constant value
brush.density = 1.0

// set to random value in range
brush.density = {min: 0.5, max: 1.5}
```

