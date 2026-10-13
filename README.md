# Ukiyo agent skill

A skill file (`SKILL.md`) that teaches an AI agent how to rent a GPU on Ukiyo, run its workload and shut the GPU down safely, using the [Ukiyo CLI](https://github.com/ukiyocompute/ukiyo-cli).

**Current version: 1.0.2** · [Docs](https://docs.u-kiyo.ai/connect/skill) · [Website](https://u-kiyo.ai)

## Install

Give your agent this file, or copy it into your agent's skills folder:

```text
https://u-kiyo.ai/releases/skill/1.0.2/ukiyo-compute/SKILL.md
```

SHA-256: `2eb89fcecef81521d1d5eed75e0109cfe9145f274cfbc63247d3a3b56d6ba52e` (also in [SHA256SUMS](https://u-kiyo.ai/releases/SHA256SUMS)).

It installs [CLI 0.2.5](https://github.com/ukiyocompute/ukiyo-cli) with a checksum check, and signs up with explicit agreement to the current [Terms](https://u-kiyo.ai/terms/) (`ukiyo signup --accept-terms 2026-10-10 --json`).

## What the skill covers

- Installing the CLI and signing up with explicit Terms agreement
- Checking the account, balance, billing model and spending limits
- Finding an offer and renting it safely, with idempotency keys so retries never double-rent
- Waiting until the GPU is ready, then running commands with `ukiyo exec`
- Terminating and confirming the final state and charges

## Related

- [ukiyo-cli](https://github.com/ukiyocompute/ukiyo-cli) · [ukiyo-mcp](https://github.com/ukiyocompute/ukiyo-mcp) · [ukiyo-api](https://github.com/ukiyocompute/ukiyo-api) · [ukiyo-guides](https://github.com/ukiyocompute/ukiyo-guides)

## Support

**contact@u-kiyo.ai**. Please don't include API keys or private keys in issues.

## License

[MIT](LICENSE) © 2026 Ukiyo Compute LLC. Covers this skill file; the Ukiyo service is governed by the [Terms](https://u-kiyo.ai/terms/).
