---
layout: api-command
language: JavaScript
permalink: api/javascript/do/
command: do
io:
    -   - any
        - any
---

# Command syntax #

{% apibody %}
any.do(arg [, args]*, expr) &rarr; any
{% endapibody %}

# Description #

Evaluate the expr in the context of one or more value bindings.

The type of the result is the type of the value returned from expr.

__Example:__ The object(s) passed to do() can be bound to name(s). The last argument is the expression to evaluate in the context of the bindings.

```js
r.do(r.table('marvel').get('IronMan'),
    function (ironman) { return ironman('name'); }
).run(conn, callback)
```
