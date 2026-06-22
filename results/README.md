# FW_001 Food Web Analysis Results
브라질 Upper Paraná River Floodplain 먹이망(FW_001)을 대상으로, 구조 기반 핵심 node 탐지 알고리즘과 WTECM(Weighted Threshold Extinction Cascade Model) 기반 연쇄 멸종 결과를 비교한 시각화 자료입니다.

## Fig. 1. Reference Ranking Distribution & Algorithm Top-1
단일 node 제거 WTECM 결과를 기준으로 생성한 Reference Ranking의 분포와, 각 알고리즘이 선정한 Top-1 node의 참조 순위를 비교합니다.

## Fig. 2. Survival Curve, AUC, and R50
각 알고리즘의 ranking 순서대로 node를 제거했을 때의 생존 비율 변화를 나타냅니다. AUC와 R50이 낮을수록 더 적은 초기 제거만으로 큰 연쇄 멸종이 발생함을 의미합니다.

## Fig. 3. Performance Summary vs Reference Ranking
Spearman 상관계수, Reference Top-k 후보와의 overlap, Top-k 동시 제거 시 Secondary Extinction을 비교합니다. CI와 CoreHD가 Reference Ranking과 높은 일치도를 보이고, 다중 제거 상황에서 큰 cascade를 유발하는 후보군을 탐지했음을 확인할 수 있습니다.

## Fig. 4. Sensitivity Analysis over Threshold θ
WTECM 임계값 θ 변화에 따른 알고리즘별 AUC Gap을 비교합니다. AUC Gap은 Reference 순서 기반 AUC와 알고리즘 기반 AUC의 차이이며, 0에 가까울수록 Reference Ranking과 유사한 붕괴 양상을 보인다는 의미입니다.
