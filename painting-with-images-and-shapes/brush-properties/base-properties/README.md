# Core Brush Properties



Each brush has a set of core parameters that affect the way it is drawn. These values can be initialized  from either a fix value or a range from which a value is selected at random \(uniformly\). These values depend on  the pseudo-random number number generator \(RNG\) internal to each brush -- specifically, they depend on its seed value, `brush.random.seed`.

{% hint style="info" %}
It is possible to "reset" these values to their initial state by calling the `reset` method or by re-seeding the brush's RNG via its `reseed` method. 
{% endhint %}

