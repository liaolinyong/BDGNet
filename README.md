# BDGNet: Explicit Multi-Scale Difference Priors with Difference-Guided Directional Response Adaptation for Remote Sensing Change Detection

**Note:** This is the official project repository of **BDGNet**. The source code, pretrained models, and training/inference instructions will be released after being organized.

## BDGNet

BDGNet is designed for bi-temporal remote sensing change detection, where reliable localization requires both fine-grained difference cues and robust long-range context modeling. The network introduces explicit multi-scale difference priors to guide feature learning rather than relying only on implicit feature differencing. Its Difference Prior Generator (DPG) builds scale-specific priors from absolute, squared, and gradient discrepancies, then injects them through zero-initialized residual paths. At deeper stages, Difference-Guided Directional Scan (DGDS) reuses the DPG prior to modulate four directional selective responses before CrossMerge while keeping the state-space recurrence unchanged. BDGNet is evaluated on binary change detection benchmarks and the SECOND semantic change detection benchmark.

![BDGNet framework](pictures/framework.png)

### Difference Prior Generator

![Difference Prior Generator](pictures/dpg.png)

### Difference-Guided Directional Scan

![Difference-Guided Directional Scan](pictures/dgds.png)

## Results

| Dataset | Precision | Recall | F1 | IoU | OA | mIoU | SeK |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| SYSU-CD | 86.74 | 84.53 | 85.62 | 74.86 | - | - | - |
| LEVIR-CD | 94.75 | 92.36 | 93.54 | 87.87 | - | - | - |
| WHU-CD | 97.86 | 94.30 | 96.04 | 92.39 | - | - | - |
| SECOND | - | - | 64.13 | - | 91.28 | 74.96 | 26.53 |
| SYSU-CD three-seed | - | - | 85.66 +/- 0.20 | 74.92 +/- 0.30 | - | - | - |

### Qualitative Comparison on SYSU-CD

![Qualitative comparison on SYSU-CD](pictures/sysu_qualitative.png)

### Qualitative Comparison on LEVIR-CD

![Qualitative comparison on LEVIR-CD](pictures/levir_qualitative.png)

### Qualitative Comparison on WHU-CD

![Qualitative comparison on WHU-CD](pictures/whu_qualitative.png)

### Qualitative Ablation

![Qualitative ablation](pictures/ablation.png)

### Three-Seed Stability

![Three-seed stability](pictures/stability.png)

### Semantic Change Detection on SECOND

![Semantic change detection on SECOND](pictures/second_qualitative.png)

## Dependency

Coming Soon...

## Data Preparation

Coming Soon...

## Quick Start

Coming Soon...

## Pretrained Models

Coming Soon...

## Citation

Citation information will be updated after publication.

## Acknowledgment

This work is implemented with inspiration from recent state-space and remote sensing change detection studies, including ChangeMamba and VMamba.
