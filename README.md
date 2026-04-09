# Paper 7: The Throughput Basin Origin — Experiments & Code

> **Note:** This is the Windstorm Labs mirror. The canonical repository &mdash; with the formal manuscript, internal adversarial review, complete CSVs, plots, and the Paper 7.1 tracking issue &mdash; is at **[sneakyfree/agi-extensions](https://github.com/sneakyfree/agi-extensions)**.

**Status:** ✅ Experiments complete (April 2026). Formal draft published with internal adversarial review attached. Paper 7.1 follow-up scoped.

---

## Read this first

The four orthogonal experiments here (synthetic-corpus training, quantization cliff, transformer-vs-state-space architecture comparison, and RTX 5090 wall-power thermodynamic survey) are complete. The internal adversarial review of the results identifies four blocking items that constrain how strongly the headline can be read.

> **Defensible claim:** *At 92M parameters, on Markov synthetic data with corpus-specific BPE tokenizers, training-data token entropy is the dominant predictor of achieved BPT, and we find no positive evidence of a transformer-specific ~4-bit ceiling in this regime.*

The full review and the Paper 7.1 re-runs are tracked at:

- **Adversarial review:** [sneakyfree/agi-extensions/review/adversarial_review.md](https://github.com/sneakyfree/agi-extensions/blob/main/review/adversarial_review.md)
- **Paper 7.1 tracking issue:** [sneakyfree/agi-extensions#1](https://github.com/sneakyfree/agi-extensions/issues/1)

---

## What lives here

This repository contains the experiment protocols for the four core Paper 7 experiments plus two scoping experiments. The full results CSVs, plots, and the formal manuscript live in the canonical repo.

```
exp-01-synthetic-training      Experiment 1: SYN-{2,4,8,12} GPT-2 training
exp-02-quantization-cliff      Experiment 2: bitsandbytes RTN sweep
exp-03-recurrent-vs-transformer Experiment 3: Pythia vs Mamba on 7 corpora
exp-04-attention-head-mi       (scoping)
exp-05-agentic-loop            (scoping)
exp-06-energy-survey           Experiment 6: RTX 5090 wall-power φ
```

## Reproducibility

**Hardware:** RTX 5090 (32GB VRAM)
**Runtime:** ~14.5 hours for the four core experiments (autonomous overnight run)
**Python:** 3.11+
**Key deps:** `torch`, `transformers`, `datasets`, `mamba-ssm`, `bitsandbytes`

See individual experiment READMEs for detailed setup. Vision Basin Phase 1 (Paper 8 prelude) lives in the canonical repo at `exp-8/`.

---

## Series Index

| # | Paper | Status |
|---|-------|--------|
| 1 | [The Fons Constraint](https://github.com/Windstorm-Labs/fons-constraint) | ✅ Published — [DOI 10.5281/zenodo.19274048](https://doi.org/10.5281/zenodo.19274048) |
| 2 | [The Receiver-Limited Floor](https://github.com/Windstorm-Labs/receiver-limited-floor) | ✅ Published — [DOI 10.5281/zenodo.19322973](https://doi.org/10.5281/zenodo.19322973) |
| 3 | [The Throughput Basin](https://github.com/Windstorm-Labs/throughput-basin) | ✅ Published — [DOI 10.5281/zenodo.19323194](https://doi.org/10.5281/zenodo.19323194) |
| 4 | [The Serial Decoding Basin τ](https://github.com/Windstorm-Labs/serial-decoding-basin) | ✅ Published — [DOI 10.5281/zenodo.19323423](https://doi.org/10.5281/zenodo.19323423) |
| 5 | [The Dissipative Decoder](https://github.com/Windstorm-Labs/dissipative-decoder) | ✅ Published — [DOI 10.5281/zenodo.19433048](https://doi.org/10.5281/zenodo.19433048) |
| 6 | [The Inherited Constraint](https://github.com/Windstorm-Labs/inherited-constraint) | ✅ Published — [DOI 10.5281/zenodo.19432911](https://doi.org/10.5281/zenodo.19432911) |
| 7 | [The Throughput Basin Origin](https://github.com/sneakyfree/agi-extensions) | 🟡 Preprint — Zenodo deposit pending Paper 7.1 |

---

*License: MIT for code, CC BY 4.0 for data*
