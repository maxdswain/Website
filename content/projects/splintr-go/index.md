---
title: "splintr-go"
description: "Go bindings for the Rust splintr tokeniser, with batch processing, streaming decoding and explicit native-resource cleanup."
summary: "Bring Rust tokenisation to Go with cgo bindings, parallel batch operations, streaming decoding and explicit resource cleanup."
weight: 40
featureimage: "project-logos/tokens.svg"
showBreadcrumbs: true
---

{{< lead >}}
Bringing Rust-based tokenisation into Go services without introducing a separate inference service.
{{< /lead >}}

{{< keywordList >}}
{{< keyword icon="skill-go" >}}Go{{< /keyword >}}
{{< keyword icon="code" >}}Rust{{< /keyword >}}
{{< keyword icon="skill-c" >}}cgo{{< /keyword >}}
{{< keyword icon="code" >}}Tokenisation{{< /keyword >}}
{{< /keywordList >}}

I built **splintr-go**, Go bindings for the Rust [splintr](https://github.com/ml-rust/splintr) tokeniser through cgo. It exposes native tokenisation through a Go API, with explicit control over native-resource lifetime.

{{< button href="https://github.com/maxdswain/splintr-go" >}}GitHub repository{{< /button >}}

## Capabilities

- **Encode and decode:** convert text to token IDs and back, with bundled pretrained vocabularies or a supplied Hugging Face `tokenizer.json`.
- **Parallel batches:** encode and decode batches using native parallelism for larger inputs while preserving input order.
- **Streaming decoding:** incrementally decode generated token IDs, buffering split UTF-8 characters until they can be emitted correctly.
- **Concurrency and cleanup:** support concurrent tokeniser calls and explicit `Close` methods for releasing native resources.
- **Distribution:** provide platform-specific native release archives and documented build and linking instructions.

## Integration notes

The bindings use cgo and require a native library and C toolchain. Bundled vocabularies can be loaded without runtime downloads; the upstream documentation lists their compatibility and separate licences. Streaming support is for **decoding**, not incremental encoding.

- [Go API reference and examples](https://pkg.go.dev/github.com/maxdswain/splintr-go)
- [Available pretrained vocabularies](https://github.com/maxdswain/splintr-go/blob/main/docs/pretrained.md)
- [Native-library release instructions](https://github.com/maxdswain/splintr-go/blob/main/docs/releases.md)
