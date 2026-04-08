# Exp 6: Energy-Optimal Inference Hardware Survey

**Paper 7, Experiment 6**

---

## Research Question

The ribosome operates at φ ≈ 1.02 of thermodynamic minimum. Silicon operates at ~10⁹× Landauer. Where does each configuration sit, and what's the theoretical minimum?

## Method

Benchmark Pythia models across configurations:

1. FP32, FP16, INT8, INT4 inference
2. FP16 + torch.compile
3. Batched inference (1, 8, 32, 128)

## Measurements

- Power: nvidia-smi polling (10ms intervals)
- Temperature: GPU die temp
- Wall-clock time
- Tokens processed

## Metrics

- Energy per token (J)
- Bits per joule
- φ = E_measured / E_Landauer
- log₁₀(φ) for ribosome comparison

## Deliverable

**Thermodynamic Roadmap for AGI Inference:**
1. Current state (RTX 5090 configurations)
2. Theoretical floor (Landauer × digital overhead)
3. Gap remaining (OOMs of improvement)
4. Projected timeline

## Comparison

| System | φ | log₁₀(φ) |
|--------|---|----------|
| Ribosome | 1.02 | 0.009 |
| RTX 5090 (FP16) | ~10⁹ | ~9 |
| RTX 5090 (INT4) | ~? | ~? |

## Output

- `results/exp7_energy_survey.csv`
- φ landscape plot
- Efficiency frontier
- Gap decomposition
- `results/exp7_thermodynamic_roadmap.txt`

## Estimated Compute

4–6 hours on RTX 5090
