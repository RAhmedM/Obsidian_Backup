
```rust
struct User {
    active: bool,
    username: String,
    email: String,
    sign_in_count: u64,
}

fn main(){
	let user1 = User{
		active: false;
		username: String::from"Ahmed";
		email: String::from("ahmed.mustafa8696@gmail.com");
		sign_in_count: 1;
	};
}
```

access individual element using the dot notation

```rust
	User.active = true;
```

#### Using the Field Init Shorthand

```rust
fn build_user(email: String, username: String) -> User {
    User {
        active: true,
        username,
        email,
        sign_in_count: 1,
    }
}
```

the parameters of the function and the struct fields have the same name hence we can use this syntax to assign them directly.

## Struct Update Syntax
```rust
let user2 = User {
		active: user1.active,
		username: user1.username,
		email: String::from("another@example.com"),
		sign_in_count: user1.sign_in_count,
};
```

change this to this

```rust
let user2 = User {
        email: String::from("another@example.com"),
        ..user1
    };
```

Using struct update syntax, we can achieve the same effect with less code, as shown in Listing 5-7. The syntax `..` specifies that the remaining fields not explicitly set should have the same value as the fields in the given instance.

The `..user1` must come last to specify that any remaining fields should get their values from the corresponding fields in `user1`

`..user1` uses `=` to assign value so when we copy string we also give up [[Ownership]]

## Tuple Structs

```rust
struct Color(i32, i32, i32);
struct Point(i32, i32, i32);

fn main() {
    let black = Color(0, 0, 0);
    let origin = Point(10, 0, 0);
	println!("{}", origin.0); //this will print 10
}
```

Damn, this is
![Alt text](data:image/jpeg;base64,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)

### Unit-Like Structs Without Any Fields
```Rust
struct AlwaysEqual;

fn main() {
    let subject = AlwaysEqual;
}
```

- every object of a struct has ownership
- every attribute of a struct also has separate ownership

## Printing Structs

We can use `println!("{:#?}", user1)` to print the struct but first we have to add 1 line before defining the struct.

```Rust
#[derive(Debug)]
struct User{
	name: String,
	email: String,
	phone_number: String
}
```
the `#[derive(Debug)]` line allows us to print the whole struct.

we can also use `dbg!()` instead of `println!()` 

---

# Methods in Structs

Implementing area function for Rectangle struct.

```rust
#[derive(Debug)]
struct Rectangle {
    width: u32,
    height: u32,
}
impl Rectangle {
    fn area(&self) -> u32 {
        self.width * self.height
    }
}

fn main() {
    let rect1 = Rectangle {
        width: 30,
        height: 50,
    };

    println!(
        "The area of the rectangle is {} square pixels.",
        rect1.area()
    );
}
```


`impl Rectangle` implements the Rectangle structure

You can add `#[derive(Copy, Clone)]` to a struct to be able to make a copy of it when needed.

# sada
- asfa