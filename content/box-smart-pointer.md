+++
title = 'Smart Pointers in Rust | Box'
date = 2024-06-16T17:51:56+05:45
draft = false
description="Smart Pointers in Rust | Box "
image ="/images/rustcrab.jpg"
imageBig ="/images/rustcrab.jpg"
categories= ["programming","rust","memory"]
authors= ["Saurab Poudel"]
avatar = "/images/avatar.webp"
+++

I read "the book" for the reference and examples

- pointer is a variable which stores address in memory
- smart pointer isn't unique to Rust . It was originated in C++\
- pointer only borrow data , but in many cases smart pointer owns the data
- it owns some memory and allow to manipulate it, they also have meta data and extra capabilities and guarantees
- Smart Pointer are usually implemented using structs, unlike an ordinary structs, they implements Deref and Drop traits
- Deref trait allows an instance of smart pointer struct to behave like a reference so we can write out code to work with either references or smart pointers
- Drop trait allows us to customize the code that run when an instance of the smart pointer goes out of scope.

## Common smart pointers in the standard library

- `Box<T>` for allocating values on the heap
- `Rc<T>`, reference counting type that enables multiple ownership
- `Ref<T>` and `RefMut<T>`, accessed through `RefCell<T>`, a type that enforces the borrowing rules at runtime instead of compile time

## Using `Box<T>` to Print to Data on the Heap

- allows us to store data on heap rather than stack
- pointer to the heap data remains in stack

### Box are used in this situations

- When we have a type whose size can't be known at compile time and we want to use a value of that type in a context that requires an exact time
- When we want ownership of large data but we don't want to deep copy
- When we want to own a value and we care only that it's a type that implements a particular trait rather than being of a specific type

### How to use a `Box<T>` to Store data on the Heap

Putting a single value on the heap isn't very useful, but ..

```rust
fn main(){
	let b = Box::new(8);
	prinln!("b = {b}");
}
```

Here b have value of box that points to the value 5, which is allocated on heap

when box goes out of scope deallocation happens both for box(stored on the stack) and the data it points to (stored on the heap)

### Enabling Recursive Types with Boxes

- Recursive type: A value of recursive type can have another value of the same type as part of itself.
- The nesting of values of recursive types could theoretically continue infinitely, so Rust can't know how much space the value needs
- But, boxes have a known size , that helps us enable recursive types by inserting a box in the recursive type definition
- cons list is an example of recursive type. Its a data structure that comes from the Lisp programming language. cons function constructs a new pair from its two argument
- pseudocode representation of a cons list containing the list 1,2,3 and each pair in parantheses: `(1,(2,(3,Nil)))`
- Nil acts as base case of recursion

#### Implementation

```rust
enum List {
    Cons(i32, Box<List>),
    Nil,
}

use crate::List::{Cons, Nil};

fn main() {
    let list = Cons(3, Box::new(Cons(4, Box::new(Cons(5, Box::new(Nil))))));
}
```

Cons variant needs the size of an i32 plus the space to store the box's pointer data.

Boxes provide only the indirection an heap allocation
It doesn't have performance overhead
It ensures that data are not copied but it ensures ownership
But its an smart pointer because it implements the Deref trait, which allows Box<T> values to be treated like references. Because of Drop trait implementation, the heap data that the box is pointing to is cleaned up.
