## Name
cljs.core/array?

## Signature
[x]

## Description

Returns true if `x` is a JavaScript array, false otherwise.

## Related
cljs.core/object?

## Examples

```clj
(array? #js [1 2 3])
;;=> true

(array? [1 2 3])
;;=> false

(array? "hi")
;;=> false
```