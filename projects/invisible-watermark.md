# Invisible Watermark

**Algorithm development · Robustness evaluation · Python packaging**

[← Back to profile](../README.md) · [한국어 요약](#한국어-요약)

## Purpose

Develop an image watermarking system that embeds an identifier with minimal visible changes, then attempts to recover and verify it after image transformations.

## My role

I worked on the insertion and detection algorithms, evaluation tools, processing efficiency, and a Python package for backend integration. I also developed AWS KMS integration code and documented the package interfaces. A separate teammate handled cloud resource configuration, deployment, and operations.

## Engineering challenges

### Balancing visual quality and recovery

A watermark needs to preserve the appearance of an image while retaining a signal that the detector can recover. I investigated visible artifacts and compared insertion and detection behavior under controlled image transformations, including compression, resizing, and cropping. This helped distinguish supported conditions from failure cases.

### Controlling processing cost

High-resolution images increase memory use and computation. I worked on explicit image-processing limits and reused preparation work across detection attempts, with limits on the amount of searching the detector performs. I checked these changes with regression tests and documented their limits.

### Preparing a backend integration

I packaged the implementation behind Python interfaces, added tests around the package behavior, and wrote integration documentation. The work included AWS KMS integration and explicit result and error handling. This gave backend developers a documented package interface to call without importing the research scripts directly.

## Deliverables

- Image watermark insertion and detection implementations.
- Evaluation and regression tests for image transformations and negative cases.
- A Python package with documented interfaces and dependencies.
- Backend handoff documentation describing integration requirements and supported behavior.

The emphasis of this work was connecting algorithm experiments to a package another developer could use. These deliverables do not imply that every transformation is supported or that the package has completed a public production rollout.

## 한국어 요약

이미지 품질을 유지하면서 식별 정보를 삽입·검출하는 워터마크 기술을 개발했습니다. 저는 알고리즘 연구·구현, 변형 조건별 성능 평가, 고해상도 처리의 연산량·메모리 사용 개선, Python 패키징을 담당했습니다.

워터마크의 시각적 흔적과 검출 성능을 함께 검토하고, 실제 확인한 조건과 실패 조건을 구분했습니다. 백엔드에서 사용할 수 있도록 AWS KMS 연동 코드와 호출 인터페이스·문서를 작성했으며, 클라우드 설정과 배포·운영은 다른 담당자가 수행했습니다.
