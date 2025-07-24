# Gas Detection and Identification Using Multimodal Artificial Intelligence Based Sensor Fusion

이 저장소는 아래 논문을 기반으로 한 구현 및 분석을 포함하고 있습니다.

**"Gas Detection and Identification Using Multimodal Artificial Intelligence Based Sensor Fusion"**  
저자: Narkhede et al., 2021  
학술지: *Applied System Innovation*  
[DOI 링크](https://doi.org/10.3390/asi4010003)

---

## 개요

본 프로젝트는 **열화상 이미지**와 **가스 센서 시계열 데이터**를 융합한 **멀티모달 인공지능 모델**을 구현하고 실험한 결과를 담고 있습니다.  
논문에서는 **CNN**(열화상 이미지 처리)과 **LSTM**(가스 센서 시계열 처리)을 결합한 **Early Fusion / Late Fusion 모델**을 제안합니다.

이러한 융합을 통해 각 단일 모달리티보다 높은 정확도의 가스 분류 및 탐지가 가능합니다.

---

## 데이터셋

- 출처: [Mendeley Data Repository](https://data.mendeley.com/datasets/zkwgkjkjn9/2)
- 구성:
  - **열화상 이미지 (Thermal Camera Images)**
  - **가스 센서 시계열 데이터 (Gas Sensor Measurements)**
 
 ---

## 모델 구조

### Early Fusion
- CNN과 LSTM의 feature vector를 결합 (concatenation)
- 이후 fully connected layer에서 최종 분류 수행

### Late Fusion
- CNN과 LSTM 각각 독립적으로 학습된 후
- Softmax 출력 값을 결합하여 최종 예측 결정

---

## 주요 실험

- 단일 모달 vs 멀티모달 성능 비교
- Early vs Late Fusion 성능 비교
- 다양한 가스에 대한 분류 정확도 분석
- 모델 구조 변경 시 성능 변화 실험

---

## 결과 요약

- 멀티모달 모델이 단일 모달 모델 대비 월등한 성능을 보임
- Early Fusion 방식이 Late Fusion보다 높은 정확도를 기록
- 가스 종류에 따라 분류 난이도에 차이가 있음

| 모델 유형        | 정확도 (Accuracy) |
|------------------|------------------|
| Image Only     | 약 93%           |
| Sensor Only      | 약 83%           |
| Early Fusion     | 약 96%           |
| Late Fusion      | 약 96%           |

---
