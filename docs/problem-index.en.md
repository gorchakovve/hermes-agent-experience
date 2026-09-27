# Problem index: Hermes, OpenClaw, VPS and devices

88 numbered case pages covering 88 distinct incidents or operational findings from April–September 2026. The status reports **verification of a usable resolution in the available record**, not perpetual service health: 40 verified, 34 partially verified, 14 open. A verified workaround may still have a root-cause limitation described in its article. The private primary records were used for fact-checking, not republished. [Русский](problem-index.md) · [English README](../README.en.md) · [Discussions](https://github.com/gorchakovve/hermes-agent-experience/discussions) · [Issues](https://github.com/gorchakovve/hermes-agent-experience/issues).

## VPS and agent operations

- **P-001** [Two OpenClaw entry points reported different CLI and gateway versions](solutions/en/P-001.md) — verified.
- **P-002** [Two OpenClaw gateways were competing for one port](solutions/en/P-002.md) — verified.
- **P-003** [OpenClaw update landed in an inactive package tree](solutions/en/P-003.md) — verified.
- **P-004** [Scheduled updater used a Node.js version below the package engine floor](solutions/en/P-004.md) — verified.
- **P-005** [OpenClaw updates overwrote local settings and compatibility patches](solutions/en/P-005.md) — verified.
- **P-006** [Desktop and VPS OpenClaw versions diverged](solutions/en/P-006.md) — verified.
- **P-007** [Gateway was active, but Telegram stopped responding](solutions/en/P-007.md) — partially verified.
- **P-008** [Hermes CLI responded, then crashed with exit code 134](solutions/en/P-008.md) — open.
- **P-009** [Hermes gateway exhausted its open-file limit](solutions/en/P-009-fd-exhaustion.md) — verified.
- **P-010** [Caches and backups filled the VPS disk](solutions/en/P-010.md) — verified.
- **P-011** [HAProxy failed to start because a TCP port was already owned](solutions/en/P-011.md) — verified.
- **P-012** [Cloudflare Access blocked HTTP-01 certificate renewal](solutions/en/P-012.md) — verified.
- **P-013** [The watchdog emitted critical alerts because its baseline was stale](solutions/en/P-013.md) — verified.
- **P-014** [An agent self-restart interrupted the current answer](solutions/en/P-014.md) — open.
- **P-088** [Updating vulnerable YAML packages does not update an already installed Desktop app](solutions/en/P-088.md) — verified.
- **P-089** [A disappearing temporary marker interrupted a Desktop profile backup](solutions/en/P-089.md) — verified.

## Authentication, models and fallbacks

- **P-015** [Multiple clients competed for a Codex OAuth refresh token](solutions/en/P-015.md) — verified.
- **P-016** [`relogin_required` did not always mean the model was currently unavailable](solutions/en/P-016.md) — verified.
- **P-017** [Device-code relogin hit a rate limit while runtime still responded](solutions/en/P-017.md) — partially verified.
- **P-018** [After updates, distinguish route misconfiguration from a verified smoke](solutions/en/P-018.md) — partially verified.
- **P-019** [`Blocked hostname` after cooldown: no proven targeted fix found](solutions/en/P-019.md) — open.
- **P-020** [The fallback chain mixed limits, a bad slug, and incompatible payload](solutions/en/P-020.md) — partially verified.
- **P-021** [`hermes doctor` falsely reported a Gemini failure](solutions/en/P-021.md) — partially verified.
- **P-022** [Direct VPS access to Gemini was region-restricted](solutions/en/P-022.md) — verified.
- **P-023** [Local proxy was blocked by private-address protection](solutions/en/P-023.md) — partially verified.
- **P-024** [An obsolete Google AI node stopped accepting connections](solutions/en/P-024.md) — partially verified.
- **P-025** [Google AI reserve was not fully accepted](solutions/en/P-025.md) — partially verified.

## MCP, external services and security

- **P-026** [Notion MCP broke strict tool-schema validation](solutions/en/P-026.md) — verified.
- **P-027** [Some Notion and Supabase MCP tools returned HTTP 403](solutions/en/P-027.md) — open.
- **P-028** [A nested env reference may have broken Notion MCP authorization](solutions/en/P-028.md) — open.
- **P-029** [Google Workspace MCP was unstable after restart](solutions/en/P-029.md) — verified.
- **P-030** [The first attempt to bind Workspace MCP to localhost stopped the service](solutions/en/P-030.md) — verified.
- **P-031** [Two Google Drive accounts made the authorization plan ambiguous](solutions/en/P-031.md) — verified.
- **P-032** [Cloudflare and Netlify access were not equivalent](solutions/en/P-032.md) — partially verified.
- **P-033** [A secondary Hermes profile did not have its own Canva OAuth state](solutions/en/P-033.md) — open.
- **P-034** [The public MCP gateway exposed a wider administrative surface than intended](solutions/en/P-034.md) — partially verified.
- **P-035** [Secrets were present in configuration and process arguments](solutions/en/P-035.md) — verified.
- **P-036** [External-access documentation diverged from live configuration](solutions/en/P-036.md) — verified.
- **P-037** [SSH file sync failed with rc=-13 while hiding the original tar error](solutions/en/P-037.md) — verified.

## Inter-agent handoffs and Telegram

- **P-038** [Hermes → OpenClaw handoff could lose the result when the runner failed](solutions/en/P-038.md) — partially verified.
- **P-039** [OpenClaw results were written to the wrong place and parsed with the wrong JSON path](solutions/en/P-039.md) — verified.
- **P-040** [A systemd watcher could select an old OpenClaw binary through PATH](solutions/en/P-040.md) — verified.
- **P-041** [Inter-agent handoff lost acknowledgement or duplicated work](solutions/en/P-041.md) — verified.
- **P-042** [Agent promised work without evidence](solutions/en/P-042.md) — verified.
- **P-043** [OpenClaw stayed silent in a Telegram group because of `NO_REPLY`](solutions/en/P-043.md) — partially verified.
- **P-044** [Telegram for macOS did not support OpenClaw rich replies](solutions/en/P-044.md) — partially verified.
- **P-045** [Telegram progress card rendered as an unsupported message](solutions/en/P-045.md) — partially verified.
- **P-046** [A Telegram topic kept stale message-tool context](solutions/en/P-046.md) — partially verified.
- **P-047** [Telegram formatting required repairing both agents](solutions/en/P-047.md) — verified.
- **P-048** [Seeker digest ran under system Python without a dependency](solutions/en/P-048.md) — partially verified.
- **P-049** [Watcher picked up service files together with tasks](solutions/en/P-049.md) — open.

## iMac and desktop applications

- **P-050** [ARM64 Hermes Desktop did not run on an Intel iMac](solutions/en/P-050.md) — verified.
- **P-051** [Hermes Desktop lost a healthy VPS because the local tunnel was stale](solutions/en/P-051.md) — verified.
- **P-052** [Desktop 401 was an expired Codex OAuth credential on the VPS](solutions/en/P-052.md) — verified.
- **P-053** [A root-owned npm cache broke the Intel Hermes Desktop update](solutions/en/P-053.md) — verified.
- **P-054** [OpenClaw Desktop repeated a stale `Approve Mac` request](solutions/en/P-054.md) — verified.
- **P-055** [An autossh monitor port was mistaken for a broken reverse SSH route](solutions/en/P-055.md) — partially verified.
- **P-056** [Proxy routing was configured, but the sing-box LaunchAgent was not loaded](solutions/en/P-056.md) — partially verified.
- **P-057** [The saved proxy upstream was stale and stopped resolving](solutions/en/P-057.md) — partially verified.
- **P-058** [The PAC file existed, but Wi‑Fi auto-proxy was disabled](solutions/en/P-058.md) — partially verified.
- **P-059** [Chromium did not load `file://` PAC; Gemini also needed routing for static assets](solutions/en/P-059.md) — verified.
- **P-060** [NotebookLM and avatar hosts were outside the selective Google AI route](solutions/en/P-060.md) — verified.
- **P-061** [DNS stalled when AmneziaVPN and a local proxy were combined](solutions/en/P-061.md) — partially verified.
- **P-062** [A `.ru` rule sent the hosting control panel to a broken route](solutions/en/P-062.md) — verified.
- **P-063** [Server routing could not give devices their normal ISP for `.ru`](solutions/en/P-063.md) — open.
- **P-064** [Long Codex chats on the iMac stalled](solutions/en/P-064.md) — open.

## VPN and devices

- **P-065** [AmneziaWG 2 → 3 migration required separate profiles](solutions/en/P-065.md) — partially verified.
- **P-066** [A VPN handshake did not prove working traffic](solutions/en/P-066.md) — partially verified.
- **P-067** [A container name did not prove the AmneziaWG version](solutions/en/P-067.md) — verified.
- **P-068** [Old and new VPN containers confused active profiles](solutions/en/P-068.md) — partially verified.
- **P-069** [VPN peers had to be recovered after migration](solutions/en/P-069.md) — partially verified.
- **P-070** [The German VPS did not open NotebookLM](solutions/en/P-070.md) — open.
- **P-071** [Phone Google AI required a separate proxy exit](solutions/en/P-071.md) — partially verified.

## Lenovo, memory and workflow

- **P-072** [Kaspersky TLS inspection broke Grok Bot on Lenovo](solutions/en/P-072.md) — partially verified.
- **P-073** [A live Hermes backend did not prove Windows Desktop was working](solutions/en/P-073.md) — partially verified.
- **P-074** [A live OpenClaw gateway did not prove the Windows panel worked](solutions/en/P-074.md) — open.
- **P-075** [Canon and live agent versions diverged](solutions/en/P-075.md) — partially verified.
- **P-076** [The Drive mirror created duplicates and stale state](solutions/en/P-076.md) — verified.
- **P-077** [Large skills transferred worse between agents](solutions/en/P-077.md) — partially verified.
- **P-078** [Honcho promoted temporary tasks into the user profile](solutions/en/P-078.md) — verified.

## VPS provisioning and early operation

- **P-079** [VPS activation was delayed after payment](solutions/en/P-079.md) — open.
- **P-080** [The first web panel had to be separately protected](solutions/en/P-080.md) — verified.
- **P-081** [A panel password entered in the terminal could remain in shell history](solutions/en/P-081.md) — open.
- **P-082** [OpenClaw and Hermes initially could not run required administrative commands](solutions/en/P-082.md) — partially verified.
- **P-083** [The first Hermes check was interrupted by a gateway restart](solutions/en/P-083.md) — partially verified.
- **P-084** [The initial Hermes fallback to Gemini did not work as expected](solutions/en/P-084.md) — partially verified.
- **P-085** [Google Workspace OAuth and Drive/Docs permissions required retries](solutions/en/P-085.md) — partially verified.
- **P-086** [OpenClaw entered a `pairing required` loop and did not answer in Telegram](solutions/en/P-086.md) — open.

## How to contribute

Found a similar case, counterexample or missing proof? Open a [Discussion](https://github.com/gorchakovve/hermes-agent-experience/discussions) for questions or an [Issue](https://github.com/gorchakovve/hermes-agent-experience/issues) for corrections. Mention the P-ID, version, sanitized symptoms, what you tried and the check you ran. Never post credentials, personal identifiers, private addresses or full configuration/logs.
