# Cloud Computing

## 1. 클라우드 컴퓨팅 정의

클라우드 컴퓨팅은 공유 가능한 컴퓨팅 자원을 통합 운영하여  
사용자가 필요할 때 네트워크를 통해 접근할 수 있도록 하는 방식이다.

책에 나온 공유 가능한 자원:

```text
네트워크
서버
스토리지
애플리케이션 서비스
```

인터넷을 통해 다음과 같은 컴퓨터 서비스를 제공한다.

```text
서버
저장소
데이터베이스
네트워킹
소프트웨어
분석
```

### 핵심

```text
Cloud Computing
→ 네트워크를 통해
→ 필요한 자원을
→ 필요한 만큼 사용
```

---

# 2. 클라우드 컴퓨팅 특징

책에 나온 주요 특징:

```text
사업자와 직접 상호작용하지 않고
사용자의 관리 화면을 통해 서비스 이용 가능

모바일 기기 등 다양한 디바이스에서 접속 가능

사업자의 컴퓨팅 자원을 여러 사용자가 공유

필요에 따라 Scale Up / Scale Down 가능

이용한 만큼 요금 부과
```

### Scale Up / Scale Down

```text
Scale Up
→ 처리 능력을 높임

Scale Down
→ 처리 능력을 낮춤
```

---

# 3. 클라우드 컴퓨팅 장점

## 통합 관리

```text
소프트웨어와 데이터 통합 관리
→ 업데이트 및 유지보수 효율 향상
→ 비용 절감
```

## 유연한 자원 활용

```text
필요할 때 자원 확장
필요하지 않을 때 자원 축소
```

## 높은 가용성

```text
하드웨어 장애 발생 시에도
서비스를 계속 사용할 수 있도록 구성 가능
```

## 빠른 시스템 구축

```text
클라우드가 제공하는 H/W와 S/W 이용
→ 시스템을 신속하게 구축 가능
```

---

# 클라우드 서비스 종류

## 4. IaaS

`IaaS`는 **Infrastructure as a Service**의 약자이다.

서버나 스토리지 같은 하드웨어 자원을 임대해 주는 클라우드 서비스이다.

```text
IaaS
→ Infrastructure
→ 서버
→ 스토리지
→ 네트워크 자원
```

특징:

```text
사용자가 하드웨어를 직접 보유하지 않음
필요할 때 자원 추가 / 제거 가능
```

책에 나온 예:

```text
Amazon EC2
```

### 핵심

```text
IaaS
= Infrastructure
= 하드웨어 자원
= Amazon EC2
```

---

## 5. PaaS

`PaaS`는 **Platform as a Service**의 약자이다.

소프트웨어 서비스를 개발하기 위한 플랫폼을 제공한다.

```text
PaaS
→ Platform
→ 애플리케이션 개발 환경 제공
```

장점:

```text
환경 구축 수고 감소
단기간에 서비스 개발 및 제공 가능
```

책에 나온 예:

```text
Google App Engine
```

### 핵심

```text
PaaS
= Platform
= 개발 환경
= Google App Engine
```

---

## 6. SaaS

`SaaS`는 **Software as a Service**의 약자이다.

클라우드 환경에서 동작하는 응용 프로그램을 서비스 형태로 제공한다.

```text
SaaS
→ Software
→ 응용 프로그램 자체를 서비스로 사용
```

기존 패키지 소프트웨어처럼 모든 기능을 라이선스로 구매하는 것이 아니라:

```text
필요한 기능을
필요한 기간만큼 임대
```

하는 방식이다.

책에 나온 예:

```text
네이버메일
G메일
네이버 클라우드
구글 드라이브
```

### 핵심

```text
SaaS
= Software
= 응용 프로그램 서비스
```

---

# 7. IaaS / PaaS / SaaS 비교

```text
IaaS
→ Infrastructure
→ 서버 / 스토리지 등의 자원

PaaS
→ Platform
→ 개발 환경

SaaS
→ Software
→ 응용 프로그램
```

### 암기

```text
I = Infra
P = Platform
S = Software
```

---

# 클라우드 서비스 모델

## 8. Private Cloud

`Private Cloud`는 기업이 자체적으로 데이터센터 내부에 클라우드 환경을 구축하여 사용하는 방식이다.

```text
운영 주체
→ 기업

운영 장소
→ 자체 데이터센터
```

특징:

```text
자사 네트워크에 직원용으로 구축
기업 정책에 맞게 구축 가능
높은 기술력과 운영 능력 필요
회사 내부 IT 자원 활용
```

---

## 9. Public Cloud

`Public Cloud`는 클라우드 사업자가 시스템을 구축하고 여러 기업과 개인에게 서비스를 제공하는 방식이다.

```text
운영 주체
→ 클라우드 사업자

운영 장소
→ 기업 또는 개인의 방화벽 외부
```

특징:

```text
인터넷을 통해 불특정 다수에게 서비스 제공
클라우드 사업자가 자원에 투자
사용자의 운영 관리 부담이 적음
단기간에 저비용으로 자원 확보 가능
```

---

## 10. Hybrid Cloud

`Hybrid Cloud`는 사설 클라우드와 공용 클라우드를 함께 사용하는 방식이다.

```text
Hybrid Cloud
= Private Cloud + Public Cloud
```

책에서는 다음에 따라 선택적으로 사용할 수 있다고 설명한다.

```text
데이터 중요도
비즈니스 핵심 업무 여부
컴퓨팅 자원의 위치
```

---

# 클라우드 구축 환경

## 11. OpenStack

OpenStack은 **IaaS 형태의 클라우드 컴퓨팅 오픈 소스 프로젝트**이다.

책에 나온 특징:

```text
2012년 설립된 OpenStack Foundation에서 유지 / 보수
Apache License
150개 이상의 회사가 프로젝트에 참여
```

책에 나온 5개의 코어 프로젝트:

```text
Nova
Swift
Glance
Keystone
Horizon
```

### 핵심

```text
OpenStack
→ IaaS
→ Open Source
→ Nova / Swift / Glance / Keystone / Horizon
```

---

## 12. CloudStack

CloudStack 역시 **IaaS 형태의 클라우드 컴퓨팅 오픈 소스 프로젝트**이다.

책에 나온 특징:

```text
Citrix에서 오픈 소스로 공개
네트워크 관리
스토리지 관리
컴퓨팅 노드 관리
클라우드 자원 배치 및 관리
```

### 핵심

```text
CloudStack
→ IaaS
→ Citrix
```

---

## 13. Eucalyptus

Eucalyptus도 **IaaS 형태의 클라우드 컴퓨팅 오픈 소스 프로젝트**이다.

책에 나온 특징:

```text
미국 UC Santa Barbara 대학에서 시작
현재 Eucalyptus Systems에서 관리
Amazon EC2 API와 동일한 API 사용
EC2와 호환
```

또한 분리된 물리 자원에서 Eucalyptus 구성 요소를 운영할 수 있는 환경을 지원한다.

### 핵심

```text
Eucalyptus
→ IaaS
→ EC2 API 호환
```

---

# 핵심 비교

```text
IaaS
→ 하드웨어 자원
→ Amazon EC2

PaaS
→ 개발 플랫폼
→ Google App Engine

SaaS
→ 응용 프로그램
→ Gmail / Google Drive 등
```

```text
Private
→ 기업 자체 데이터센터

Public
→ 클라우드 사업자가 제공

Hybrid
→ Private + Public
```

```text
OpenStack
→ Nova / Swift / Glance / Keystone / Horizon

CloudStack
→ Citrix

Eucalyptus
→ Amazon EC2 API 호환
```

---

# 시험 직전 암기

```text
Cloud
→ 필요한 자원을
→ 네트워크로
→ 필요한 만큼 사용
```

```text
Scale Up
→ 처리 능력 ↑

Scale Down
→ 처리 능력 ↓
```

```text
IaaS = Infrastructure
PaaS = Platform
SaaS = Software
```

```text
Private = 자체 구축
Public = 사업자 제공
Hybrid = Private + Public
```

```text
OpenStack
→ Nova
→ Swift
→ Glance
→ Keystone
→ Horizon
```

```text
CloudStack = Citrix
Eucalyptus = EC2 API 호환
```
