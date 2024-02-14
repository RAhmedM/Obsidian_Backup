## _Slices_ let you reference a contiguous sequence of elements in a collection rather than the whole collection. A slice is a kind of reference, so it is a non-owning pointer.

```
fn main() {
	let s = String::from("hello world");
	
	let s1: &str = &s[0..5];
	let s2: &str = &s[6..11];
	let s3: &String = &s; 
}
```


s1 points to the hello part of the s string
s2 points to the world parts of the s string
s3 points to the whole s string

#### &str is a pointer hence it can not be mutable.

```rust
	let mut index = String::from("sad this is not what i wanted to do");
	let strr = &index[1..3];
	println!("{}", strr);
```

strr points to the index[1] and index[2] location


[Main Page](obsidian://open?vault=Notes&file=Rust%2FRust)