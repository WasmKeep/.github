# WasmKeep

**Self-hosted stateful actors, written in any language that compiles to
WebAssembly, on servers you own.**

WasmKeep runs *actors*: small programs that each own a piece of state (a chat
room, a user's session, a game lobby, a rate limit, a device) and handle one
event at a time.

- Each actor is a WebAssembly component, run on [Wasmtime](https://wasmtime.dev).
- Each actor has its own SQLite database. Idle actors leave memory and come
  back on the next request.
- Actor databases are replicated to S3-compatible object storage, so an actor
  can be restored on another node when one goes down.
- Run it as a single node, or as a cluster of nodes sharing one bucket.
- SDKs for Rust, TypeScript, Go, Python, C and Zig.

> **Status: pre-alpha.** APIs and storage formats may change, and it is not
> ready for production use.

Start with the main repository: [WasmKeep/wasmkeep](https://github.com/WasmKeep/wasmkeep).

WasmKeep is open source under the Apache-2.0 licence.
