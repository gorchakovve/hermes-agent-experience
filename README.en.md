# Hermes Agent: real incidents, checks and resolutions

**English** · [Русский](README.md)

This archive documents practical work with Hermes Agent, OpenClaw, VPS infrastructure, Telegram, desktop clients and VPNs from April to September 2026. It is not a universal setup guide or a catalogue of victories. Each case distinguishes an observation from a hypothesis, a check from an assertion, and the operator's actions from those of an agent. Private operational records were used to check facts; they have not been republished.

**88 distinct cases:** 40 resolutions or bounded workarounds are verified, 34 partially verified, and 14 remain open. These are evidence counts, not claims about the present health of anyone else's installation. Browse the [English index](docs/problem-index.en.md) or [Russian index](docs/problem-index.md). Published case IDs remain stable, and reciprocal language links make it possible to follow each case in either language.

## Starting points

- [Topic and status index](docs/problem-index.en.md): find a symptom and follow its P-ID.
- [P‑009: Hermes gateway file-descriptor exhaustion](docs/solutions/en/P-009-fd-exhaustion.md): recovery was verified, but the source of FD growth remains unknown.
- [P‑088: YAML dependencies versus the installed Desktop build](docs/solutions/en/P-088.md): an example of verifying the checkout and the shipped artifact separately.

Similar symptoms are not necessarily duplicates. For example, an ordinary Telegram reply and a tool-progress card travel through different delivery paths ([P‑044](docs/solutions/en/P-044.md), [P‑045](docs/solutions/en/P-045.md)). Related cases cross-reference one another; merging them without proof of a shared cause would obscure the distinct checks needed to repair them.

## Contribute or ask

Have a similar failure or a better test? Start a [Discussion](https://github.com/gorchakovve/hermes-agent-experience/discussions) for questions or open an [Issue](https://github.com/gorchakovve/hermes-agent-experience/issues) for a factual correction. Include the P-ID, versions, redacted symptoms, steps tried, and an observable result. An open case needs its own reproducible verification before it can be marked resolved.

**Privacy:** do not attach passwords, keys, tokens, login codes, personal contact information, private addresses, full logs, or configuration files. Substitute clear placeholders in commands and review attachments before posting.
