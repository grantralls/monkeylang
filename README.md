# Monkey Interpreter

This repo contains the completed monkey interpreter from [Writing an Interpreter in Go](https://interpreterbook.com/).

# Packages

- lexer - Takes code (as a string) as input and spits out tokens with `NextToken()`
- parser - Receives tokens from the parser and generates an Abstract Syntax Tree (AST). This adds semantic meaning to the tokens.
- evaluator - Takes the AST, and "runs" (or evaluates) each node. This produces objects.
- repl - Read-Eval-Print-Loop. A live interactive environment to run monkey code.

# Language Features

## Variables

```
let a = 5;
let name = "Bob";
let conditional = false;
```

## Control Flow

```
if (conditional) {
} else {
}
```

## Functions

```
let add = fn(x, y) {
    return x + y;
};
let result = add(2, 2);
puts(result); // prints 4
```

## Arrays

```
let list = [1, 2, "three", false]
```

## Maps

```
let data = {"name": "Bob", "age": 50, isCustomer: false};
puts(data["name"]) // prints "Bob"
```

## Builtin Functions
- `len(x)` - returns the length of a passed string or array
- `first(arr)` - returns the first element in an array
- `last(arr)` - returns the last element in an array
- `rest(arr)` - returns a newly allocated array containing every element in `arr` except the first
- `push(arr, x)` - returns a newly allocated array containing every element of `arr`, with `x` appended to the end
- `puts(x, y, z, ....)` - prints the string representation of each parameter in its own line.
