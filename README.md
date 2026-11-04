<div align="center">

<img src="media/logo.svg" alt="VisionDiff" width="120">

# VisionDiff

### Did the new vision model actually get better? Get an answer, not an impression.

**Local, reproducible regression testing for vision-language models, on your own machine.**

![Runs locally](https://img.shields.io/badge/runs-100%25%20local-2ea44f?style=for-the-badge)
![LM Studio](https://img.shields.io/badge/inference-LM%20Studio-7c5cff?style=for-the-badge)
![95% CI](https://img.shields.io/badge/verdicts-95%25%20confidence%20interval-e5484d?style=for-the-badge)
![Proprietary](https://img.shields.io/badge/license-proprietary-555?style=for-the-badge)

[**See it in action**](#see-it-in-action) &nbsp;·&nbsp; [**What you get**](#what-you-get) &nbsp;·&nbsp; [**Honest about its limits**](#honest-about-its-limits) &nbsp;·&nbsp; [**Get access**](#get-access)

</div>

<br>

https://github.com/user-attachments/assets/b7f5cb41-8c8d-4ffb-b9ca-19bf44d57e49

<sub align="center">The real app against a real backend, LM Studio and an RTX 4080. The inference is real and the numbers are whatever the models actually scored. Long waits are skipped or time-lapsed, and every cut says so on screen.</sub>

<br>

## Why VisionDiff

Most model comparisons are impressions: load two models, ask a few questions, form a view. VisionDiff answers a narrower question that has an answer. Given a fixed dataset, fixed decoding parameters and byte-identical inputs, **which samples did the Candidate get right that the Baseline got wrong, and which did it break?**

|  |  |
|---|---|
| ⚖️ **A verdict you can defend** | Improved, regressed or no change, with a 95% confidence interval and an exact McNemar test. |
| 🔁 **Same conditions, every time** | Both models run back to back under one lock, and every run records a fingerprint of its conditions. |
| 🏠 **Entirely on your machine** | Inference goes through LM Studio on your own GPU. Reports open offline, with no network calls of any kind. |
| 🧾 **Every sample on show** | Each image with both answers against the same ground truth, never just a final number. |

<br>

## See it in action

### 1 · Find a model that fits

Browse what's on disk or download from a curated catalog. The **Fit Estimate** scores each model against your machine first: fits, tight, CPU offload or too big.

https://github.com/user-attachments/assets/1ac7469e-a33c-4b31-a86a-78ddbc75dfa2

<br>

### 2 · Pick a dataset

Four datasets and 460 samples, generated from a fixed seed so ground truth is exact by construction. Every image sits beside its answer. You can import your own too, and any invalid row is reported by line number before anything is written.

https://github.com/user-attachments/assets/e3f663f7-9840-4317-b55f-6343febea333

<br>

### 3 · Watch a run

One model over one dataset, streaming live: a phase stepper, a pass/fail tally, and one line per sample with the answer and its latency. The scorecard appears when it finishes.

https://github.com/user-attachments/assets/45747c95-3fcd-48ef-b350-9fbf99eee237

<br>

### 4 · Get the verdict

The **Regression Matrix** shows what was fixed against what broke, and its cells work as filters. Both scorecards sit side by side, with the difference in its own column. The video at the top of this page shows all of it.

<br>

### 5 · Keep the evidence

The report carries every sample above a full provenance block. It's a self-contained HTML file, so it still opens offline years from now, and it prints to PDF from its own toolbar. **[See an example PDF](media/sample-report.pdf)**.

https://github.com/user-attachments/assets/374c10b6-186f-43aa-8dfe-e077284d8633

<br>

## What you get

<table>
<tr>
<td width="50%" valign="top">

**🧩 Models**
- Every vision-capable model LM Studio has on disk
- Curated downloads: sixteen models across six families
- Live GPU VRAM, RAM and disk readout
- Guarded delete that shows the exact path and size first

</td>
<td width="50%" valign="top">

**🏃 Runs**
- Temperature, seed, token budget, context length and sampler set per run
- Live console with cancel that always unloads the model
- Scorecards by task type and difficulty band
- Mean score, latency, time to first token and decode rate

</td>
</tr>
<tr>
<td width="50%" valign="top">

**📊 Comparisons**
- Verdict, confidence interval and Regression Matrix
- Reuse a run you already have instead of measuring it again
- A banner offers an existing result before any GPU time is spent

</td>
<td width="50%" valign="top">

**📤 Reports and history**
- Export to self-contained HTML, JSON and CSV
- Searchable timeline of every run and comparison
- Pages, filters and single samples all have shareable URLs

</td>
</tr>
</table>

<br>

## Honest about its limits

- **Synthetic datasets are cleaner than photographs.** Absolute scores run higher than on real-world benchmarks. VisionDiff measures the *difference* between two models on identical inputs.
- **Temperature 0 is not determinism.** The same request can produce different output across runs, which is exactly why the confidence interval matters.
- **One GPU, one model at a time.** There's no multi-GPU scheduling and no tournaments across more than two models.

<br>

## Requirements

- **Windows** (setup scripts are Windows-first).
- **LM Studio** is the inference engine. Setup installs it and the rest of what the app needs.
- An **NVIDIA GPU** is recommended, since CPU-only inference is impractically slow for a full sweep. Developed against an RTX 4080 with 16 GB of VRAM.

<br>

## Get access

VisionDiff is proprietary software in **private early access**. If you'd like to try it, [**open an issue**](../../issues/new?title=Access%20request) titled *Access request* and tell me what you'd use it for.

<br>

<div align="center">
<sub>© 2026 Mashraki. All rights reserved. This repository contains only promotional material; VisionDiff's source code is not public and is not open source.</sub>
</div>
