# Network Devices & Cabling

## 1. 케이블

LAN에서 사용할 수 있는 케이블:

```text
TP(Twisted Pair)
동축 케이블
광섬유 케이블
```

TP 케이블은 여러 꼬임선을 절연체로 구성한 케이블이다.

종류:

```text
UTP
STP
```

---

## 2. UTP

`UTP`는 **Unshielded Twisted Pair**이다.

책 기준 특징:

```text
전송 길이 → 100m
전송 속도 → 10~100Mbps
설치 → 쉽고 취급이 용이
외부 간섭 → 약함
설치 비용 → 매우 저렴
용도 → Ethernet
```

### 핵심

```text
UTP
→ Unshielded
→ 저렴
→ 설치 쉬움
→ 전기적 간섭에 약함
```

---

## 3. STP

`STP`는 **Shielded Twisted Pair**이다.

책 기준 특징:

```text
전송 길이 → 100m
전송 속도 → 최대 155Mbps
설치 → UTP보다 조금 어려움
외부 간섭 → 없음
설치 비용 → 저렴
용도 → Token Ring, AppleTalk
```

### 핵심

```text
STP
→ Shielded
→ 외부 간섭에 강함
```

---

# Ethernet 케이블 표기

## 4. Ethernet 표기 방법

예:

```text
100 BASE FX
```

구성:

```text
100
→ 속도

BASE
→ 채널

FX
→ 케이블 타입
```

책에 나온 케이블 표현:

```text
SX
→ 단파장(Shortwave)

LX / LH
→ 장파장(Longwave / Long-haul)

FX
→ 광전송
```

---

## 5. Ethernet 종류

### 100BaseTX

```text
케이블
→ EIA/TIA CAT5, 2Pair

전송 거리
→ 100m
```

### 100BaseFX

```text
케이블
→ 62.5/125 멀티모드 광섬유

전송 거리
→ 400m
```

### 1000Base-CX

```text
케이블
→ STP

전송 거리
→ 25m
```

### 1000Base-T

```text
케이블
→ EIA/TIA CAT5, UTP 4Pair

전송 거리
→ 100m
```

### 1000Base-SX

```text
62.5 멀티모드
→ 275m

50 멀티모드
→ 550m
```

### 1000Base-LX

```text
62.5 멀티모드
→ 440m

50 멀티모드
→ 550m

9 싱글모드
→ 5km
```

---

# LAN 구성 장비

## 6. Repeater

리피터는 네트워크 케이블을 통해 신호가 전달될 때 발생하는  
**신호의 약화나 왜곡을 복구하고 증폭**한다.

또한 장거리 통신이 가능하도록 두 지점 사이의 거리를 연장한다.

```text
Repeater
→ 신호 복구
→ 신호 증폭
→ 전송 거리 연장
```

---

## 7. Hub

허브는 **신호를 노드에 전달하는 장비**이다.

주요 기능:

```text
네트워크 확장
다른 허브와 상호 연결
신호 증폭
```

---

## 8. Hub 종류

### 더미 허브

```text
각 노드를 집중화하는 장비
```

### 인텔리전트 허브

```text
자체 중앙 처리 장치
소량의 버퍼
SNMP 관리 가능
```

### 스태커블 허브

```text
허브의 백본 버스를 상호 연결
별도의 트렁크 포트 보유
```

### 이더넷 허브

```text
10Mbps 인터페이스 포트
```

### 패스트 이더넷 허브

```text
100Mbps 인터페이스 포트
```

### 토큰링 허브

```text
16Mbps 인터페이스 포트
```

---

## 9. LAN 카드

LAN 카드는 컴퓨터가 네트워크에 접속할 수 있도록 설치하는 확장 카드이다.

주요 기능:

```text
데이터를 전기신호로 변환하여 송신
전기신호에서 데이터를 변환하여 수신
MAC 주소를 이용하여 데이터 수신 여부 판별
```

### 핵심

```text
LAN Card
→ 네트워크 접속
→ 데이터 ↔ 전기신호 변환
→ MAC 주소 사용
```

---

## 10. Bridge

브리지는 수신 프레임을 먼저 버퍼에 저장한 후  
주소에 따라 목적지 포트로 전달하는 장비이다.

주요 특징:

```text
큰 네트워크를 작은 Segment로 분할
트래픽 감소
송수신 주소 분석
프레임 통과 여부 판단
필터링 수행
```

### 핵심

```text
Bridge
→ 프레임 버퍼 저장
→ 주소 분석
→ 목적지 포트 전달
→ Segment 분할
→ 필터링
```

---

## 11. Switch

스위치는 브리지와 비슷한 기능을 가진 장비이다.

책 기준 특징:

```text
브리지보다 빠르게 데이터 전송
MAC Address Table 기반으로 프레임 전송
트래픽 병목 현상 제거
포트별 속도를 전용으로 보장
```

### 핵심

```text
Switch
→ Bridge와 유사
→ Bridge보다 빠름
→ MAC Address Table 사용
→ 병목 현상 감소
```

---

# 핵심 비교

```text
Repeater
→ 신호 복구 / 증폭

Hub
→ 노드에 신호 전달

LAN Card
→ 네트워크 접속
→ MAC 주소

Bridge
→ Segment 분리
→ 주소 분석 / 필터링

Switch
→ MAC Address Table
→ Bridge보다 빠름
```

```text
Intelligent Hub
→ CPU + Buffer + SNMP

Stackable Hub
→ Trunk Port
```

---

# 시험 직전 암기

```text
UTP
→ 싸고 설치 쉬움
→ 간섭에 약함

STP
→ Shielded
→ 간섭에 강함
```

```text
Repeater = 신호
Hub = 집중 연결
Bridge = Segment
Switch = MAC Address Table
```

```text
1000Base-T
→ UTP 4Pair
→ 100m

1000Base-CX
→ STP
→ 25m
```
