# WTECM Model and Implementation Design Evidence
이 폴더는 FW_001 먹이망 분석 프로젝트에서 수행한 **WTECM 연쇄 멸종 모델 설계**, **데이터 전처리 방식**, 그리고 **핵심 node 탐지 알고리즘과 평가 흐름**을 정리한 개인 기여 증빙 자료입니다.

## 1. WTECM 연쇄 멸종 모델 설계 및 구현 로직
LTM의 임계값 개념을 먹이망의 멸종 상황에 적용하여 WTECM(Weighted Threshold Extinction Cascade Model)을 설계하였습니다.

* 멸종한 먹이의 누적 식단 비율이 임계값 θ 이상이면 해당 포식자가 멸종하도록 정의
* 같은 wave에서 판정된 node를 한 번에 반영하는 staged cascade 방식 설계
* 초기 제거 seed, 먹이 손실률 계산, secondary extinction, cascade depth를 포함한 의사 코드 및 구현 로직 정리
* 알고리즘별 ranking을 동일한 WTECM 조건에서 검증하는 평가 구조 설계
* [WTECM 설계 자료](./WTECM%20설계.pdf)

## 2. 데이터 전처리 및 전체 알고리즘 구현 구조
원본 FW_001 식단 비율 행렬을 WTECM과 그래프 알고리즘에 적용할 수 있도록 전처리·그래프 모델링 방식을 설계하였습니다.

* 원본 `40 × 36` 식단 비율 행렬을 포식자 기준 계산이 가능하도록 전치
* 종명 기반 node id 매핑을 적용하여 그래프와 WTECM 간 인덱스 일관성 확보
* 먹이 관계를 `prey → predator` 방향의 가중 그래프로 변환
* WTECM용 그래프와 구조 알고리즘용 그래프의 self-loop 처리 방식 분리
* Kosaraju, BC, CI(l=1), CI(l=2), CoreHD ranking 생성부터 WTECM 평가·시각화까지의 전체 분석 파이프라인 정리
* [실험 설계 및 구현 구조 문서](./experiment_design_v5%281%29.docx)

## Contribution Summary
본 자료는 WTECM 모델의 핵심 규칙과 구현 절차를 설계하고, 이를 적용하기 위한 데이터 전처리·그래프 모델링·알고리즘 평가 흐름을 정리한 증빙 자료입니다.
