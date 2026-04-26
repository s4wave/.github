<h1 align="center">
  <a href="https://github.com/s4wave/spacewave" target="_blank" rel="noopener noreferrer">
    <img height="120" src="https://github.com/s4wave/.github/blob/master/images/s4wave-github.png?raw=true" alt="spacewave">
  </a>
</h1>
<h2 align="center">
  Self-host anything in the browser.
</h2>
<p align="center">
  Local-first apps on a portable Go + WebAssembly + TypeScript stack.<br/>
  Open source. Cloud optional.
</p>
<p align="center">
  <a href="https://github.com/s4wave/spacewave"><b>Get Spacewave →</b></a>
</p>
<p align="center" style="margin-top: 5px">
  <a href="https://discord.gg/KJutMESRsT">
    <img src="https://img.shields.io/discord/803825858599059487.svg?label=Join%20Discord&logo=Discord&colorB=7289da&style=for-the-badge" alt="Join Discord" />
  </a>
</p>

## 🚀 [Spacewave][spacewave]

**Self-host anything in the browser.** Local-first apps with optional cloud
sync, running natively or in the browser.

- 🌐 **Local-first** Apps run in the browser against an OPFS-backed object store
- ☁️ **Optional cloud** Fast cross-device sync and backup on Cloudflare
- 🦫 **Portable** Same Go code runs as WASM in the browser and natively as a CLI
- 🧩 **Composable** ObjectTypes, plugins, and packfile-based content addressing

[**Get started with Spacewave →**][spacewave]

[spacewave]: https://github.com/s4wave/spacewave

## [ocpipe]

Build LLM pipelines with [OpenCode] and [Zod].

- **Type-safe** Define inputs and outputs with Zod schemas
- **Modular** Compose modules into complex pipelines
- **Checkpoints** Resume from any step
- **Multi-model** Works with 75+ providers through OpenCode

```typescript
const Greet = signature({
  doc: "Generate a greeting.",
  inputs: { name: field.string("Name to greet") },
  outputs: { greeting: field.string("The greeting") },
});

const result = await pipeline.run(module(Greet), { name: "World" });
```

[Get started][ocpipe] · [OpenCode Discord][discord]

[ocpipe]: https://github.com/s4wave/ocpipe
[OpenCode]: https://github.com/sst/opencode
[Zod]: https://zod.dev
[discord]: https://discord.gg/opencode

## 🏗️ Projects

Spacewave is built on the App Stack below. Get started building your own
application on the stack with [the project template]!

[the project template]: https://github.com/aperturerobotics/template

### 🧱 App Stack

- [**ControllerBus**][controllerbus] - Dynamically configurable communicating control loops
- [**Bifrost**][bifrost] - Cross-platform networking engine with pluggable transports
- [**goscript**][goscript] - Transpile Go to TypeScript
- [**ocpipe**][ocpipe-link] - Build LLM pipelines with OpenCode and Zod

[controllerbus]: https://github.com/aperturerobotics/controllerbus
[bifrost]: https://github.com/aperturerobotics/bifrost
[goscript]: https://github.com/aperturerobotics/goscript
[ocpipe-link]: https://github.com/s4wave/ocpipe

### <img src="https://raw.githubusercontent.com/skiffos/SkiffOS/master/resources/images/skiff-icon.png" alt="SkiffOS logo" width="28" height="28" style="vertical-align: bottom"/> SkiffOS

[SkiffOS] is a minimal Linux distribution designed to run containers on embedded
devices. It uses [Buildroot] to cross-compile a tiny system image with support
for Docker and other container runtimes. [SkiffOS] enables running any Linux
distribution or application in lightweight containers on embedded hardware.

[SkiffOS]: https://github.com/skiffos/skiffos
[Buildroot]: https://buildroot.org

### 🪶 Lightweight Protobuf

These are lightweight reflection-free code-generation based implementations of
Protobuf designed to optimize binary size and performance, especially for
WebAssembly (wasm) applications.

- [**StaRPC**][starpc] - Protobuf 3 RPC services over any stream multiplexer
- [**protobuf-es-lite**][protobuf-es-lite] - Lightweight TypeScript protobuf implementation
- [**protobuf-go-lite**][protobuf-go-lite] - Lightweight Go protobuf implementation
- [**protobuf-project**][protobuf-project] - Template repository for projects using protobufs

[starpc]: https://github.com/aperturerobotics/starpc
[protobuf-es-lite]: https://github.com/aperturerobotics/protobuf-es-lite
[protobuf-go-lite]: https://github.com/aperturerobotics/protobuf-go-lite
[protobuf-project]: https://github.com/aperturerobotics/protobuf-project

Protobuf libraries like [protobuf-es] and [protobuf-go] focus on spec compliance
and feature-complete implementations. These **lite** libraries focus on just the
base proto2 and proto3 spec including RPCs to simplify the implementation.

[protobuf-es]: https://github.com/bufbuild/protobuf-es
[protobuf-go]: https://github.com/protocolbuffers/protobuf-go

### 🔌 QuickJS WASI Reactor

Run [QuickJS-NG] JavaScript engine in Go and TypeScript using the WASI reactor model for re-entrant execution:

- [**quickjs**][quickjs] - QuickJS-NG fork with WASI reactor build target
- [**go-quickjs-wasi**][go-quickjs-wasi] - Go module with embedded QuickJS-NG WASI command binary
- [**go-quickjs-wasi-reactor**][go-quickjs-wasi-reactor] - Go module with embedded QuickJS-NG WASI reactor binary
- [**js-quickjs-wasi-reactor**][js-quickjs-wasi-reactor] - Run QuickJS-NG within JavaScript with WASI reactor model

[QuickJS-NG]: https://github.com/quickjs-ng/quickjs
[quickjs]: https://github.com/paralin/quickjs
[go-quickjs-wasi]: https://github.com/paralin/go-quickjs-wasi

### 📚 Libraries

Common Go/TypeScript libraries:

- [**Common**][common] - Common project configuration files and Protobuf toolchain.
- [**Util**][util] - Go utilities for easy concurrent programming.
- [**go-kvfile**][go-kvfile] - File format for storing a compressed key/value store

Lightweight / modified forks of other libraries:

- [**Cayley**][cayley] - Go Graph database forked from [cayleygraph]
- [**FlexLayout**][flex-layout] - Interactive drag/drop layout manager for React
- [**fastjson**][fastjson] - Reflection-free json parser and validator
- [**go-brotli-decoder**][go-brotli-decoder] - Pure Go Brotli decompressor
- [**go-indexeddb**][go-indexeddb] - Low-level Go driver for IndexedDB in Wasm
- [**goprotowrap**][goprotowrap] - Package-at-a-time wrapper for protoc
- [**json-iterator-lite**][json-iterator-lite] - Minimal and fast reflection-free json marshal and unmarshal for Go

[cayley]: https://github.com/aperturerobotics/cayley
[fastjson]: https://github.com/aperturerobotics/fastjson
[flex-layout]: https://github.com/aperturerobotics/flex-layout
[go-brotli-decoder]: https://github.com/aperturerobotics/go-brotli-decoder
[go-indexeddb]: https://github.com/aperturerobotics/go-indexeddb
[go-kvfile]: https://github.com/aperturerobotics/go-kvfile
[go-quickjs-wasi-reactor]: https://github.com/aperturerobotics/go-quickjs-wasi-reactor
[goprotowrap]: https://github.com/aperturerobotics/goprotowrap
[js-quickjs-wasi-reactor]: https://github.com/aperturerobotics/js-quickjs-wasi-reactor
[json-iterator-lite]: https://github.com/aperturerobotics/json-iterator-lite
[cayleygraph]: https://cayley.io/
[util]: https://github.com/aperturerobotics/util
[common]: https://github.com/aperturerobotics/common

## 🙋 Support

Please open a [GitHub issue][github-issue] with any questions / issues / suggestions.

... or feel free to reach out via [Email] or [Discord][s4wave-discord]!

[github-issue]: https://github.com/s4wave/spacewave/issues/new
[Email]: mailto:oss@spacewave.app
[s4wave-discord]: https://discord.gg/KJutMESRsT

## License

[MIT](https://opensource.org/licenses/MIT) or [Apache-2.0](https://opensource.org/licenses/Apache-2.0)

---

<sub>An [Aperture Robotics, LLC](https://github.com/aperturerobotics) project.</sub>
