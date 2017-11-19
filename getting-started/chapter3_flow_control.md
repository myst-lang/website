# Chapter 3: Flow Control

Flow control is the act of modifying the flow of execution based on some condition. Myst provides two native methods of flow control - conditionals and loops.

## Conditionals

### When

Unlike most popular languages, Myst does not have an `if` expression. Instead the same concept is expressed using the keyword `when`.

For example, the Ruby code:

```ruby
if 1 < 2
  # ...
end
```

would be written in Myst as:

```myst
when 1 < 2
  # ...
end
```

The reason that Myst uses `when` instead of `if` is for consistency when multiple conditional expressions are chained together.


### When chaining

In languages with `if` expressions, there is often a mechanism for providing an alternative to execute when the condition is not met. Most often, this uses the `else` keyword. Myst follows suit, so the following will return `"condition was not met"`:

```myst
when 1 > 2
  "condition was met"
else
  "condition was not met"
end
```

In addition to this, most languages also provide a way to define another condition for that alternative. For example, Ruby has `elsif`:

```ruby
if 1 > 2
  "1 is more than 2"
elsif 1 == 2
  "1 is equal to 2"
else
  "no condition was met"
end
```

In Myst, however, multiple conditions can be chained together simply by using the `when` keyword again. So, in Myst, the above would be written as:

```myst
when 1 > 2
  "1 is more than 2"
when 1 == 2
  "1 is equal to 2"
else
  "no condition was met"
end
```

This is the primary motivation for using `when` instead of `if`. By re-using the same keyword for all conditional expressions, even when defining alternatives for another condition, the code is kept more visually-aligned. All of the conditions being evaluated start in the same column, meaning the code can be scanned more quickly, and avoids having a jagged pattern, as in the Ruby version above.


### Unless

Myst also provides an `unless` keyword to define an "inverse condition". In other words, where a `when` expression would evaluate its body when the condition is truthy, an `unless` expression evaluates its body when the condition is falsey.

`unless` expressions can stand on their own, or be mixed into `when` chains to more cleanly define behavior:

```myst
unless true == false
  "true was not equal to false"
end
```


## Loops

Loops execute blocks of code repeatedly based on a conditional value that is evaluated each time.

### While

`while` is used to execute a block of code repeatedly until the condition is not met. For example:

```myst
n = 0
while n < 10
  # do some work
  n += 1
end
```

The above code would execute 10 times, after which the condition `n < 10` would be false, and looping would stop.

### Until

Similar to how `unless` is the inverse of `when`, `until` is the inverse of `while`. Its body will be executed repeatedly until the condition _is_ met. The above example could be re-written with `until` like so:

```myst
n = 0
until n >= 10
  # do some work
  n += 1
end
```

`until` (and `unless`) are provided as a convenience for more clearly showing the intent of a conditional expression.
