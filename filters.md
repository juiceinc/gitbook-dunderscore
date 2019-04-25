---
description: >-
  Filters allow interpolated values to be transformed. After a value is
  interpolated it can be passed through a chain of filtering functions.
---

# Filters

Filters allow interpolated values to be transformed. After a value is interpolated it can be passed through a chain of filtering functions.

```text
<%= value|filter1 %>

// multiple filters can be chained

<%= value|filter1|filter2 %>
```

Filters may take one or more arguments like this.

```text
<%= value|filter1:arg1,arg2 %>

// multiple filters with arguments can be chained

<%= value|filter1:arg1,arg2|filter2|filter3:arg1 %>
```

