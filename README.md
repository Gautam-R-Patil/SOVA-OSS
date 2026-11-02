<div align="center">

# SOVA OSS

**Record, replay and reproduce what AI agents actually do.**

Open source · Apache-2.0 · pre-alpha · by [TRUSCOR](https://truscor.org)

**The full project lives at [github.com/TRUSCOR/SOVA-OSS](https://github.com/TRUSCOR/SOVA-OSS).** This repository is an overview and quick start.

</div>

---

## What it is

SOVA OSS is the free, public toolkit for AI-agent security: map, test, record, replay and forensics. It writes what an agent was shown, what it did and what changed into **.sova**, a signed, tamper-evident evidence format, so a third party can check a finding instead of trusting a screenshot.

*Sova* is the Serbian and Russian word for owl.

## Try it in one minute

No model, no API key and no network needed:

```bash
git clone https://github.com/TRUSCOR/SOVA-OSS
cd SOVA-OSS
uv sync --locked
uv run sova --version
uv run sova demo sleeper
```

`sova demo sleeper` finds a planted hidden behaviour and writes a signed `.sova-trace` and `.sova` file. It's tested on Windows, macOS and Linux.

## What it won't claim

> "A short test cannot prove an agent safe."

SOVA OSS results are self-assessments. Only TRUSCOR issues the independent TRUSCOR Rating.

## Where it fits

SOVA OSS is the open layer of the SOVA stack. The closed parts are [SOVA Engine](https://github.com/TRUSCOR/SOVA-Engine), [SOVA Black Box](https://github.com/TRUSCOR/SOVA-Blackbox), [O.W.L](https://github.com/TRUSCOR/O.W.L) and [TAFAAR](https://github.com/TRUSCOR/TAFAAR).

## Contribute

Issues and pull requests go to **[TRUSCOR/SOVA-OSS](https://github.com/TRUSCOR/SOVA-OSS)**.

---

Built by [Gautam Patil](https://github.com/Gautam-R-Patil) and [TRUSCOR](https://truscor.org).
