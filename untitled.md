---
description: >-
  Dunderscore can automatically emphasize any interpolation that matches a
  pattern.
---

# Auto-emphasis

Dunderscore can automatically emphasize any interpolation that matches a pattern.

Add the `autoEmphasize` setting to `_.templateSettings` with the pattern to match or pass it to the `_.template` method and if the pattern is found, the value will be automatically emphasized.

```javascript
  var t = _.template('<%= label %> is auto emphasized!', {autoEmphasize: /label/});
  t({'label': 'Dunderscore'});

  // Outputs:
      <strong>Dunderscore</strong> is auto emphasized!
```

You can use the `noemphasis` filter to suppress the auto emphasis on certain interpolations.

```javascript
  var t = _.template('This <%= label %> is auto emphasized but this <%= label|noemphasis %> is not.');
  t({'label': 'Dunderscore'});

  // Outputs:
    This <strong>Dunderscore</strong> is auto emphasized but this Dunderscore is not.
```

