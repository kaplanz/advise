# advise

[![build status][ci.rust.badge]][ci.rust.hyper]
[![dependency status][deps.badge]][deps.hyper]
[![latest version][version.badge]][version.hyper]
[![documentation][docs.badge]][docs.hyper]
![license][license.badge]

## About

This crate offers a streamlined way to keep users informed about your program's
progress and potential issues. It provides:

- Convenience macros: Advise at familiar logging levels `error!`, `warn!`,
  `info!`, `debug!`, and `trace!` to categorize your messages.
- Customizable tags: Design your own message tags using the `Render` trait,
  tailoring the specific needs to your application.

## Usage

Similar to the [`log`][log] crate, `advise` provides a simple API for printing
status messages that should be enough for the majority of use-cases.

```rust
use advise::{info, warn};

fn main() {
    warn!("It's dangerous to go alone!");
    info!("Take this.");
}
```

Running the above code will print the following to stderr.

<pre>
<span style="color:orange">warn</span><b>:</b> It's dangeous to go alone!
<span style="color:green">info</span><b>:</b> Take this.
</pre>

> [!IMPORTANT]
>
> GitHub currently does not support coloured text in markdown. You can run this
> [example] with `cargo run --example=basic` to see the above output rendered in
> colour.

## License

This project is dual-licensed under both [MIT License][license.mit] and [Apache
License 2.0][license.ap2]. You have permission to use this code under the
conditions of either license pursuant to the rights granted by the chosen
license.

<!-- Reference-style badges -->
[ci.rust.badge]: /../../actions/workflows/rust.yml/badge.svg
[ci.rust.hyper]: /../../actions/workflows/rust.yml
[deps.badge]:    https://deps.rs/repo/github/kaplanz/advise/status.svg
[deps.hyper]:    https://deps.rs/repo/github/kaplanz/advise
[docs.badge]:    https://docs.rs/advise/badge.svg
[docs.hyper]:    https://docs.rs/advise
[license.badge]: https://img.shields.io/crates/l/advise.svg
[version.badge]: https://img.shields.io/crates/v/advise.svg
[version.hyper]: https://crates.io/crates/advise

<!-- Reference-style files -->
[license.ap2]: ./LICENSE-APACHE
[license.mit]: ./LICENSE-MIT
[example]:     ./examples/basic.rs

<!-- Reference-style links -->
[log]: https://docs.rs/log
