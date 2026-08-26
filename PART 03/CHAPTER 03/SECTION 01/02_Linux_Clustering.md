# Linux Clustering

## 1. 클러스터링(Clustering)

클러스터링은 여러 개의 시스템을 연결하여  
**하나의 거대한 시스템처럼 보이고 동작하게 만드는 기술**이다.

```text
여러 컴퓨터
→ 네트워크로 연결
→ 하나의 컴퓨터처럼 동작
```

### 핵심

```text
Clustering
→ 여러 시스템
→ 하나의 시스템처럼 동작
```

---

# 클러스터 구성요소

## 2. 클러스터 노드

클러스터의 **실질적인 작업을 처리**하는 시스템이다.

```text
Cluster Node
→ 실제 작업 처리
→ 클러스터에 소속
```

---

## 3. 클러스터 관리자

각 노드의 자원을 분배하고 관리한다.

책에 나온 특징:

```text
각 노드 자원 분배 및 관리
클러스터 노드가 관리자 기능을 가질 수도 있음
환경에 따라 여러 대의 클러스터 관리자 존재 가능
```

### 핵심

```text
Cluster Manager
→ 자원 분배
→ 노드 관리
```

---

# 클러스터 구축 목적

## 4. 고성능 컴퓨팅

여러 시스템의 프로세싱 능력을 결합하여  
대용량의 처리 능력을 갖는 하나의 시스템을 구성한다.

```text
여러 시스템 처리 능력 결합
→ 고성능 컴퓨팅
→ HPC
```

---

## 5. Load Balancing

여러 웹서버 등의 노드를 두고 중앙 관리 부분에서 부하를 조정한다.

```text
Load Balancing
→ 여러 서버에 부하 분산
```

---

## 6. Fail-over

주 서버에 문제가 발생하면 백업 서버가 대신 동작하도록 한다.

```text
Fail-over
→ 주 서버 장애
→ Backup Server 가동
→ 서비스 지속
```

---

# 클러스터 종류

## 7. HPC Cluster

`HPC`는 **High Performance Computing**의 약자이다.

책에서는 **Beowulf Cluster**라고도 부른다.

주요 특징:

```text
고성능 계산 능력 제공
과학 계산용으로 활용 가치가 높음
```

### 핵심

```text
HPC
→ High Performance Computing
→ Beowulf
→ 고성능 계산
→ 과학 계산
```

---

## 8. LVS Cluster

`LVS`는 **Linux Virtual Server**의 약자이다.

책에서는 **부하 분산 클러스터**로 설명한다.

주요 특징:

```text
대규모 서비스 제공 목적
주로 웹서비스에 활용
여러 서버가 로드밸런서에 연결
로드밸런서가 부하를 분산
```

### 핵심

```text
LVS
→ Linux Virtual Server
→ Load Balancing
→ 대규모 웹서비스
```

---

## 9. LVS 웹 요청 처리 과정

```text
1. 인터넷에서 웹 요청이 Load Balancer로 들어옴

2. Load Balancer가 알고리즘에 따라
   서비스를 수행할 서버를 선택

3. 웹 요청을 선택된 서버로 Forwarding

4. 서버가 응답을 Load Balancer에 제공

5. Load Balancer가 응답 데이터를
   요청한 컴퓨터로 재전송
```

### 흐름

```text
Client
→ Load Balancer
→ Server 선택
→ Forwarding
→ Server 응답
→ Client
```

---

## 10. HA Cluster

`HA`는 **High Availability**의 약자이다.

목적:

```text
지속적인 서비스 제공
```

책에 나온 주요 활용 분야:

```text
금융권
데이터센터
회사의 기간업무
```

주요 특징:

```text
Load Balancer 시스템 이용

Load Balancer와 Backup Server가
주기적으로 통신하여 이상 여부 확인

장애 발생 시
→ Load Balancer가 점유한 IP를
   Backup Server로 이동

→ 지속적인 서비스 수행
```

### 핵심

```text
HA
→ High Availability
→ 지속적인 서비스
→ 장애 대비
→ Backup Server
```

---

# HPC / LVS / HA 비교

```text
HPC
→ 성능
→ High Performance Computing
→ Beowulf
→ 과학 계산
```

```text
LVS
→ 부하 분산
→ Linux Virtual Server
→ Load Balancer
→ 대규모 웹서비스
```

```text
HA
→ 가용성
→ High Availability
→ 장애 시 Backup Server
→ 지속적인 서비스
```

---

# 시험 직전 암기

```text
Clustering
→ 여러 시스템을 하나처럼
```

```text
Cluster Node
→ 실제 작업 처리

Cluster Manager
→ 자원 분배 / 관리
```

```text
HPC = 계산 성능
LVS = 부하 분산
HA  = 장애 대비
```

```text
HPC
→ Beowulf

LVS
→ Linux Virtual Server

HA
→ High Availability
```

```text
Load Balancing
→ 부하 분산

Fail-over
→ 장애 발생 시 백업 서버로 전환
```
