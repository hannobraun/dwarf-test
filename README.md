# DWARF Test

A small project to demonstrate that rustc generates invalid DWARF when LTO is enabled.

How to reproduce:

```
git clone https://github.com/hannobraun/dwarf-test.git
git clone https://github.com/gimli-rs/gimli.git
```

In the `dwarf-test` directory, run:
```
cargo build
```

In the Gimli directory, run:
```
cargo run --example dwarf-validate ../dwarf-test/target/debug/dwarf-test
```

You should see a whole lot of error messages.
