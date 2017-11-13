# Hello Exonum!

## Dependencies

Exonum depends on the following third-party system libraries:

* LevelDB (persistent storage)
* RocksDB (persistent storage)
* libsodium (cryptography engine)
LevelDB and RocksDB are used as alternative storage engines, with LevelDB used by default. You need to install only the storage engine(s) you are intending to use.

## Rust Toolchain

Exonum repositories use the stable Rust toolchain that can be installed by using the rustup program:

```
curl https://sh.rustup.rs -sSf | sh -s -- --default-toolchain stable
```

## Compiling Exonum

You can verify that you installed dependencies and the Rust toolchain correctly by cloning the exonum repository and running its built-in unit test suite:

```
git clone https://github.com/exonum/exonum.git
cd exonum
cargo test --manifest-path exonum/Cargo.toml
```

You may also run the extended test suite located in the sandbox directory:

```
cargo test --manifest-path sandbox/Cargo.toml
```

Exonum supports RocksDB as an alternative data storage since version 0.2.0. To enable RocksDB support you need to pass additional parameter to Cargo:

```
cargo test --manifest-path exonum/Cargo.toml --features rocksdb
```
and for extended test suite:

```
cargo test --manifest-path sandbox/Cargo.toml --features rocksdb
```

If you want to use Exonum framework with RocksDB support as a dependency in your project, you should add the following line into Cargo.toml:

```
exonum = { version = "0.2.0", features = ["rocksdb"] }
```
