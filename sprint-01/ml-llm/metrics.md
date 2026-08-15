# ML/LLM — Metrics

## Day 1 baseline

- Date: 2026-08-13
- Duration: 66 minutes
- Mode: manual baseline without code and without PASS/FAIL

## Confusion matrix exercise

The exercise contained 100 objects. The final manually corrected counts were:

|  | Predicted positive | Predicted negative |
|---|---:|---:|
| Actual positive | TP = 6 | FN = 4 |
| Actual negative | FP = 2 | TN = 88 |

The initial value `TN = 92` was incorrect and was corrected to 88 after checking that all four cells sum to 100.

## Manual verification

- Precision: `6 / (6 + 2) = 0.75`.
- Recall: `6 / (6 + 4) = 0.60`.
- F1 was not calculated during the baseline.

Interpretation recovered during the session:

- Precision denominator = all predicted positives.
- Recall denominator = all actual positives.
- When false negatives are expensive, recall is usually a primary metric, but the final choice must account for the costs of both error classes.

## Other manual results

- `E[X] = 0·0.5 + 1·0.3 + 2·0.2 = 0.7`.
- `Var(X) = 0.61`; the formula was applied, but the verbal interpretation of variance was not reproduced.
- `(32, 10) @ (10, 4) → (32, 4)`.
- The result of `X @ W + b` was identified as `(32, 4)`.
- A NumPy array can be doubled through element-wise multiplication by a scalar.

## Errors and gaps

- Euclidean norm was not recognized as vector length.
- Dot product was computed with an incorrect expression and signs were not preserved.
- Cosine similarity was not calculated.
- A one-dimensional array was written as `(1, 3)` instead of `(3,)`.
- Broadcasting was initially applied only to the first row.
- PyTorch, autograd, training loop, train/validation/test, baseline, overfitting and leakage were not known.
- Repeating the same deterministic model run was incorrectly expected to fix missed positives.
- The number of operations was incorrectly treated as a direct cause of worse model error rates.

## Evidence boundary

No executable ML code, dataset, seed, split or experiment was created on Day 1. These results are manual baseline calculations, not acceptance evidence for the required training loop or controlled experiment.
