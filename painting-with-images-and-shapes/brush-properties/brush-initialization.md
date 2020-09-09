# Initialization

Brushes are initialized from a plain _parameters_ object. Internally, each brush has a distinct pseudo-random number generator \(RNG\), which it uses to compute values brush properties, based on brush parameters. When a brush is initialized with missing parameters, reasonable defaults are used.

### Parameters

Fixed values, ranges of random values, and in some cases, parametric functions can be set as brush parameters. Each brush inherits certain base properties, whose initial values are derived from parameters upon instantiation, while other properties are computed each time a "paint" method is called.

