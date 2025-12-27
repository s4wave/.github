<p align="center">
  <a href="https://github.com/s4wave" target="_blank" rel="noopener noreferrer">
    <img height="120" src="https://github.com/s4wave/.github/blob/master/images/s4wave-github.png?raw=true" alt="Spacewave">
  </a>
</p>
<h3 align="center">
  Next-generation Go and TypeScript tools.
</h3>
<p align="center">
  s4wave builds next-generation Go and TypeScript tools<br />
  with a focus on type safety, testability, and developer experience.
</p>
<p align="center" style="margin-top: 5px">
  <a href="https://discord.gg/opencode">
    <img src="https://img.shields.io/discord/1323070894973878292.svg?label=OpenCode&logo=Discord&colorB=7289da&style=for-the-badge" alt="OpenCode Discord" />
  </a>
  &nbsp;
  <a href="https://discord.gg/KJutMESRsT">
    <img src="https://img.shields.io/discord/803825858599059487.svg?label=Aperture&logo=Discord&colorB=7289da&style=for-the-badge" alt="Aperture Discord" />
  </a>
</p>

## Projects

### ocpipe

[**ocpipe**][ocpipe] is an SDK for building LLM pipelines with [OpenCode] and [Zod].

- **Type-safe signatures** - Define inputs and outputs with Zod schemas
- **Modular architecture** - Compose modules into complex pipelines
- **Built-in checkpointing** - Resume pipelines from any step
- **OpenCode integration** - Leverage the OpenCode agent runtime

```typescript
import { signature, field, module, Pipeline, createBaseState } from "ocpipe";

const Greet = signature({
  doc: "Generate a friendly greeting for the given name.",
  inputs: { name: field.string("The name of the person to greet") },
  outputs: { greeting: field.string("A friendly greeting message") },
});

const pipeline = new Pipeline(
  {
    name: "hello-world",
    defaultModel: { providerID: "anthropic", modelID: "claude-haiku-4-5" },
  },
  createBaseState,
);

const result = await pipeline.run(module(Greet), { name: "World" });
```

[ocpipe]: https://github.com/s4wave/ocpipe
[OpenCode]: https://github.com/sst/opencode
[Zod]: https://zod.dev

## Support

Please open a [GitHub issue][github-issue] with any questions or feedback.

Join the [OpenCode Discord][discord] to connect with the community.

[github-issue]: https://github.com/s4wave/ocpipe/issues/new
[discord]: https://discord.gg/opencode

## License

Projects are licensed under [MIT](https://opensource.org/licenses/MIT) or [Apache-2.0](https://opensource.org/licenses/Apache-2.0).

---

<sub>An [Aperture Robotics, LLC](https://github.com/aperturerobotics) project.</sub>
