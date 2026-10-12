# Ukiyo agent skill

A skill file (`SKILL.md`) that teaches an AI agent how to rent a GPU on Ukiyo, run its workload and shut the GPU down safely, using the [Ukiyo CLI](https://github.com/ukiyocompute/ukiyo-cli).

**Current version: 1.0.1** · [Docs](https://docs.u-kiyo.ai/connect/skill) · [Website](https://u-kiyo.ai)

## Install

Give your agent this file, or copy it into your agent's skills folder:

```text
https://u-kiyo.ai/releases/skill/1.0.1/ukiyo-compute/SKILL.md
```

SHA-256: `719fca36ec699aecd30f391c307703a9935aa56f510f8cc8803546f06c37fddf` (also in [SHA256SUMS](https://u-kiyo.ai/releases/SHA256SUMS)).

> **Use the current CLI.** Skill 1.0.1's install section points at CLI 0.2.2. New accounts now need explicit Terms acceptance at signup, which requires **CLI 0.2.5**. Install the CLI from [ukiyo-cli](https://github.com/ukiyocompute/ukiyo-cli#install) and sign up with `ukiyo signup --accept-terms 2026-10-10 --json`. The rest of the skill's workflow is unchanged.

## What the skill covers

- Checking the account, balance and spending limits
- Finding an offer and renting it safely, with idempotency keys so retries never double-rent
- Waiting until the GPU is ready, then running commands with `ukiyo exec`
- Terminating and confirming the final state and charges

## Related

- [ukiyo-cli](https://github.com/ukiyocompute/ukiyo-cli) · [ukiyo-mcp](https://github.com/ukiyocompute/ukiyo-mcp) · [ukiyo-api](https://github.com/ukiyocompute/ukiyo-api) · [ukiyo-guides](https://github.com/ukiyocompute/ukiyo-guides)

## Support

**contact@u-kiyo.ai**. Please don't include API keys or private keys in issues.

## License

[MIT](LICENSE) © 2026 Ukiyo Compute LLC. Covers this skill file; the Ukiyo service is governed by the [Terms](https://u-kiyo.ai/terms/).
