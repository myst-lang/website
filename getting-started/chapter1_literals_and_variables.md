# Chapter 1: Values and Variables


## Values

### Primitives

Literal values: `nil`, `false`, `true`, `1`, `1.0`, `"hello"`, `:hi`.

### Collections

`[1, 2, 3]`, `{a: 1, b: 2}`.

### User-defined types

Covered later.



## Variables

Variables store values. Any value can be assigned to any variable at any time.

### Locals

Local variables start with a lowercase alphabetic character and are written in `snake_case`.

### Underscores

Underscores are local variables that start with an ASCII underscore character, `_`.

### Constants

Constants start with uppercase alphabetic characters, and are written either in `UpperCamelCase`, or `SCREAMING_CASE`.



## Assignments

Variables are created by assigning values to them. They can be re-assigned to later on to change their value

```myst
x = 1 #=> 1
x     #=> 1
x = 2 #=> 2
x     #=> 2
```
