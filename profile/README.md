# Swift Atoms

Use this organization when you need a small, single-purpose building block that anything else can depend on: bytes and bits, typed values and phantom tags, ownership and memory, indices and cursors, algebraic structures, geometry, time, and raw async coordination. It is Layer 1 of the [Swift Institute](https://github.com/swift-institute), what must exist. For a domain built from these alone, such as buffers or trees, look in [swift-molecules](https://github.com/swift-molecules). For a specification, look in [swift-standards](https://github.com/swift-standards). For I/O, rendering and anything opinionated, look in [swift-compositions](https://github.com/swift-compositions).

## Start here

- [swift-tagged](https://github.com/swift-atoms/swift-tagged): phantom-typed value wrappers
- [swift-async](https://github.com/swift-atoms/swift-async): raw async coordination, a layer below `AsyncSequence`
- [swift-ownership](https://github.com/swift-atoms/swift-ownership): `~Copyable` ownership types: borrows, inouts, unique and copy-on-write cells, atomic slots
- [swift-byte](https://github.com/swift-atoms/swift-byte): a byte type distinct from `UInt8`
- [swift-geometry](https://github.com/swift-atoms/swift-geometry): affine geometry with compile-time coordinate spaces
- [swift-logic](https://github.com/swift-atoms/swift-logic): classical and three-valued Strong Kleene logic for `Bool?`
