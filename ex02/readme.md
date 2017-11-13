# Testing

At its simplest, a test in Rust is a function that's annotated with the test attribute. Let's make a new project with Cargo called adder

```
cargo new adder
$ cd adder

```
Cargo will automatically generate a simple test when you make a new project. Here's the contents of src/lib.rs:

```
#[cfg(test)]
mod tests {
    #[test]
    fn it_works() {
    }
}
```
We can run the tests with cargo test

```
$ cargo test
   Compiling adder v0.1.0 (file:///home/you/projects/adder)
    Finished debug [unoptimized + debuginfo] target(s) in 0.15 secs
     Running target/debug/deps/adder-941f01916ca4a642

running 1 test
test it_works ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured

   Doc-tests adder

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured
```

# TO DO

You should write a simple test that compares two numbers

