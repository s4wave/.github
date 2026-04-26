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

## License

[MIT](https://opensource.org/licenses/MIT) or [Apache-2.0](https://opensource.org/licenses/Apache-2.0)

---

<sub>An [Aperture Robotics, LLC](https://github.com/aperturerobotics) project.</sub>
