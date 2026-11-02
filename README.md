# SurgEye
### Instruction Tuning-Free Perception-Reasoning Framework for Surgical Scene Understanding

**Status:** Submitted to [IEEE ISBI 2027](https://biomedicalimaging.org/2027/); acceptance pending.

**Personal research portfolio of Siyi Li**, a co-author of the SurgEye manuscript. This page summarises the collaborative project and my individual contributions.

## Overview

SurgEye addresses fine-grained surgical scene understanding and evidence-grounded question answering. It combines a shared vision foundation model with a frozen large language model, allowing surgical reasoning over structured perception evidence without instruction tuning on question-answer pairs.

## Framework

- **Routed Multi-Task Perception (RMP):** A frozen DINOv3 ViT-L backbone with task-specific LoRA adapters and prediction heads supports segmentation, detection, action triplet recognition, key event recognition and phase recognition.
- **Agentic Compositional Reasoning (ACR):** A frozen LLM coordinates perception specialists and structured temporal memory as callable tools to answer questions using evidence across tasks and time.
- **SurgEye-Bench:** A benchmark containing approximately 63K question-answer samples over 452K surgical frames, spanning eight surgical procedures and four reasoning dimensions.

## My Contributions

My main responsibility was the **Action triplet recognition component**, which recognises **instrument–verb–target** interactions in surgical images.

- Prepared and harmonised surgical datasets and annotations for action and triplet recognition.
- Implemented and trained recognition models using a frozen DINOv3-L backbone, LoRA adaptation and task-specific prediction heads.
- Conducted model evaluation and investigated data-processing and label-consistency issues across datasets.
- Contributed to the project demonstration interface.

The framework design, benchmark construction and overall results below reflect the work of the full research team.

## Selected Results Reported in the Manuscript

### Surgical perception

| Task | Metric | SurgEye |
| --- | --- | ---: |
| Segmentation | Dice (%) | 82.59 |
| Detection | AP50 (%) | 82.66 |
| Action triplet recognition | APIVT (%) | 35.76 |
| Key event recognition | F1 (%) | 91.02 |
| Phase recognition | F1 (%) | 72.40 |

Perception results are averaged over the datasets for each task, as reported in Table 3 of the manuscript.

### Surgical reasoning on SurgEye-Bench

| Evaluation dimension | Accuracy (%) |
| --- | ---: |
| Multi-Granular Semantic Reasoning (MSR) | 76.05 |
| Binary Existential Reasoning (BER) | 76.78 |
| Spatial Quantitative Reasoning (SQR) | 56.21 |
| Procedural Temporal Reasoning (PTR) | 78.11 |

SurgEye outperformed the evaluated VLM baselines across all four reasoning dimensions in the reported experiments.

## Manuscript

**Title:** SurgEye: Instruction Tuning-Free Perception-Reasoning Framework for Surgical Scene Understanding


**Submission:** IEEE International Symposium on Biomedical Imaging (ISBI) 2027.

The manuscript PDF will be added to this repository. This submission has not yet been accepted for publication.

## Research Areas

Surgical AI · Computer Vision · Vision Foundation Models · Parameter-Efficient Adaptation · Action Triplet Recognition · Agentic Reasoning
