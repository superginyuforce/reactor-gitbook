---
description: Understanding brush parameters
---

# Parameters

Each brush has a set of core parameters that affect the way it is drawn. These values can be initialized  from either a fix value or a range from which a value is selected at random \(uniformly\). These values depend on  the pseudo-random number number generator \(RNG\) internal to each brush -- specifically, they depend on its seed value, `brush.random.seed`.

{% hint style="info" %}
It is possible to "reset" these values to their initial state by calling the `reset` method or by re-seeding the brush's RNG via its `reseed` method. 
{% endhint %}

{% hint style="warning" %}
Other non-core properties are computed for each brush stroke, _not_ upon brush initialization. Such properties include things like shape scaling, scattering, etc. See: [Polygon Brushes](../brush-types/polygon-brushes.md)
{% endhint %}

### [Density](static-parameters/density.md)

The degree to which points between the start and end of a path are sparse or densely packed

### [Radius](static-parameters/radius.md)

The size of the brush image or shape, relative to a host layer's canvas

### [Angle](static-parameters/angle.md)

The angle by which the brush shape or image is rotated around its center

### [Time Steps](static-parameters/time-steps.md)

Number of iterations with which a brush image or shape is drawn at each point along a path

