# WTECM Model Design Evidence
이 폴더는 먹이망 핵심 node 탐지를 위해 제안한 WTECM(Weighted Threshold Extinction Cascade Model)의 초기 설계 자료를 담고 있습니다.

## Personal Contribution
* LTM의 임계값 기반 확산 원리를 먹이망의 연쇄 멸종 문제에 맞게 변형하여 WTECM 모델을 설계하였습니다.
* 멸종한 먹이의 누적 식단 비율이 임계값 θ 이상일 때 포식자가 다음 wave에서 멸종하도록 하는 staged cascade 절차와 의사 코드를 작성하였습니다.
* Secondary Extinction, Final Survival Ratio, R50, SCC Fragmentation, Largest Component Loss 등 알고리즘 비교를 위한 평가 지표와 실험 구조를 제안하였습니다.

본 설계 자료를 기반으로 최종 프로젝트에서는 FW_001 식단 비율 데이터를 가중 방향 먹이망으로 모델링하고, 알고리즘별 핵심 node ranking을 동일한 WTECM 조건에서 비교·검증하였습니다.
