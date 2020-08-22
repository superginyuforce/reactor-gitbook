# Polygon Brushes

Polygon brushes use polygons as brush tips. The default polygon is an equilateral triangle, but this can be controlled programmatically through the [sides parameter](sides.md), alongside many other things. Like [core brush parameters](../base-properties/), polygon or "shape" parameters can be defined as fixed values or probabilistic ranges; however, unlike core parameters, they can also be defined as parametric functions. Another significant difference is that shape parameters are computed for each brushstroke -- that is, each `brush.paint(...)` call -- and _not_ computed upon brush initialization.

