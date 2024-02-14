- just a collection of data
- data could be of different types


```rust
fn main() {
    let a: (i32, char, &str)= (1, 'c', "this is not ok")
}
```

As always you don't have to define the data types of the values it will recognize them.

you can access the individual values using this notation:
```rust
	let num: int = a.0
	let c: char = a.1
	let s: &str = a.2
```

# Arrays

You also have the array type.

```rust
	let arr: [i32; 5] = [1, 2, 3, 4, 5]
```

You can either define the size of the array yourself or just let the interpreter figure it out itself.

to access array elements:
```
	arr[1];
```