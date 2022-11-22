# tokio-bincodec

![Crates.io](https://img.shields.io/crates/v/tokio-bincodec.svg) ![Crates.io](https://img.shields.io/crates/l/tokio-bincodec.svg) ![Docs.rs](https://docs.rs/tokio-bincodec/badge.svg)

A fork of tokio-bincode

## Usage

First, add this to your `Cargo.toml`:

``` toml
[dependencies]
tokio-bincodec = "0.1"
```

Then you can use it like so:

``` rust
#[derive(Serialize, Deserialize)]
struct MyProtocol;

// Create the codec based on your custom protocol
let codec = tokio_bincodec::bincodec::<MyProtocol>();

// Frame the transport with the codec to produce a stream/sink
let f = Framed::new(transport, codec);
```

## License

This project is licensed under the [MIT license](LICENSE).
