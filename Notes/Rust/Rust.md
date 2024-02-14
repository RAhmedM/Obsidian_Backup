# Types

- `u32` -> unsigned 32 bit integer
- `i32` -> signed 32 bit integer
- `str` -> string slice
- `char` -> single character
- [[&str ]]-> string slice
- [[Tuples]] 
# [[Ownership]]



# Functions in rust

```
fn func_name(parameters) -> return_type
{}
```

```rust
fn plus_one(x: i32) -> i32 {
    x + 1;
}
```

In Rust, the return value of the function is synonymous with the value of the final expression in the block of the body of a function. You can return early from a function by using the `return` keyword and specifying a value, but most functions return the last expression implicitly.

## { } in rust

{ } in define scope and an expression. 

```rust
{
	let y = 1;
	y+1;
}
```

this is and expression and will return 2;

## [[Struct]]

```rust
struct User {
    active: bool,
    username: String,
    email: String,
    sign_in_count: u64,
}
```

- access individual elements using dot notation
- objects can be mutable


# Enums
**