# Ukiyo agent skill

## 1. Agents paying with x402 or MPP, no account

Buy GPU blocks at `POST https://pay.u-kiyo.ai/api/machine/gpu-blocks` or jobs at `POST https://pay.u-kiyo.ai/api/machine/gpu-jobs`. Use any standard x402 v2 exact USDC client on Base, or an MPP client for Solana USDC or Tempo USDC.e. No signup or API key is required.

Read [pricing](https://pay.u-kiyo.ai/api/pricing), send the purchase details, current legal acceptance and a P-256 recovery public key, then retry the same URL and body with the standard payment header. Save the returned access token and retain the recovery private key. Read the [complete payment, recovery and Bazaar guide](https://docs.u-kiyo.ai/connect/machine-payments) before paying.

Cloudflare operators: raise the default $0.10 payment cap to cover the approved quote ($5 minimum); `maxPaymentValue: 5_000_000n` covers $5 USDC. Keep a cumulative budget. Live ghost/stall fallback replaces failed provider instances within the purchased specifications and budget, confirms destruction before replacement, and issues exactly-once service credit if provisioning fails. Anonymous cards and inference are unavailable.

## 2. Agents and developers using the API with an account

The existing API-key/account-balance flow is unchanged: CLI `ukiyo` 0.2.5, local MCP `ukiyo-mcp` 0.2.0 and pinned Skill `ukiyo-compute` 1.0.1. These are existing release downloads, not new npm releases. The account instructions below apply to this path. Skill 1.0.1's immutable artifact references CLI 0.2.2; keep the separately installed CLI 0.2.5. See the full guide for artifact links and checksums.


A skill file (`SKILL.md`) that teaches an AI agent how to rent a GPU on Ukiyo, run its workload and shut the GPU down safely, using the [Ukiyo CLI](https://github.com/ukiyocompute/ukiyo-cli).

**Pinned version: 1.0.1** · [Docs](https://docs.u-kiyo.ai/connect/skill) · [Website](https://u-kiyo.ai)

## Install

Give your agent this file, or copy it into your agent's skills folder:

```text
https://u-kiyo.ai/releases/skill/1.0.1/ukiyo-compute/SKILL.md
```

SHA-256: `719fca36ec699aecd30f391c307703a9935aa56f510f8cc8803546f06c37fddf` (also in [SHA256SUMS](https://u-kiyo.ai/releases/SHA256SUMS)).

Install CLI 0.2.5 separately. The pinned Skill references CLI 0.2.2; do not downgrade the installed CLI. Read the current Terms and Privacy before explicit acceptance; obtain the current version from the API rather than copying an old example.

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
