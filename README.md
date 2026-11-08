# Advassess — Evaluation Results

This directory contains selected evaluation outputs from Advassess runs performed in November 2026. It is intended to document tool capabilities and observed results, not to claim that any evaluated model is secure or insecure in general.

## Evaluations

| Target | Evaluation | Run date (UTC) | Summary |
|---|---|---|---|
| Qwen2.5:14B (Ollama) | LLM security probes (Garak + PyRIT) | 2026-11-04 | 11 probe/strategy entries; 3 detector-reported failures |
| MNIST classifier | Adversarial robustness (ART) | 2026-11-03 | 13 attack configurations completed |
| ViT-Base-Patch16-224 | Adversarial robustness (ART) | 2026-11-06 | 28 attack configurations; some timed out or errored |

## Important interpretation notes

- These are individual runs with the exact sample counts and parameters recorded in each `report.json`. They are not standardized benchmark claims.
- Attack success rate (ASR) is calculated only over samples that were correctly classified before the attack, as indicated by the reports. Always read ASR together with the evaluated sample count and clean accuracy.
- A completed attack with a high ASR is evidence about that configuration and sample subset only. It does not establish general model vulnerability.
- A low ASR, zero ASR, timeout, or attack error is not evidence of robustness. In particular, under-configured attacks can fail to find adversarial examples.
- The JSON reports have local filesystem paths and the Ollama host address redacted.

## Directory contents

- [`llm-qwen25-14b/`](llm-qwen25-14b/) — Garak/PyRIT report, summary image, and HTML report.
- [`image-mnist/`](image-mnist/) — ART report, summary/sweep charts, and selected adversarial-example visualizations.
- [`image-vit-imagenet/`](image-vit-imagenet/) — ART report, summary chart, and selected adversarial-example visualizations.

Each subdirectory includes a machine-readable `report.json` and a human-readable `RESULTS.md`.
