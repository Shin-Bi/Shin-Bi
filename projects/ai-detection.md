# AI Image Detection

**Computer vision · Model experiments · Evaluation design**

[← Back to profile](../README.md) · [한국어 요약](#한국어-요약)

## Purpose

Research methods for detecting AI-generated images, with dedicated experiments comparing human-created and AI-generated illustrations and evaluating detection after compression and resizing.

## My role

I worked on training and evaluation data preparation, detection model experiments, robustness analysis, and reproducible experiment tooling. This included investigating failures and comparing candidate models against a baseline.

## Research and development

### Model experiments

I implemented and compared detection heads using features from a pretrained vision model. The experiments included linear and nonlinear heads and training across transformed views of an image. The goal was to test whether a candidate maintained useful discrimination under image degradation.

### Data and evaluation

I prepared reproducible data selections and kept training, validation, and test roles separate. I examined whether acquisition differences, such as image dimensions or file format, could become shortcuts for the detector. Candidate selection and threshold setting were separated from final evaluation.

### Robustness and failure analysis

I evaluated compression, resizing, and chained transformations, considering false positives as well as detection rates. In one experiment, a candidate improved overall discrimination but failed an acceptance check on held-out compressed images. I recorded the decision not to advance that candidate. Research evaluation and approval for deployment were treated as separate steps.

## Deliverables

- Model training and evaluation scripts.
- Reproducible dataset selections and experiment configurations.
- Baseline comparisons, transformation tests, and failure analyses.
- Research reports documenting candidate decisions and remaining limitations.

These experiments use controlled transformations as proxies for image distribution conditions. They do not establish performance across every social platform, generator, or image domain.

## 한국어 요약

AI 생성 이미지 탐지 모델을 연구·개발하며 데이터 구성, 모델 학습·비교 실험, 압축·리사이즈 조건에서의 성능 평가를 수행했습니다.

특히 이미지 크기나 파일 형식 같은 데이터 특성에 탐지 결과가 의존하는지 확인하고, 학습·모델 선택·최종 평가를 구분해 실험했습니다. 성능이 개선된 조건과 기준을 충족하지 못한 조건을 함께 기록하며 후속 개발 방향을 정리했습니다.
