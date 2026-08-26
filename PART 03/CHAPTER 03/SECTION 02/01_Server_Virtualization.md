# Server Virtualization

## 1. 가상화(Virtualization)

가상화는 **하나의 물리적인 IT 자원을 동시에 여러 개의 논리적인 IT 자원으로 사용할 수 있게 하는 기술**이다.

책에 나온 가상화 종류:

```text
데스크톱 가상화
서버 가상화
스토리지 가상화
네트워크 가상화
```

### 핵심

```text
Virtualization
→ Physical 1개
→ Logical 여러 개
```

---

# 서버 가상화

## 2. 서버 가상화의 정의

서버를 구성하는 모든 자원을 가상화하는 것을 의미한다.

하나의 물리적인 서버 호스트에서  
여러 개의 서버 운영체제를 Guest로 실행할 수 있게 해주는 소프트웨어 아키텍처이다.

```text
Physical Server Host
→ 여러 Guest OS 실행
```

여러 애플리케이션, 미들웨어, 운영체제가 서로 영향을 미치지 않으면서 동시에 사용될 수 있다.

---

# 서버 가상화 도입 목적

## 3. 물리 서버 및 공간 절감

여러 서버를 하나의 서버로 통합하여 가상환경을 구축한다.

```text
서버 통합
→ 물리 서버 감소
→ 공간 절감
```

---

## 4. Redundancy

한 서버에 문제가 발생하더라도 다른 서버에서 동일한 애플리케이션을 구동할 수 있다.

```text
Redundancy
→ 장애 대비
→ 중요한 시스템 구성요소 복제
```

---

## 5. 하드웨어 가용성 증가

```text
서버 자원 통합 운영
→ 하드웨어 가용성 증가
```

---

## 6. 업무 연속성 확보

체계적이고 안정적인 정보센터 이전 등을 통해 업무의 연속성을 확보할 수 있다.

---

## 7. HA와 자원 할당

```text
쉬운 이중화(HA) 구성
+
유연한 자원 할당

→ 시스템 가용성 증가
→ 안정성 확보
```

---

## 8. 비용 절감

책에 나온 내용:

```text
통합 구축
공동 활용
유지 관리
전력 비용
관리 비용

→ 중복 투자 및 예산 절감
```

---

# Hypervisor

## 9. 하이퍼바이저(Hypervisor)

하이퍼바이저는 **가상머신과 하드웨어 사이에 위치**하여 여러 가상머신이 동작할 수 있게 한다.

주요 역할:

```text
CPU
메모리
기타 하드웨어 자원

→ 각 가상머신에 논리적으로 분할 / 할당
```

또한 물리적 자원을 공유하면서 가상머신 간 **고립화(Isolation)**를 보장한다.

### 핵심

```text
Hypervisor
→ VM ↔ Hardware 사이
→ 자원 분할 / 할당
→ Isolation 보장
```

---

## 10. Isolation

책에서 고립화(Isolation)는 다음 목적을 위해 특정 서버를 다른 시스템이나 네트워크로부터 분리하여 독립적으로 운영하는 것을 의미한다.

```text
보안 강화
장애 확산 방지
성능 보장
```

---

# Hypervisor 방식

## 11. Native 방식

하드웨어에 직접 설치하여 실행하는 방식이다.

책에 나온 예:

```text
Xen
KVM
Xen Server
ESXi
```

### 핵심

```text
Native
→ Hardware에 직접 설치
```

---

## 12. Hosted 방식

일반 애플리케이션처럼 프로그램으로 실행하는 방식이다.

책에 나온 예:

```text
VirtualBox
VMware Workstation
```

### 핵심

```text
Hosted
→ 일반 프로그램처럼 실행
```

---

# Xen

## 13. Xen 특징

책에 나온 특징:

```text
케임브리지 대학교에서 개발 시작
2003년 첫 공개 버전 발표
리눅스 기본 커널에 포함
기본 Repository를 이용한 yum 설치 가능
KVM과 호환되는 가상 장치 관리자 사용
네트워크 MAC 주소 고정 가능
Xen 설치 후 Xen 커널로 부팅 필요
반가상화 및 전가상화 모두 이용 가능
상용화된 제품이 많음
```

### 핵심

```text
Xen
→ Linux Kernel 포함
→ 반가상화 + 전가상화
```

---

# KVM

## 14. KVM 특징

책에 나온 특징:

```text
Qumranet에서 개발
x86 시스템 기반
CPU 전가상화 방식
Intel VT / AMD-V 기반
리눅스 기본 커널 포함
기본 Repository 이용 yum 설치 가능
Xen과 호환되는 가상 장치 관리자 사용
네트워크 MAC 주소 고정 가능
KVM 및 KVM 모듈 설치 후 관련 모듈 로딩 필요
```

### 핵심

```text
KVM
→ x86
→ CPU 전가상화
→ Intel VT / AMD-V
→ Linux Kernel 포함
```

---

# VirtualBox

## 15. VirtualBox 특징

책에 나온 특징:

```text
InnoTek에서 개발
현재 Oracle이 개발
자유 소프트웨어
리눅스 기본 커널에 포함되지 않음
추가 Repository 설치를 통한 yum 사용 가능
설치 후 관련 모듈 로딩 필요
독자적인 가상 장치 관리자 사용
전가상화만 지원
대용량 가상머신 생성 시에도 빠르게 설치 가능
Mac OS 지원
```

### 핵심

```text
VirtualBox
→ InnoTek
→ Oracle
→ Linux Kernel 미포함
→ 전가상화만 지원
```

---

# Xen / KVM / VirtualBox 비교

```text
Xen
→ Linux Kernel 포함
→ 반가상화 + 전가상화
```

```text
KVM
→ Linux Kernel 포함
→ x86
→ Intel VT / AMD-V
→ CPU 전가상화
```

```text
VirtualBox
→ Linux Kernel 미포함
→ Oracle
→ 전가상화만
```

---

# 시험 직전 암기

```text
가상화
→ 물리 자원 1개를
→ 논리 자원 여러 개처럼 사용
```

```text
서버 가상화
→ Host 1대
→ Guest OS 여러 개
```

```text
Hypervisor
→ VM과 Hardware 사이
→ CPU / Memory 자원 분할
→ Isolation
```

```text
Native
→ Hardware에 직접
→ Xen / KVM / Xen Server / ESXi
```

```text
Hosted
→ 프로그램처럼 실행
→ VirtualBox / VMware Workstation
```

```text
Xen
→ 반가상화 + 전가상화

KVM
→ Intel VT / AMD-V
→ CPU 전가상화

VirtualBox
→ 전가상화만
```

```text
Redundancy
→ 장애 대비용 구성요소 복제

Isolation
→ 시스템을 분리하여 독립 운영
```
