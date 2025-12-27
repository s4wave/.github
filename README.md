<h3 align="center">
  <a href="https://github.com/s4wave" target="_blank" rel="noopener noreferrer">
    <img height="100" src="https://github.com/s4wave/.github/blob/master/images/s4wave-github.png?raw=true" alt="spacewave">
  </a>
  <br/>
  &nbsp;
</h3>
<p align="center">
  next-gen go and typescript tools
</p>
<p align="center" style="margin-top: 5px">
  <a href="https://discord.gg/opencode">
    <img src="https://img.shields.io/discord/1391832426048651334.svg?label=OpenCode&logo=Discord&colorB=7289da&style=for-the-badge" alt="OpenCode Discord" />
  </a>
  &nbsp;
  <a href="https://discord.gg/KJutMESRsT">
    <img src="https://img.shields.io/discord/803825858599059487.svg?label=Aperture&logo=Discord&colorB=7289da&style=for-the-badge" alt="Aperture Discord" />
  </a>
</p>

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
