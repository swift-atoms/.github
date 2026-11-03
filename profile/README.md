# Swift Atoms

Atomic Swift building blocks — Layer 1 of the [Swift Institute](https://github.com/swift-institute) ecosystem.

## What this is

What must exist: the small, single-purpose packages every other layer builds on — bytes and bits, typed values and phantom tags, ownership and memory, indices and cursors, algebraic structures, geometry, time, and raw async coordination. [swift-molecules](https://github.com/swift-molecules) (Layer 2) builds from these packages alone; [swift-standards](https://github.com/swift-standards) (Layer 3) and [swift-compositions](https://github.com/swift-compositions) (Layer 4) build on top.

## Start here

| Package | What it gives you |
|---|---|
| [swift-tagged](https://github.com/swift-atoms/swift-tagged) | Phantom-typed value wrappers for zero-cost type safety |
| [swift-async](https://github.com/swift-atoms/swift-async) | Raw async coordination — Channel, Broadcast, Semaphore, Mutex, Barrier, Promise — a layer below AsyncSequence |
| [swift-ownership](https://github.com/swift-atoms/swift-ownership) | `~Copyable` ownership types — borrows, inouts, unique and copy-on-write cells, atomic slots |
| [swift-byte](https://github.com/swift-atoms/swift-byte) | A byte type distinct from `UInt8`, with bitwise operations and hex access |
| [swift-geometry](https://github.com/swift-atoms/swift-geometry) | Affine geometry — points, vectors, rectangles, transforms — with compile-time coordinate spaces |
| [swift-logic](https://github.com/swift-atoms/swift-logic) | Classical and three-valued Strong Kleene logic for `Bool?` |

## Browse everything

The [repositories tab](https://github.com/orgs/swift-atoms/repositories) lists every package with its description. Narrow it down:

[buffer](https://github.com/orgs/swift-atoms/repositories?q=buffer) · [memory](https://github.com/orgs/swift-atoms/repositories?q=memory) · [async](https://github.com/orgs/swift-atoms/repositories?q=async) · [geometry](https://github.com/orgs/swift-atoms/repositories?q=geometry) · [time](https://github.com/orgs/swift-atoms/repositories?q=time) · [parser](https://github.com/orgs/swift-atoms/repositories?q=parser) · [morphism](https://github.com/orgs/swift-atoms/repositories?q=morphism)

## Conventions

Every package in this organization adheres to a shared set of conventions:

- **Nest.Name naming** — no compound type names; `File.Directory.Walk`, never `FileDirectoryWalk`.
- **Typed throws end-to-end** — `throws(Domain.Error)`, not `any Error`.
- **One type per file** — predictable navigation, minimal merge conflicts.
- **`~Copyable` by default** — types opt into `Copyable`, not out of it.
- **`~Escapable` for views** — pointer-based views cannot outlive their base.
- **Strict memory safety** — enabled on every target; every unsafe-pointer site carries explicit `unsafe` vocabulary.
- **Multi-target per package** — Core + variants + umbrella; import the narrow variant you need.

## How to use a package

Each package is a separate Swift Package Manager package with its own repository — add the one you need directly:

```swift
dependencies: [
    .package(url: "https://github.com/swift-atoms/swift-tagged.git", branch: "main")
]
```

See each package's README for current products, platforms, and umbrella-vs-variant choices.

## Status

Public alpha. Packages are released repository by repository; APIs may change until first tagged releases.

Maintained by [Coen ten Thije Boonkkamp](https://github.com/coenttb) — contributions welcome via pull request.

## License

All packages in this organization use the Apache License 2.0.
