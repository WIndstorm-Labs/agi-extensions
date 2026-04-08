# Exp 1: Synthetic Training Baseline

**Paper 7, Experiment 1**

---

## Research Question

Does the throughput basin live in the training data or the transformer architecture? Training on high-entropy synthetic data tests this directly.

## Hypotheses

**H₁ (Inherited Constraint):** Model trained on SYN-8 (8 bits/event) achieves BPT ≈ 8. Basin is data-driven.

**H₀ (Architectural Constraint):** SYN-8 model shows BPT near τ ≈ 4.4 regardless of training data. Basin is architectural.

## Synthetic Corpora

| Corpus | Target H | Structure |
|--------|----------|-----------|
| SYN-2 | ~2 bits | 4-symbol Markov-1 |
| SYN-4 | ~4 bits | 16-symbol Markov-2 |
| SYN-8 | ~8 bits | 256-symbol Markov-3 |
| SYN-12 | ~12 bits | 4096-symbol minimal dependency |
| SYN-MIX | Mixed | Interleaved blocks |

Each: 100M tokens, custom BPE tokenizer (vocab=8192)

## Training

- Architecture: GPT-2-small (124M params)
- Steps: 50K
- Batch: 32, seq: 512
- LR: 3e-4, cosine schedule
- Seed: 42

## Critical Tests

1. **Self-evaluation:** Does SYN-8 achieve BPT ≈ 8 on SYN-8?
2. **Cross-corpus:** BPT on all 5 synthetic corpora
3. **Biological transfer:** BPT on WikiText-2
4. **Internal compression:** Layer-wise entropy in SYN-8 model
5. **Learning dynamics:** Does SYN-4 converge faster on WikiText-2?

## Falsification

- H₁ falsified if SYN-8 shows BPT < 6 on SYN-8
- H₀ falsified if SYN-8 shows BPT > 7 on SYN-8

## Output

- `results/exp1_self_eval.csv`
- `results/exp1_cross_corpus.csv`
- `results/exp1_layer_entropy.csv`
- `results/exp1_learning_dynamics.csv`

## Estimated Compute

8–12 hours on RTX 5090
