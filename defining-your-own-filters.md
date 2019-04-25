---
description: >-
  Any method mixed into underscore via the _.mixin method can be used as a
  filter.
---

# Defining your Own Filters

Any method mixed into underscore via the `_.mixin` method can be used as a filter.

For example, we can define a filter to reverse a string like this:

```javascript
  _.mixin({
    reverseFilter: function(s) {
      return s.split('').reverse().join('');
    }
  });
```

And then use it in a template like this:

```javascript
var template = _.template('Reverse of <%= label %> is <%= label|reverseFilter %>');
template({label: 'dunderscore'});

// Outputs:
    "Reverse of dunderscore is erocsrednud"
```

Any of the existing underscore methods can also be used as filters. For example:

```javascript
  var t = _.template('<% var f = new Function("stooge", "return stooge.age"); %> Maximum age: <%= stooges|max:f|values|last %>');
  var stooges = [{name: 'moe', age: 40}, {name: 'larry', age: 50}, {name: 'curly', age: 60}];
  t({stooges: stooges});

// Outputs:
    Maximum age: 60
```

