---
title: "Brain2VLM: Hierarchical Alignment Between Cortical Representations and Vision-Language Latent Spaces"
authors: "Pritam, N. A. A., O, J. S., Jain, S."
date: 2026-04-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.23.720313v1.full.pdf"
tags: ["query:flrlvldm"]
score: 9.0
evidence: 基于扩散的视觉语言模型和CLIP嵌入
tldr: 通过将皮层表征与基于扩散的VLM潜空间对齐，分析大脑到图像的重建。
source: biorxiv
selection_source: fresh_fetch
motivation: 基于扩散的视觉语言模型和CLIP嵌入。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
This work introduces Brain2VLM, a framework for analyzing how cortical representations align with latent spaces of pretrained diffusion-based vision-language models for brain-to-image reconstruction. While recent approaches achieve strong performance by mapping functional Magnetic Resonance Imaging (fMRI) signals to model latents, the structure of this mapping remains poorly understood. We hypothesize that brain-to-latent alignment is hierarchical, with early visual cortex exhibiting approximately linear correspondence to structural diffusion latents, and higher-order visual areas requiring nonlinear mappings to align with semantic embedding spaces. To test this, we decode diffusion latents and CLIP embeddings from fMRI signals using both linear ridge regression and a nonlinear residual MLP on the Natural Scenes Dataset. Our results reveal that nonlinear decoding provides only marginal improvements for diffusion latents ({approx}{Delta} 0.05 - 0.06 in correlation), but yields substantial gains for semantic embeddings ({Delta}{approx}0.47), significantly improving distributional alignment (MMD: 0.042 vs 0.358). However, increased decoder expressivity can introduce shifts in latent distributions, highlighting a trade-off between prediction accuracy and generative compatibility. Despite using a simple reconstruction pipeline, Brain2VLM achieves strong performance (PixCorr 0.33, CLIP 85%), suggesting that improvements in brain-to-latent alignment play an important role in reconstruction quality alongside generative modeling. These findings provide empirical evidence for hierarchical alignment between cortical representations and model latent spaces, positioning the brain-to-latent interface as a primary bottleneck in brain decoding systems. Our code can be found at https://github.com/adarsh-crafts/Brain2VLM