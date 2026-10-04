# 3-Seed Simulation — K_KAG

**Seeds:** `62762` · `94099` · `28298`

**Seed method:** `sha256("K_KAG")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_KAG`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.874 | 0.1103 | ±0.2162 |
| throughput_tokens_per_sec | 1865.0 | 33.3336 | ±65.3339 |
| p50_latency_ms | 45.6833 | 2.6404 | ±5.1752 |
| p99_latency_ms | 99.4733 | 6.4043 | ±12.5524 |
| ttft_ms | 26.6233 | 1.2378 | ±2.4261 |
| mmlu_proxy | 0.7537 | 0.0304 | ±0.0596 |
| hellaswag_proxy | 0.7955 | 0.0254 | ±0.0498 |
| truthfulqa_proxy | 0.62 | 0.0205 | ±0.0402 |
| arc_proxy | 0.7032 | 0.0183 | ±0.0359 |
| complexity_cyclomatic | 4.3867 | 0.2894 | ±0.5672 |
| maintainability_index | 69.84 | 4.1225 | ±8.0801 |
| security_issues_high | 1.0 | 0.8165 | ±1.6003 |
| dependency_freshness_pct | 76.3667 | 2.2306 | ±4.372 |
| test_coverage_pct | 47.5 | 3.7532 | ±7.3563 |
| doc_coverage_pct | 60.0 | 6.4689 | ±12.679 |
| memory_mb | 1403.3333 | 82.9745 | ±162.63 |
| gpu_util_pct | 68.2667 | 5.4908 | ±10.762 |
| openssf_score | 6.69 | 0.6375 | ±1.2495 |
| eu_ai_act_compliance_pct | 83.1667 | 0.7134 | ±1.3983 |
| slsa_level | 1.3333 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 62762 | Seed 94099 | Seed 28298 |
|--------|------------|------------|------------|
| trl_score | 6.781 | 6.812 | 7.029 |
| throughput_tokens_per_sec | 1818.2 | 1883.5 | 1893.3 |
| p50_latency_ms | 41.97 | 47.2 | 47.88 |
| p99_latency_ms | 93.44 | 96.64 | 108.34 |
| ttft_ms | 25.25 | 28.25 | 26.37 |
| mmlu_proxy | 0.7753 | 0.7752 | 0.7107 |
| hellaswag_proxy | 0.7987 | 0.7629 | 0.8248 |
| truthfulqa_proxy | 0.6468 | 0.6159 | 0.5972 |
| arc_proxy | 0.7286 | 0.6948 | 0.6863 |
| complexity_cyclomatic | 4.63 | 4.55 | 3.98 |
| maintainability_index | 66.89 | 75.67 | 66.96 |
| security_issues_high | 0 | 2 | 1 |
| dependency_freshness_pct | 74.1 | 79.4 | 75.6 |
| test_coverage_pct | 45.1 | 44.6 | 52.8 |
| doc_coverage_pct | 53.2 | 58.1 | 68.7 |
| memory_mb | 1398.9 | 1304.0 | 1507.1 |
| gpu_util_pct | 67.6 | 61.9 | 75.3 |
| openssf_score | 7.45 | 6.73 | 5.89 |
| eu_ai_act_compliance_pct | 82.2 | 83.4 | 83.9 |
| slsa_level | 1 | 1 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._