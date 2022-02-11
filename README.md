# rust-cheatsheet

[Rust Language Cheat Sheet](https://cheats.rs/)

## Prepare
### Cargo

```bash
PKG_NAME=hello_world
cargo new $PKG_NAME --bin
cd $PKG_NAME
```

### Vim Plugin

* https://github.com/rust-lang/rust.vim/

## Data Types

### Unsigned

type | value range
---- | ----
u8 | 0 ~ 255
u16 | 0 ~ 65_535
u32	| 0 ~ 4_294_967_295
u64	| 0 ~ 18_446_744_073_709_551_615
u128 | 0 ~ 340_282_366_920_938_463_463_374_607_431_768_211_455
usize	| Depending on platform pointer size, same as u16, u32, or u64.

### Signed

type | value range
---- | ----
i8 | -128 ~ 127
i16 | -32_768 ~ 32_767
i32	| -2_147_483_648 ~ 2_147_483_647
i64	| -9_223_372_036_854_775_808 ~ 9_223_372_036_854_775_807
i128 | -170_141_183_460_469_231_731_687_303_715_884_105_728 ~ -170_141_183_460_469_231_731_687_303_715_884_105_728
isize	| Depending on platform pointer size, same as i16, i32, or i64.

### Float

| type |
| ---- |
| f32 |
| f64 |

### Char

Always 4 bytes and only holds a single Unicode scalar value.

### str

An u8-array of unknown length guaranteed to hold UTF-8 encoded code points.

### Custom Types

#### Array and Slice
```rust
// array
let numbers: [i32; 5] = [1, 2, 3, 4, 5];
// slice
let slice = &numbers[1..3];
assert_eq!(slice, &[2, 3]);
```
