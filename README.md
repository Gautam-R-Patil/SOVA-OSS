<p align="center">
  <img src="./assets/sova-owl-logo.svg" width="170" alt="SOVA owl logo" />
</p>

<h1 align="center">S.O.V.A.</h1>

<p align="center">
  <strong>The open-source portable record for AI behavior.</strong>
</p>

<p align="center">
  Record what happened. Package the conditions. Replay the evidence.<br/>
  Reproduce the behavior. Compare systems. Share research others can inspect.
</p>

<p align="center">
  <a href="https://github.com/TRUSCOR/SOVA-OSS"><img alt="Active development" src="https://img.shields.io/badge/ACTIVE%20DEVELOPMENT-TRUSCOR%2FSOVA--OSS-0B8793?style=for-the-badge"></a>
  <img alt="This repo" src="https://img.shields.io/badge/THIS%20REPO-v1%20PROTOTYPE%2C%20FROZEN-6554C0?style=for-the-badge">
  <a href="./LICENSE"><img alt="Apache License 2.0" src="https://img.shields.io/badge/LICENSE-Apache--2.0-D22128?style=for-the-badge"></a>
  <img alt="Status" src="https://img.shields.io/badge/STATUS-PRE--ALPHA-FFB000?style=for-the-badge">
</p>

---

> ### This is the v1 prototype — the original build
>
> This repository is the **first version of SOVA OSS**, preserved with its full
> 108-commit history exactly as it was first written.
>
> **All active development has moved to [github.com/TRUSCOR/SOVA-OSS](https://github.com/TRUSCOR/SOVA-OSS).**
> Issues, pull requests and releases belong there. This copy stays as the record
> of where the project started.
>
> **This copy is frozen and no longer updated.** Gautam R. Patil started SOVA OSS
> on 28 July 2026. Papers built on it are released at
> [TRUSCOR/research](https://github.com/TRUSCOR/research), and working
> drafts are kept at [Gautam-R-Patil/research-papers](https://github.com/Gautam-R-Patil/research-papers).

---

## The problem

An AI agent tells you what it did. A screenshot shows you what a dashboard
claimed. Neither is evidence.

When an autonomous system causes harm, the investigation runs into the same
wall every time: **nobody can reproduce what actually happened.** The logs are
unsigned. The environment is gone. The model has been updated. The finding
cannot be checked by anyone who was not in the room.

Aviation solved this with the flight recorder. Consumer credit solved it with
the bureau. Autonomous AI has solved it with neither.

## What SOVA does

SOVA writes what an agent **was shown**, what it **did**, and what **actually
changed** into `.sova` — a signed, tamper-evident, portable evidence format.

The point is not the logging. The point is that a third party can take the file,
replay it, and reach their own conclusion. **Evidence instead of trust.**

> *Sova* is the Serbian and Russian word for owl.

## Try it in one minute

No model, no API key, no network:

```bash
git clone https://github.com/TRUSCOR/SOVA-OSS
cd SOVA-OSS
uv sync --locked
uv run sova --version
uv run sova demo sleeper
```

`sova demo sleeper` plants a dormant behaviour in a test agent, finds it, and
seals the result as a signed `.sova-trace` and `.sova` capsule. Verified on
Windows, macOS and Linux, CPython 3.11–3.14.

```bash
uv run sova verify   <capsule>   # check the signature and the chain
uv run sova replay   <capsule>   # re-run the recorded conditions
```

## How it is built

| | |
|---|---|
| **Local first** | No SOVA-hosted service required. Telemetry off by default. |
| **Bring your own model** | No provider lock-in. |
| **Deterministic** | Seeded runs, pinned schemas, provenance-controlled goldens, performance budgets. |
| **Fail-closed** | Extensions and providers refuse rather than guess. |
| **Signed** | SHA-256 fingerprints, UUIDv7 identifiers, optional Ed25519 signing. |
| **Checked** | Strict typing, branch coverage, fault injection, crash recovery, CodeQL, secret scanning, dependency audit. |

## What it will not claim

> **A short test cannot prove an agent safe.**

SOVA OSS results are self-assessments. They are a record of what happened under
stated conditions — not a certificate, and not a guarantee about conditions
nobody tested. Only TRUSCOR issues the independent TRUSCOR Rating, and that is
deliberately a separate thing from this toolkit.

This repository is **pre-alpha**. Live Firecracker isolation, blinded
multi-provider field results, a public Registry deployment, independent review
and publication all remain open gates. That list is published rather than
hidden on purpose.

## Where it fits

SOVA OSS is the open layer. The closed layers are built on the same `.sova`
format:

| Layer | Role | Access |
|---|---|---|
| **SOVA OSS** | Map, test, record, replay, investigate | Open source, Apache-2.0 |
| **[SOVA Engine](https://github.com/TRUSCOR/SOVA-Engine)** | Attacks and stress-tests AI products into `.sova` evidence | Rating team, licensed firms |
| **[SOVA Black Box](https://github.com/TRUSCOR/SOVA-Blackbox)** | 24×7 production recorder | Deployments, OEM partners |
| **[O.W.L](https://github.com/TRUSCOR/O.W.L)** | Checks claims against real effects | Internal, licensed measurers |
| **[TAFAAR](https://github.com/TRUSCOR/TAFAAR)** | Grades evidence into the TRUSCOR Rating | TRUSCOR only, never licensed |

## Contribute

Not here — this is a frozen v1. Everything happens at
**[TRUSCOR/SOVA-OSS](https://github.com/TRUSCOR/SOVA-OSS)**.

---

<p align="center">
  Apache-2.0. Built by <a href="https://github.com/Gautam-R-Patil">Gautam Patil</a> and <a href="https://truscor.org">TRUSCOR</a>.<br/>
  <em>Where intelligence meets accountability.</em>
</p>
