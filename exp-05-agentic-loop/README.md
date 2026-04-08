# Exp 5: The Agentic Loop Throughput

**Paper 7, Experiment 5**

---

## Research Question

When an LLM operates as an agent (observe → think → act), how many bits of decision-relevant information does it resolve per step? Is agentic reasoning constrained by τ ≈ 4.16?

## Hypotheses

**H₁:** Agent resolves ~4 bits per reasoning step. Performance scales with number of steps.

**H₀:** Agentic reasoning is not serial — each step involves parallel attention over full context.

## Tasks with Known Decision Information

| Task | Decisions | Total bits | Predicted steps |
|------|----------|------------|-----------------|
| 20 Questions | 20 binary | 20 bits | ~5 steps |
| Sudoku 4×4 | 12 cells × 2 bits | 24 bits | ~6 steps |
| Logic grid 3×3 | 9 cells × ~3 bits | 27 bits | ~7 steps |
| Sudoku 9×9 | 81 × ~3.2 bits | ~260 bits | ~65 steps |
| Mastermind | ~10 bits | 10 bits | ~3 steps |

## Method

ReAct-style agent on each task:
1. Count reasoning steps (each "Thought:" block)
2. After each step: how many bits of solution resolved?
3. Slope = per-step throughput
4. Compare to τ = 4.16

## Models

- Local: Pythia-410M, Pythia-1.4B
- API: Claude Sonnet (comparison)

## Output

- `results/exp6_bits_per_step.csv`
- Cumulative bits resolved plots
- Per-step throughput by task
- Scaling comparison (model size vs throughput)

## Estimated Compute

2–4 hours on RTX 5090 + API costs
