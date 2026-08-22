# LAN Topology & Media Access Control

## 1. LAN 토폴로지

토폴로지(Topology)는 **호스트와 장비들의 물리적인 배치 형태**이다.

책에 나온 종류:

```text
성형(Star)
망형(Full Mesh)
버스형(Bus)
링형(Ring)
트리형(Tree)
```

---

## 2. 성형 Star

중앙 장치를 중심으로 여러 컴퓨터가 연결되는 구조이다.

주요 특징:

- 중앙 컴퓨터에 여러 컴퓨터가 허브 또는 스위치로 연결
- 네트워크 확장이 용이
- 고속의 대규모 네트워크에 적합
- 중앙 장치 고장 시 전체 네트워크 사용 불가능

```text
Star
→ 중앙 집중
→ 확장 쉬움
→ 중앙 장치 고장 = 전체 장애
```

---

## 3. 망형 Full Mesh

모든 노드가 서로 일대일로 연결되는 구조이다.

주요 특징:

- 대량 데이터 송수신에 적합
- 장애 발생 시 다른 경로로 우회 가능
- 가장 신뢰성이 높은 방식
- 회선 구축 비용이 많이 듦

노드가 N개일 때 최대 회선 수:

```text
N(N-1) / 2
```

### 핵심

```text
Full Mesh
→ 모든 노드 직접 연결
→ 우회 가능
→ 신뢰성 높음
→ 비용 높음
```

---

## 4. 버스형 Bus

하나의 통신 회선에 여러 컴퓨터를 연결하는 구조이다.

주요 특징:

- 하나의 통신 회선 공유
- 단말 추가 및 제거가 쉬움
- 설치 비용이 저렴
- 노드 수 증가 시 트래픽 증가
- 병목 현상 발생 가능
- 문제가 발생한 노드 위치 파악이 어려움

```text
Bus
→ 하나의 선 공유
→ 저렴
→ 추가/제거 쉬움
→ 노드 증가 시 병목
```

---

## 5. 링형 Ring

각 노드가 좌우의 인접한 노드와 연결되어 원형을 이루는 구조이다.

주요 특징:

- 받은 데이터를 다음 컴퓨터로 재전송
- Token Passing 사용
- 전송상 충돌이 없음
- 노드 수가 증가해도 성능 저하가 적음
- 노드 추가 및 삭제가 쉽지 않음
- 논리적 순환형에서는 한 노드 장애가 전체 토폴로지에 영향을 줄 수 있음

```text
Ring
→ 원형
→ Token Passing
→ 충돌 없음
→ 추가/삭제 어려움
```

---

## 6. 트리형 Tree

버스형과 성형 토폴로지를 확장한 구조이다.

주요 특징:

- Backbone과 같은 공통 버스 사용
- 허브나 스위치를 사용하여 링크 확장
- 트래픽 증가 시 병목 현상 가능

```text
Tree
→ Bus + Star 확장
→ Backbone
→ 계층 구조
```

---

# Media Access Control

## 7. MAC

`MAC`은 **Media Access Control**의 약자이다.

여러 단말이 공유 매체를 사용할 때 발생하는 충돌 및 경합을 제어한다.

```text
MAC
→ Media Access Control
→ 공유 매체 접근 제어
→ 충돌 / 경합 제어
```

---

## 8. CSMA/CD

`CSMA/CD`는 다음의 약자이다.

```text
Carrier Sense Multiple Access
/
Collision Detection
```

### 동작 과정

```text
1단계
→ 네트워크 캐리어 감지
→ 전송 가능한지 검사

2단계
→ 전송 가능하면 데이터 전송

3단계
→ 충돌 감지
→ JAM 신호 Broadcast

4단계
→ Back-off 알고리즘에 따라 랜덤 시간 대기
→ 다시 전송 시도
```

### 핵심 흐름

```text
감지
→ 전송
→ 충돌
→ JAM
→ Back-off
→ 재전송
```

```text
CSMA/CD
→ Collision Detection
→ JAM
→ Back-off
```

---

## 9. Token Passing

Token의 흐름에 의해 데이터의 전송 순서가 결정된다.

`Free Token`과 `Busy Token`을 이용하여 매체 접근을 제어한다.

### 동작 과정

```text
1단계
→ Free Token인지 Busy Token인지 확인

2단계
Free Token이면
→ Busy Token으로 변경
→ 데이터 전송

3단계
전송 완료 후
→ Busy Token을 Free Token으로 변경
```

---

## 10. Free Token / Busy Token

### Free Token

```text
Free Token
→ 회선에 데이터가 전송되지 않는 상태
→ 사용 가능
```

### Busy Token

```text
Busy Token
→ 특정 컴퓨터가 데이터를 전송 중인 상태
→ 회선 사용 불가
```

### 암기

```text
Free = 비어 있음 = 전송 가능
Busy = 사용 중 = 전송 불가
```

---

# 핵심 비교

```text
Star
→ 중앙 장치

Full Mesh
→ 모두 연결
→ N(N-1)/2

Bus
→ 하나의 회선 공유

Ring
→ Token Passing

Tree
→ Bus + Star
→ Backbone
```

```text
CSMA/CD
→ 충돌 감지
→ JAM
→ Back-off

Token Passing
→ Free Token / Busy Token
→ 전송 순서 제어
```

## 시험 직전 암기

```text
Star = 중앙
Mesh = 모두 연결
Bus = 한 줄
Ring = 원형 + Token
Tree = Backbone
```

```text
Mesh 최대 회선 수
= N(N-1)/2
```

```text
CSMA/CD
= JAM + Back-off

Token Passing
= Free → Busy → Free
```
