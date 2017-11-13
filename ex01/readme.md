# Hello Cargo!

Cargo is Rust’s build system and package manager, and Rustaceans use Cargo to manage their Rust projects. Cargo manages three things: building your code, downloading the libraries your code depends on, and building those libraries.

To start a new project with Cargo, enter cargo new at the command line:

```
cargo new hello_world --bin

```
Cargo has generated two files and one directory for us: a Cargo.toml and a src directory with a main.rs file inside. These should look familiar, they’re exactly what we created by hand, above.

First, open Cargo.toml. It should look somethinglike this:

```
[package]

name = "hello_world"
version = "0.1.0"
authors = ["Your Name <you@example.com>"]

[dependencies]

```
Here’s what should be in src/main.rs:

```
fn main() {
    println!("Hello, world!");
}
```

Then

```
cargo build

cargo run
```

## Source

http://doc.crates.io/guide.html
