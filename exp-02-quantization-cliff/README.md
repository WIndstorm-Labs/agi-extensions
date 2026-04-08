# Exp 2: The Quantization Cliff

**Paper 7, Experiment 2**

---

## Research Question

At what weight precision does a transformer lose the ability to maintain basin-level throughput (~4.4 BPT)? The cliff location reveals minimum information-carrying capacity for AGI hardware.

## Hypotheses

**H₁:** Cliff occurs at ~4 bits per weight. Below INT4, BPT degrades sharply.

**H₂:** Cliff occurs at ~2 bits per weight. Basin structure is more compressible.

## Models

- Pythia family: 70M, 160M, 410M, 1B, 1.4B
- GPT-2 family: base, medium, large (cross-validation)

## Quantization Levels

1. FP16 (baseline)
2. INT8 (bitsandbytes)
3. INT4 (bitsandbytes nf4)
4. INT4-GPTQ (if available)
5. INT3 (custom)
6. INT2 (custom)
7. INT1 (binary)

## Measurements

- BPT/BPB on WikiText-2
- Structural bonus (original vs fully shuffled)
- Energy per token (nvidia-smi)
- Bits-per-joule efficiency

## Key Deliverable

**AGI Hardware Spec Plot:** Bits-of-intelligence per joule vs precision, with basin threshold marked. The Pareto frontier for AGI inference chips.

## Predicted Cliff Location

| Model | Predicted Cliff | Structural Bonus Degradation |
|-------|-----------------|------------------------------|
| Pythia-410M | INT3–INT4 | Syntax degrades before raw BPT |

## Output

- `results/exp2_quantization_cliff.csv`
- Cliff plot (primary result)
- Efficiency frontier
- Pareto-optimal configurations

## Estimated Compute

6–10 hours on RTX 5090
