# Adding these results to the Advassess repository

A suggested location is `docs/evaluations/november-2026/`:

```text
docs/
└── evaluations/
    └── november-2026/
        ├── README.md
        ├── llm-qwen25-14b/
        ├── image-mnist/
        └── image-vit-imagenet/
```

Copy the contents of this package into that directory. Then add a short section to the repository's main README:

```markdown
## Evaluation Results

See [November 2026 evaluation results](docs/evaluations/november-2026/README.md) for
LLM security testing (Garak/PyRIT) and adversarial robustness evaluations (ART)
on MNIST and ViT-Base/ImageNet.
```

Review the reports and images before publishing. The included JSON reports have local paths and the Ollama host address redacted. Do not publish unredacted logs, transcripts, API keys, private model files, or datasets. The results are experimental and should be presented with the sample counts, attack parameters, and limitations documented alongside them.

Suggested commit:

```bash
git add docs/evaluations/november-2026 README.md
git commit -m "docs: add November 2026 evaluation results"
git push
```
