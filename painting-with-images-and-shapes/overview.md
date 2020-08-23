# Overview

Reactor contains a powerful library for using shapes and images as brushes. A wide array of brush properties can be controlled programmatically, using combinations of constant values, random variables, and parametric functions. At a basic level, the process of creating and using a brush looks like this:

```javascript
import { Brush } from 'reactor'

const brush = new PolygonBrush()
const start = {x: 0, y: 0}
const end = layer.size

brush.paintLine(layer, start, end)  // paint a diagonal line
```

