# Chapter 2: Basic Operations

## Mathematic operations

Most primitive values define the basic mathematic operations, `+`, `-`, `*`, `/`, `%`. Some examples:

```myst
1 + 1       #=> 2
2.6 + 3.8   #=> 6.4
10 * 10     #=> 100
120 % 100   #=> 20
"h" + "i"   #=> "hi"
```

Collections also implement some operations like `+`:

```myst
[1, 2] + [3, 4] #=> [1, 2, 3, 4]
```


## Logical operations and truthiness

Myst provides two native logical operations, "or" (`||`) and "and" (`&&`). These operate based on the truthiness of the first operand.

All values are considered truthy unless they are either `nil` or `false`.

The result of a logical operation is the value that determined the action taken by the operation.

```myst
false || false  #=> false
false || true   #=> true

1 || 2          #=> 1
nil || 2        #=> 2
nil && 2        #=> nil
2 && 3          #=> 3
```


## Comparison operations

Most values define comparison operators, `<`, `<=`, `==`, `!=`, `>=`, `>`. These operations _always_ return a boolean value.

```myst
1 < 2         #=> true
10 == 20      #=> false
true != false #=> true
```


## Unary operations

`!`, `-`, and `*`.
