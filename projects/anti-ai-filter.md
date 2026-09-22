# Anti-AI Filter

**Image protection · PyTorch · LoRA training disruption**

[← Back to profile](../README.md) · [한국어 요약](#한국어-요약)

## Purpose

Research image-protection filters aimed at disrupting unauthorized LoRA (low-rank adaptation) training on creators’ artwork while limiting visible changes to the original images.

## My role

I worked on protective image perturbation algorithms, visual-quality evaluation, diffusion-model LoRA fine-tuning experiments, and Python tooling for running and comparing those experiments.

## Research and development

- **Filter optimization:** Implemented and experimented with PyTorch optimization pipelines that constrain pixel changes and account for perceptual image quality.
- **Downstream evaluation:** Compared diffusion models fine-tuned using LoRA on original images, protected images, and control images with added noise or texture. Examined generated outputs to assess whether changes in optimization metrics translated into effects on model learning.
- **Robustness analysis:** Investigated how preprocessing and attempts to remove perturbations affected candidate filters, recording failures alongside promising results.
- **Experiment tooling:** Worked on Python and command-line interfaces for image processing, batch handling, and experiment manifests recording configurations, model revisions, and identifiers for input images and experiment outputs.

## Evaluation approach

I distinguished successful pipeline execution, changes in intermediate model features, and effects observed after diffusion-model fine-tuning using LoRA. These answer different questions; an improved optimization metric alone was not treated as proof of protection.

In one comparison, a candidate improved intermediate metrics but failed the downstream evaluation against control conditions. I retained it as an experimental option rather than promoting it to the default method.

I documented the tested models, artwork, preprocessing, and training seeds when interpreting results. Findings are limited to those research conditions and do not establish universal prevention of AI training.

## 한국어 요약

원본 작품의 시각적 변화를 제한하면서, 해당 작품을 이용한 생성 모델의 무단 LoRA 학습을 방해하는 것을 목표로 이미지 보호 필터를 연구·개발했습니다. PyTorch 기반 보호용 섭동 최적화, 화질 평가, 원본·보호 이미지·대조군을 사용한 확산모델의 LoRA 미세조정 비교 실험과 Python 실행 도구 개발을 수행했습니다.

최적화 지표의 변화와 실제 미세조정 후 생성 결과를 구분해 평가하고, 전처리나 섭동 제거 시도에 따른 한계를 함께 기록했습니다. 중간 지표가 개선되어도 후속 비교 평가를 통과하지 못한 후보는 기본 방식으로 채택하지 않고 실험용으로 남겼습니다. 결과는 평가한 모델과 실험 조건의 범위 안에서 해석했습니다.
