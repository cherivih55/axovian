# Axovian Scoring Logic

## Baseline Calculation
For each user, compute baseline mean (μ) and standard deviation (σ) over initial baseline window (7–14 days).

Metrics:
- rt_median_ms
- rt_sd_ms
- wm_accuracy

## Daily Z-Scores

z_rt = (rt_median − μ_rt) / σ_rt

z_var = (rt_sd − μ_var) / σ_var

z_wm = (μ_wm − wm_accuracy) / σ_wm

## Deviation Score (DS)

DS = average(|z_rt|, |z_var|, |z_wm|)

## Deviation Threshold

Deviation event defined as:
DS > 2.0

## Resilience Score (RS)

RS = 1 / (days until DS < 1.0)

Max recovery window capped at 7 days.

## Stressor Load (SL)

SL = sum of stressor flags

Range: 0–6

## Neuro Vulnerability Index (NVI)

NVI = 0.6 × DS + 0.2 × SL + 0.2 × (1 / RS)

NVI categories:
- Low
- Medium
- High
