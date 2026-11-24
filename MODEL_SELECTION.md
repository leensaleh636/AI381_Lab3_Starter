## The champion
I picked `logreg` (`f1: 0.495`, `auc: 0.798`, `p95_latency_ms: 3.13`, MLflow run ID `d2d71128375147b3a094994803a7e1f2`) because it had the best F1 and ROC-AUC scores while running well under the 25.0 ms latency limit[span_4](start_span)[span_4](end_span)[span_5](start_span)[span_5](end_span).

## My promotion rules
- Latency budget (p95): 25.0 ms, because real-time predictions need to stay fast[span_6](start_span)[span_6](end_span).
- Minimum gain to replace the champion (F1 points): 0.005, because a new model should beat the current one by a meaningful margin rather than tiny noise[span_7](start_span)[span_7](end_span).

## What I would check next
I would check performance on smaller customer slices, tune the classification threshold for class imbalance, and watch for data or concept drift in production[span_8](start_span)[span_8](end_span).
