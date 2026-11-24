## The champion
I picked `logreg` (`f1: 0.495`, `auc: 0.798`, `p95_latency_ms: 3.13`, MLflow run ID `d2d71128375147b3a094994803a7e1f2`) because it had the best F1 and ROC-AUC scores while staying well inside the 25.0 ms p95 latency budget.

## My promotion rules
- Latency budget (p95): 25.0 ms, because real-time inference needs low latency.
- Minimum gain to replace the champion (F1 points): 0.005, because a new model should beat the champion by a real margin rather than minor noise.

## What I would check next
I would check smaller customer slices, tune the classification threshold for class imbalance, and monitor data or concept drift in production.
