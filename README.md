TNetStrings: Tagged Netstrings

This module implements bindings for the [tnetstring](http://tnetstrings.org)
serialization format.

## API

    let t = tnetstring::str("hello world");
    let s = tnetstring::to_str(t) // returns "11:hello world,"

    let (t, extra) = tnetstring::from_str(s);
    alt option::get(t) {
      tnetstring::str(s) { ... }
      ...
    }

See the `tests` module in `lib.rs` for more examples.

## Compatibility

Use tag v0.1 with Rust 0.2.
