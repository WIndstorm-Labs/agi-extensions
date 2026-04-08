# Exp 3: Recurrent vs Transformer Throughput

**Paper 7, Experiment 3**

---

## Research Question

Does truly serial architecture (Mamba, RWKV) show tighter basin convergence than parallel attention transformers? If the throughput basin constrains serial decoding, serial architectures should hit a harder ceiling.

## Hypotheses

**H₁:** Mamba/RWKV show BPT closer to τ = 4.16 (tighter variance) than transformers.

**H₀:** No difference — basin is property of training data, not architecture.

## Model Pairs

| Pair | Transformer | Serial Model | Params |
|------|------------|--------------|--------|
| A | Pythia-160M | Mamba-130M | ~150M |
| B | Pythia-410M | Mamba-370M | ~400M |
| C | GPT-2-medium | RWKV-430M | ~400M |
| D | Pythia-1.4B | Mamba-1.4B | ~1.4B |

## Measurements

1. BPT/BPB on WikiText-2
2. Full shuffling cascade (5 levels)
3. Structural bonus (ΔBPT)
4. Energy per token
5. Seven-corpus battery (NL, code, DNA, synthetic, math, random, shuffled)

## Analysis

- Welch's t-test: Mean BPT difference
- F-test: BPT variance comparison (tighter variance = tighter constraint)
- Mann-Whitney U: Structural bonus distributions
- Effect sizes (Cohen's d)

## Output

- `results/exp3_bpt_comparison.csv`
- `results/exp3_shuffling_cascade.csv`
- `results/exp3_energy.csv`
- `results/exp3_seven_corpus.csv`
- Plots in `results/exp3_plots/`

## Estimated Compute

4–8 hours on RTX 5090 (pre-trained models only)
