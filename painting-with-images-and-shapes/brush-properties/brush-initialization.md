---
description: How to set up your brushes
---

# Initialization

Brush parameters define the visual dynamics of a stroke. They have several core parameters that define the size and orientation of the brush tip as well as stroke density. Depending on the type of brush, there are a myriad of other parameters whose values are computed at runtime with each stroke and can be set to fixed values, random ranges, sample sets, or parametric functions. Overall, there are many more details and features, but if you can wrap your head around the basic idea of a Brush in Reactor,  you can get quite far, generating jaw-dropping art.

### Example Brush Definition

Here's a typical example of what you might want to do with a brush in Reactor. We'll create a new `Brush` object and proceed to set various parameters to demonstrate different ways to define them. The following will result in a brush whose stroke is a rotating ellipse, that gets larger and smaller and cycles through an array of colors as it goes.

```javascript
const brush = new EllipseBrush()

// conventient aliases...
const PI = Math.PI
const sin = Math.sin

// set parameters that are constant between strokes...
brush.radius = 0.025      // 2.5% canvas radius
brush.density = 10.0      // default is 1.0

// set parameters that are computed at each point in a stroke...
brush.tip.angle = (i, n) => 2 * PI * sin(8 * PI * i / (n - 1))
brush.tip.scale = (i, n) => 0.25 + 0.75 * sin(16 * PI * i / (n - 1))
brush.tip.fill.color = (i) => colors[i % colors.length]

// finally, configure and draw a ring!
const center = layer.center
const radius = 0.45                        // 45% canvas radius
const startAngle = this.random.radians()   // where on ring we start drawing 

brush.drawRing(layer, center, radius, startAngle)
```





