# Paper 7: AGI Extensions of the Throughput Basin Framework

**Full title:** "Does the Basin Live in the Data or the Architecture? AGI-Directed Extensions of the Throughput Basin Framework"

**Status:** In Progress (April 2026)  
**Principal Investigator:** Grant Lavell Whitmer III  
**Infrastructure:** RTX 5090 (32GB VRAM), Hermes OC1 Autonomous Agent

---

## Research Question

Paper 6 showed AI converges on ~4.4 bits/token through inheritance from biological training data. But a critical alternative remains untested: **maybe transformer architecture itself has an intrinsic throughput preference near τ**, independent of training data.

If the basin is **architectural** (not inherited), AGI must scale by parallelizing attention heads, not by increasing per-head throughput.

---

## Hypotheses

**H₁ (Inherited Constraint — data-driven):** A transformer trained on high-entropy synthetic data (8–12 bits) will achieve BPT matching the training data, NOT the biological basin.

**H₀ (Architectural Constraint):** Regardless of training data, transformers compress toward ~4 bits per step due to attention bottlenecks.

---

## Six Experiments

### Exp 1: Synthetic Training Baseline
Train GPT-2-small on 5 synthetic corpora (2–12 bits/event).
- **Falsifies H₁ if:** SYN-8 model shows BPT < 6 on SYN-8
- **Falsifies H₀ if:** SYN-8 model shows BPT > 7 on SYN-8
- **Status:** Ready | **Compute:** 8–12 hours

### Exp 2: Quantization Cliff
Determine minimum weight precision for basin-level BPT.
- Tests: FP16, INT8, INT4, INT3, INT2, INT1
- **Deliverable:** AGI hardware spec — bits-per-joule frontier
- **Status:** Ready | **Compute:** 6–10 hours

### Exp 3: Recurrent vs Transformer
Compare BPT variance between transformers and state-space models (Mamba, RWKV).
- If serial models show tighter clustering → architecture constrains
- **Status:** Ready | **Compute:** 4–8 hours

### Exp 4: Attention Head MI Decomposition
Measure per-head mutual information in Pythia-410M (192 heads).
- If each head resolves ~4 bits → parallel serial decoders
- **Status:** Ready | **Compute:** 8–16 hours

### Exp 5: Agentic Loop Throughput
Measure bits-per-decision in ReAct-style agents.
- Tasks: 20 Questions, Sudoku, Mastermind
- If ~4 bits/step → planning depth = N/4 steps for N-bit problems
- **Status:** Ready | **Compute:** 2–4 hours + API

### Exp 6: Energy-Optimal Inference Survey
Map thermodynamic efficiency landscape of RTX 5090.
- Compute φ = E_measured / E_Landauer for each config
- **Deliverable:** Thermodynamic roadmap for AGI chips
- **Status:** Ready | **Compute:** 4–6 hours

---

## Execution Priority

| Order | Experiment | Rationale |
|-------|-----------|-----------|
| 1 | Exp 3 (Recurrent vs Transformer) | Lowest risk — pre-trained models only |
| 2 | Exp 2 (Quantization Cliff) | Builds hardware context |
| 3 | Exp 1 (Synthetic Training) | Highest value — resolves core question |
| 4 | Exp 6 (Energy Survey) | Baseline for comparison |
| 5 | Exp 4 (Attention Head MI) | Most technically complex |
| 6 | Exp 5 (Agentic Loop) | Most speculative |

**Total compute budget:** ~32–56 hours on RTX 5090

---

## Directory Structure

```
paper-07-agi-extensions/
├── README.md                          # This file
├── exp-01-synthetic-training/         # Training from scratch
├── exp-02-quantization-cliff/         # Precision sweep
├── exp-03-recurrent-vs-transformer/   # Architecture comparison
├── exp-04-attention-head-mi/          # Per-head decomposition
├── exp-05-agentic-loop/               # Agent reasoning
└── exp-06-energy-survey/              # Thermodynamic efficiency
```

---

## Citation

```bibtex
@article{whitmer2026agi,
  title={AGI Extensions of the Throughput Basin Framework},
  author={Whitmer, Grant Lavell III},
  journal={Windstorm Institute},
  year={2026}
}
```

---

*This paper tests the limits of the inherited constraint hypothesis. If H₀ holds, AGI architecture must fundamentally differ from current transformers.*
