# Built-in filters

Dunderscore comes with two filters:

* `emphasis`: Surrounds a string value with `<strong></strong>` tags.
* `noemphasis`: Disables emphasis for this interpolation.

You can override either/both of these by defining your own versions.

```javascript
  _.mixin({
    emphasis: function(text) {
      return '<b>' + text + '</b>';
    }
  });
```

hello there chris
