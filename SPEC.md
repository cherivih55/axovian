# Axovian Specification v1

## Objective
Quantify brain stability and resilience using longitudinal within-person cognitive performance data.

## Daily Session Components

### Cognitive Tasks
1. Reaction Time Task
- duration: 15 seconds
- metrics:
  - median reaction time (ms)
  - reaction time standard deviation (ms)

2. Working Memory Task
- duration: 20 seconds
- metrics:
  - accuracy (%)
  - response time (optional)

### Stressor Tags
Binary inputs:
- low sleep
- high stress
- illness
- heavy workload / exam
- exercise
- late caffeine

## Outputs

### Deviation Score (DS)
Measures deviation from individual baseline.

### Resilience Score (RS)
Measures recovery time after deviation.

### Neuro Vulnerability Index (NVI)
Composite vulnerability score derived from deviation, recovery, and stressors.

## Baseline Window
7–14 days initial baseline period.

## Deviation Definition
DS > threshold (initial threshold = 2.0)

## Recovery Definition
Days required for DS to return below recovery threshold (initial threshold = 1.0)

## Data Storage
Daily sessions stored with timestamp and performance metrics.
