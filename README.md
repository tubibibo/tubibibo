<div align="center">

### Zzup012 · YangoSec

Local-first security tooling · vulnerability research · CTF

<sub>No account, no cloud service, no telemetry.</sub>

[![ReachScope](https://img.shields.io/github/v/release/tubibibo/reachscope-workbench?label=reachscope&color=2e7d5b&logo=python&logoColor=white)](https://github.com/tubibibo/reachscope-workbench)
[![CI](https://github.com/tubibibo/reachscope-workbench/actions/workflows/ci.yml/badge.svg)](https://github.com/tubibibo/reachscope-workbench/actions/workflows/ci.yml)
[![LRC Toolkit](https://img.shields.io/github/v/release/tubibibo/lrc-toolkit?label=lrc-toolkit&color=3178c6)](https://github.com/tubibibo/lrc-toolkit)
[![CodeSheaf](https://img.shields.io/badge/codesheaf-v1.1.0-3178c6)](https://github.com/tubibibo/codesheaf)

</div>

---

## What I'm building

**[ReachScope Workbench](https://github.com/tubibibo/reachscope-workbench)** — a local workbench that turns a finding into a closed loop: collect → harden → re-test → compare → close. Android, web, cloud config and host share one job queue, one evidence model and one SQLite workspace. It listens on loopback only, and the UI keeps "observations", "candidate paths" and "confirmed findings" apart — heuristics don't get promoted to conclusions.

**[LRC Toolkit](https://github.com/tubibibo/lrc-toolkit)** / **[CodeSheaf](https://github.com/tubibibo/codesheaf)** — two VS Code extensions: one edits and checks synced lyrics, the other bundles files, selections and their import graph into a single context for a model.

## Vulnerability research

**2 original high-severity vulnerabilities accepted by CNVD** (2026.05, 2026.09) — found, verified and reported end to end, covering a telemedicine platform and a network storage device.

**Vendor SRC / crowdsourced programs** — 20+ reports submitted through Vulbox, Butian and in-house SRC programs across mobility, social, healthcare and gaming; 11 confirmed. A few of them:

- **Critical** · weak callback validation lets a WeChat OAuth code be handed to a third party, taking over the account (mobility platform)
- **High** · enumerable `t_id` reads other verified users' real phone numbers (logistics platform community)
- **High** · the server trusts `user_id` in the request body, allowing bulk reads of any user's contacts (logistics platform app)
- **High** · the SSO redirect allowlist includes a domain its owner had lost control of, so session tickets can be delivered there (short-video platform account center)
- **Medium** · DOM XSS through an unauthenticated `gourl` parameter (video platform passport)
- **Medium** · a semicolon bypasses nginx path rules, allowing anonymous DWR method calls (healthcare platform)

## Competitions

| Event | Result |
| --- | --- |
| ISCC 2026 · national finals | Second Prize |
| "Yuwang Cup" Cybersecurity Competition (10th edition, Henan) | First Prize |
| RAICOM 2026 · Fujian | Second Prize |
| Software System Security Competition · East China | Third Prize |

## Open source

Fixes merged into [Frida](https://github.com/frida) (frida-gum, frida-core, frida-tools) and [projectdiscovery/naabu](https://github.com/projectdiscovery/naabu): x86 relocation and Stalker edge cases, an agent load fallback, `frida-ps` enumeration breaking when icons fail to load, and an explicit `-rate` being overridden on connect-scan fallback. Six more PRs are in review at semgrep, impacket, APKiD and others.

## What I care about

Evidence that survives the conversation — something you can point at later and say "there". And saying **"not proven"** when it isn't. Next: a red/blue verification layer on top of ReachScope — authorized, non-destructive, but able to actually prove impact, with the evidence travelling alongside the conclusion. I'll write about it when it's real.

---

<sub>Open an issue if you want to talk.</sub>
