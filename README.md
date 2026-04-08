# AGI Extensions

**Paper 7 Experiments & Code**

🚧 In Progress

**Paper Publication:** https://github.com/Windstorm-Institute/agi-extensions  
**Windstorm Institute:** https://windstorminstitute.org

---

## Quick Start

```bash
# Six experiments ready to run:

# Exp 3: Recurrent vs Transformer (lowest risk, 4-8 hrs)
cd exp-03-recurrent-vs-transformer
python run_experiment.py

# Exp 2: Quantization Cliff (6-10 hrs)
cd exp-02-quantization-cliff
python run_experiment.py

# Exp 1: Synthetic Training (8-12 hrs, training from scratch)
cd exp-01-synthetic-training
python run_experiment.py
```

---

## Reproducibility Info

**Hardware:** RTX 5090 (32GB VRAM) required
**Runtime:** 32-56 hours for all 6 experiments
**Python:** 3.11+
**Key deps:** torch, transformers, datasets, mamba-ssm (for Exp 3)

See individual experiment READMEs for detailed setup.

---

## Results Preview

Experiments not yet run - this is the protocol repository

---

## Series Index

| # | Paper | Status | Key Result |
|---|-------|--------|------------|
| 1 | [Fons Constraint](./fons-constraint) | 📋 Planned | 64-codon alphabet |
| 2 | [Receiver-Limited Floor](./receiver-limited-floor) | ✅ Complete | Vocab-independent BPT |
| 3 | [Throughput Basin](./throughput-basin) | 📋 Planned | 31-system convergence |
| 4 | [Dissipative Decoder](./dissipative-decoder) | 📋 Planned | Regime A/B analysis |
| 5 | [Serial Decoding Basin τ](./serial-decoding-basin) | 📋 Planned | τ = 4.16 ± 0.19 bits |
| 6 | [Inherited Constraint](./inherited-constraint) | 📋 Planned | AI inherits biology |
| 7 | [AGI Extensions](./agi-extensions) | 🚧 In Progress | Data vs architecture |

Legend: ✅ Complete | 🚧 In Progress | 📋 Planned



---

## About Windstorm-Labs

This organization contains the experimental code, data, and analysis supporting the Windstorm Institute paper series. Each repository is designed for reproducibility and extension.

**Questions?** Open an issue.  
**Want to contribute?** Fork and PR.  
**Found a bug?** Let us know.

---

*License: MIT for code, CC BY 4.0 for data*
