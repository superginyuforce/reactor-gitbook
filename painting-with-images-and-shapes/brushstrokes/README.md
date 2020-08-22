# Brushstrokes: Lines, Rings, etc.

The path followed by a brush can be one of several things, including **points**, **lines**, **rings**, **spirals**, and arbitrary sequences of points, or **paths**. There are two call conventions. For stroking lines, either of the following is acceptable...

```javascript
brush.paint(layer, {type: 'line', start, end})
```

or...

```javascript
brush.paintLine(layer, start, end)
```



