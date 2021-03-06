---
id: token-supply
title: Token Supply and Distribution
sidebar_label: Token Supply and Distribution
---

TON의 모든 공급은 초기발행량과 추가발행량으로 이루어진다. 추가발행량은 TON을 스테이킹한 오퍼레이터가 커밋을 수행할 때마다 발행되는 커밋 보상으로, 그 양은 항상 스테이킹된 TON의 양과 기간에 비례해서 결정된다. 커밋 보상의 분배 또한 스테이킹한 TON의 양과 기간에 따라 이루어진다.

## 토큰 공급

### 원칙
TON의 공급(발행)과 관련된 모든 정책은 다음 원칙에 근거하고 있다.

1. 매년 고정량이 추가 발행된다.
2. 추가 발행량은 전체발행량 중 스테이킹된 TON의 비율과 기간에 비례하며, 스테이킹된 TON의 비율이 100% 미만이거나, 스테이킹된 기간이 최대값이 아니라면 원칙 1에서 제시된 발행량보다 낮게 발행된다.
3. 원칙 2에 따른 미발행분의 일부는 파워톤에 사용된다. (이는 [파워톤](powerton)에서 자세히 다룬다)

### 공급
TON의 최초 발행량은 $IS$이며, TON의 연간 최대 커밋 보상은 $S_{y} = IS*IR_{y}$이다. 하지만 원칙 2에 명시된 것처럼 스테이킹된 TON의 양과 기간에 따라 연간 실제 커밋 보상인 $s_{y}$는 상이할 수 있다. $s_{y}$는 다음과 같이 계산된다.

$s_{y} = \sum_{i=1}^{N_{y}}\cfrac{td_{i}}{ts_{i}} * S_{b}$

#### 표기
* $IS$ : 최초 발행량
* $IR_{y}$ : 연간 목표 인플레이션율
* $S_{y}  = IS*IR_{y}$ : 연간 최대 커밋 보상
* $s_{y}$ : 실질 연간 커밋 보상
* $S_{b}$ : 루트체인 블록당 최대 커밋 보상
* $N_{y}$ : 루트체인에서 1년간 생성되는 총 블록의 수
* $ts_{t}$ : 시점 $t$의 총 발행량
* $td_{t}$ : 시점 $t$에 스테이킹된 TON의 총량

$s_{y}$는 해당 기간 동안 스테이킹된 TON의 양과 기간에 따라 $0\leq{s_{y}}\leq{S_{y}}$의 값을 가질 수 있다. **원칙 2** 에 따라 $td_{t}$이 $ts_{t}$에 가까울수록, 또 오랜 기간 동안 스테이킹이 될수록 $s_{y}$는 $S_{y}$에 근접하게 된다. 반대의 경우에 $s_{y}$는 0에 가까워지게 될 것이다.

여기서 유의해야 할 점은 시간을 계산의 기준이 실제 시간이 아니라 루트체인의 블록 단위라는 것이다. 예를 들어 연간이라는 시간 기준도 블록 높이로 계산되기 때문에 1년이라는 시간과 정확히 일치하지 않을 수 있다.

## 토큰 분배

### 원칙
앞서 다룬 $s_{y}$의 분배는 다음과 같은 원칙을 기준으로 이루어진다.

1. 커밋 보상은 토카막 네트워크에 기여한 이에게 주어진다.
2. 네트워크에 기여하는 대표적인 행위는 스테이킹을 통해 오퍼레이터가 되어 커밋을 수행하는 것이다.

### 커밋 보상 분배
커밋 보상은 토카막 네트워크에서 커밋 작업을 수행한 이에게 주어지며, 기여도에 따라 차등적으로 분배된다.

