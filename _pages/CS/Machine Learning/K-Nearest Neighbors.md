---
title: "[Machine Learning] K-Nearest Neighbors (K-NN)"
tags:
    - K-NN
date: "2025-07-23"
thumbnail: "/assets/img/thumbnail/machinelearning.png"
---

> 본 글은 국민대학교 한재섭 교수님의 2025년 1학기 AIX 교과목 내용을 참고하여 작성하였습니다.

# 개요
K-NN은 데이터의 분류를 예측할 때, 학습 데이터 중 가장 가까운 K개의 이웃 중 다수결을 결과로 예측하는 알고리즘이다.

# 거리
개요에서 설명했듯 가까운 이웃을 골라야 한다. 이때 가깝다를 판별하는 기준인 "거리"에도 여러 종류의 거리들이 있다.
## 맨해튼 거리(\\(L_1\\) Distance)
맨해튼 거리는 데카르트 좌표계에서 각 좌표의 차의 합이다.
수식으로 표현하면 \\(|x_1-x_2|+|y_1-y_2|\\) 로 나타낼 수 있다.

## 유클리드 거리(\\(L_2\\) Distance)
유클리드 거리는 우리가 수학에서 일반적으로 사용하는 점 사이 거리공식이다.
수식으로 표현하면 \\(\sqrt{(x_1-x_2)^2 + (y_1-y_2)^2}\\) 로 나타낼 수 있다.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Manhattan_distance.svg/250px-Manhattan_distance.svg.png" width="100" height="100"><br> <span style="color:gray">출처: 위키피디아</span></sup></sub>


위 그림에서 빨간색, 파란색, 노란색 선의 길이가 맨해튼 거리,
초록색 선의 길이가 유클리드 거리이다.

주로 이 두 거리 중 하나를 택하여 사용한다.

# parameter
파라미터로는 K하나만 가진다. K개의 이웃을 살필 때의 K이다. K가 작으면 과적합이 생길 수 있고 K가 크면 과소적합의 가능성이 커진다.
그림으로 K-NN을 살펴보자
![knn시각화](https://i.imgur.com/4GW6KdE.png)
순서대로 K=1, 3, 5일 때 모습이다.

적절한 파라미터를 정하기 위해서는 train 데이터와 test 데이터를 구분해 정확도를 높여 가야한다. 이 과정은 다른 글에서 다룰 예정이다.