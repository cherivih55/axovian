# Axovian Database Schema

## Users
- user_id
- created_at
- age_range (optional)
- device_type (optional)

## DailySessions
- session_id
- user_id
- date
- rt_median_ms
- rt_sd_ms
- wm_accuracy
- wm_rt_ms (optional)

## Stressors
- session_id
- low_sleep
- high_stress
- illness
- heavy_workload
- exercise
- late_caffeine

## Scores
- session_id
- deviation_score (DS)
- resilience_score (RS)
- neuro_vulnerability_index (NVI)
- baseline_version
