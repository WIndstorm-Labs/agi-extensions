# Exp 4: Attention Head Throughput Decomposition

**Paper 7, Experiment 4**

---

## Research Question

A transformer with 12 heads processes ~4.4 BPT aggregate. Does each head resolve ~4 bits individually (parallel serial decoders), or do some specialize (8+ bits) while others are redundant (<3 bits)?

## Hypotheses

**H₁ (Parallel Serial Decoders):** Each head resolves ~3–5 bits. Model aggregates across heads.

**H₂ (Specialized Heads):** Bimodal distribution — some high-throughput, some low-throughput.

## Method

Instrument Pythia-410M (12 layers × 16 heads = 192 heads):

1. Forward pass with hooks on every attention head
2. Compute I(X_t; Y_head_t | context) per head
3. Use InfoNCE bound or binned MI estimation
4. Aggregate across 10K WikiText-2 sequences

## Head Taxonomy

- **Basin heads:** 3–6 bits
- **Precision heads:** >6 bits
- **Redundancy heads:** <3 bits

## Scaling Question

Repeat for Pythia-70M, 1B, 1.4B. Does basin-head proportion change with scale?

## Output

- `results/exp5_head_mi.csv` (per-head mutual information)
- `results/exp5_head_taxonomy.csv` (classification)
- Distribution plots
- Scaling analysis

## Estimated Compute

8–16 hours on RTX 5090 (forward passes with MI estimation)
