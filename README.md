markdown.rs [![](https://travis-ci.org/johannhof/markdown.rs.svg?branch=master)](https://travis-ci.org/johannhof/markdown.rs) [![](https://img.shields.io/crates/v/markdown.svg)](https://crates.io/crates/markdown) [![](https://coveralls.io/repos/johannhof/markdown.rs/badge.svg?branch=master&service=github)](https://coveralls.io/github/johannhof/markdown.rs?branch=master)
===========

A simple native Rust library for parsing Markdown and (outputting HTML).

Usage
----------

To include markdown in your project add the following to your Cargo.toml:

```toml
[dependencies]
markdown = "0.2"

```

Now you can use the crate in your code with
```rust
extern crate markdown;
```

There is no full documentation right now, the only function exported by the library is `to_html`, which takes a markdown `&str` and converts it to an owned `String` containing html.

```rust
let html : String = markdown::to_html("__I am markdown__");

assert_eq!(&html, "<strong>I am markdown</strong>")
```

TODO
----------

- [ ] Reference Style Images
- [ ] Inline HTML
- [ ] Backslash Escapes
- [ ] Automatic Links
- [ ] List wrapping
- [ ] HTML Entities
- [ ] Obscure Emails

## License

Licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally
submitted for inclusion in the work by you, as defined in the Apache-2.0
license, shall be dual licensed as above, without any additional terms or
conditions.
