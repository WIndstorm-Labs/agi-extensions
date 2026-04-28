# Paper 7: The Throughput Basin Origin — Experiments & Code

**Four Orthogonal Experiments on Whether Serial Decoding Convergence Is Architectural, Thermodynamic, or Data-Driven**

[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.19498582-blue)](https://doi.org/10.5281/zenodo.19498582)
[![License: MIT](https://img.shields.io/badge/Code-MIT-green)](https://opensource.org/licenses/MIT)

---

## Canonical Repository

All code, data, results, the manuscript PDF, and the adversarial review now live at:

**→ [Windstorm-Institute/throughput-basin-origin](https://github.com/Windstorm-Institute/throughput-basin-origin)**

This Labs mirror is maintained for org-level consistency. The canonical repo above has the paper (v1.6), the internal adversarial review, the Grand Slam supplementary materials, all CSVs, paper7.1 follow-up data, and the Paper 8 preliminary scripts.

**Companion article:** [windstorminstitute.org/articles/throughput-basin-origin.html](https://windstorminstitute.org/articles/throughput-basin-origin.html) · **Zenodo (concept DOI, always-latest):** [10.5281/zenodo.19498582](https://doi.org/10.5281/zenodo.19498582) · **v1.6:** [10.5281/zenodo.19672654](https://doi.org/10.5281/zenodo.19672654)

---

## Hardware (when this paper's experiments were originally run)

- **GPU:** NVIDIA RTX 5090 (32 GB VRAM)
- **CPU:** Intel Core Ultra 9 285K (24 cores)
- **RAM:** 256 GB
- **OS:** Ubuntu 24.04, Python 3.12, PyTorch 2.11
- **Quantization:** bitsandbytes 0.49.2 (with CUDA 13.0 library path fix)

The seven-round verification journey detailed in v1.6 §1.3-3.12: ~14.5 hours autonomous Sonnet 4.5 execution (Exps 1-6), ~10 hours parallel Opus 4.6 follow-ups (B1/B4/R6/R9/stats), ~16 hours automated nohup R5 + intermediate-entropy runs, plus the Grand Slam round. Full per-round breakdown in the canonical paper's acknowledgments.

---

## The Windstorm Series

| # | Paper | DOI |
|---|-------|-----|
| 1 | [The Fons Constraint](https://github.com/Windstorm-Institute/fons-constraint) | [10.5281/zenodo.19274048](https://doi.org/10.5281/zenodo.19274048) |
| 2 | [The Receiver-Limited Floor](https://github.com/Windstorm-Institute/receiver-limited-floor) | [10.5281/zenodo.19322973](https://doi.org/10.5281/zenodo.19322973) |
| 3 | [The Throughput Basin](https://github.com/Windstorm-Institute/throughput-basin) | [10.5281/zenodo.19323194](https://doi.org/10.5281/zenodo.19323194) |
| 4 | [The Serial Decoding Basin τ](https://github.com/Windstorm-Institute/serial-decoding-basin) | [10.5281/zenodo.19323423](https://doi.org/10.5281/zenodo.19323423) |
| 5 | [The Dissipative Decoder](https://github.com/Windstorm-Institute/dissipative-decoder) | [10.5281/zenodo.19433048](https://doi.org/10.5281/zenodo.19433048) |
| 6 | [The Inherited Constraint](https://github.com/Windstorm-Institute/inherited-constraint) | [10.5281/zenodo.19432911](https://doi.org/10.5281/zenodo.19432911) |
| 7 | [The Throughput Basin Origin](https://github.com/Windstorm-Institute/throughput-basin-origin) *(this paper)* | [10.5281/zenodo.19498582](https://doi.org/10.5281/zenodo.19498582) |
| 8 | [The Vision Basin](https://github.com/Windstorm-Institute/vision-basin) | [10.5281/zenodo.19672827](https://doi.org/10.5281/zenodo.19672827) |
| 9 | [The Hardware Basin](https://github.com/Windstorm-Institute/hardware-basin) | [10.5281/zenodo.19672921](https://doi.org/10.5281/zenodo.19672921) |

**Website:** [windstorminstitute.org](https://windstorminstitute.org)

---

*Code: MIT License · Data: CC BY 4.0*
