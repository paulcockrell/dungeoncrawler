# Dungeon Crawl

Rust dungeon crawl game built from the tutorial book 'Hands on Rust'

## Resources for converting to WASM

[Link](https://hands-on-rust.com/2021/11/06/run-your-rust-games-in-a-browser-hands-on-rust-bonus-content/)

## Deps

Appart from Rust, to compile to WASM run the following before the release build step

```
rustup target add wasm32-unknown-unknown
cargo install wasm-bindgen-cli
```

## Dev

```
cargo run
```

## Build

```
cargo build --target wasm32-unknown-unknown --release
wasm-bindgen target/wasm32-unknown-unknown/release/dungeoncrawl.wasm --out-dir ./wasm_help --no-modules --no-typescript
```
