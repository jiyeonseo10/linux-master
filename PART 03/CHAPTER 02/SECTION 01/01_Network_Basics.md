# Network Basics

## 1. 통신망 종류

통신망은 지역적 범위에 따라 다음과 같이 구분한다.

```text
LAN
→ MAN
→ WAN
→ Internet
```

범위는 다음 순서로 커진다.

```text
LAN < MAN < WAN < Internet
```

---

## 2. LAN

`LAN`은 **Local Area Network**의 약자이며 근거리 통신망이다.

주요 특징:

- 빌딩 내부 또는 근접한 거리의 빌딩 등 제한된 지역에서 사용
- 정보 기기 사이의 고속 통신 제공

책에 나온 LAN 종류:

```text
Ethernet
Token Ring
FDDI
```

---

## 3. Ethernet

Ethernet의 주요 특징:

```text
IEEE 802.3
CSMA/CD 사용
```

1980년 DEC, Intel, Xerox가 DIX Ethernet 표준을 발표하였다.

### 핵심

```text
Ethernet
→ IEEE 802.3
→ CSMA/CD
```

---

## 4. Token Ring

Token Ring의 주요 특징:

- IBM이 개발
- IEEE 802.5 LAN
- 데이터가 한 방향으로 순차적으로 전달
- Token Passing 사용

### 핵심

```text
Token Ring
→ IBM
→ IEEE 802.5
→ Token Passing
```

---

## 5. FDDI

`FDDI`는 **Fiber-Distributed Data Interface**의 약자이다.

주요 특징:

- LAN 사이의 고속 통신에 사용
- 백본망 연결에 사용
- 이중 링(Dual Ring) 구조
- 데이터 전송 링과 백업용 링으로 구성
- Token Passing 사용

### 핵심

```text
FDDI
→ Dual Ring
→ Token Passing
→ 백본망
```

---

## 6. MAN

`MAN`은 **Metropolitan Area Network**의 약자이다.

LAN보다 크고 WAN보다 작은 도시권 통신망이다.

주요 특징:

- 같은 도시나 지역의 여러 LAN 연결
- 여러 LAN을 연결하여 Backbone Line 형성
- 광섬유 또는 동축 케이블 사용
- 45Mbps, 100Mbps 속도 제공

### DQDB

```text
DQDB
→ Distributed Queue Dual Bus
→ IEEE 802.6
```

주요 특징:

```text
Dual Bus
→ 이중 버스

각 버스
→ 단방향
```

### 핵심

```text
MAN
→ 도시권 통신망
→ DQDB
→ IEEE 802.6
```

---

## 7. WAN

`WAN`은 **Wide Area Network**의 약자이며 원거리 통신망이다.

주요 특징:

- 국가, 대륙 등 넓은 지역 연결
- 거리 제한이 없음
- 여러 경로를 거치므로 속도가 느려지고 전송 오류율이 높을 수 있음

책에 나온 WAN 구성 방식:

```text
전용선
회선교환망
패킷교환망
```

---

# WAN 프로토콜

## 8. HDLC

HDLC의 주요 특징:

- Serial Interface의 기본 Encapsulation Type
- 같은 기종 간 동기식 Serial 연결 시 사용
- 3계층 Protocol이 일치해야 함

```text
HDLC
→ 같은 기종
→ 동기식 Serial
```

---

## 9. PPP

PPP의 주요 특징:

- Async, Sync Interface 모두 사용 가능
- 다른 기종 간 연결에 사용
- Multi Protocol 지원
- NCP(Network Control Protocol)
- LCP(Link Control Protocol)
- 인증, 압축, Call Back, Error Detect, Multilink 지원

```text
PPP
→ 다른 기종 연결
→ Async / Sync 모두 가능
→ NCP + LCP
```

---

## 10. X.25

X.25의 주요 특징:

- ITU-T 표준화 통신 규약
- 패킷망에서 DCE와 DTE 사이의 상호 작용에 사용
- 가변 길이 프레임 전송
- 저속 패킷 릴레이 방식

```text
X.25
→ ITU-T
→ DCE ↔ DTE
→ 패킷 교환
```

---

## 11. Frame Relay

Frame Relay의 주요 특징:

- 안정적인 데이터망 구축 이후 개발
- 속도에 초점을 둠
- Frame 단위로 전송
- 실시간 데이터 전송은 어려움

```text
Frame Relay
→ Frame 단위 전송
→ 속도 중심
```

---

## 12. ATM

ATM의 주요 특징:

- Frame을 Cell 단위로 나누어 전송
- 실시간 데이터 전송이 용이

Cell 크기:

```text
53 Byte
```

구성:

```text
48 Byte → Data
5 Byte  → Header
```

### 핵심

```text
ATM
→ Cell
→ 53 Byte
→ Data 48 + Header 5
```

---

## 13. SAN

`SAN`은 **Storage Area Network**의 약자이다.

스토리지를 위해 고안된 전용 고속 네트워크이다.

주요 특징:

- 저장장치 네트워크
- 파이버 채널을 이용하여 구성
- 대용량 데이터 전송 가능
- 서버가 파일 I/O 요청을 Block I/O로 변환하여 SAN 스토리지로 전달

### 핵심

```text
SAN
→ Storage Area Network
→ 저장장치 전용 고속 네트워크
→ Fiber Channel
→ Block I/O
```

---

# 핵심 비교

```text
LAN
→ Ethernet / Token Ring / FDDI

MAN
→ DQDB / IEEE 802.6

WAN
→ 전용선 / 회선교환망 / 패킷교환망

SAN
→ Storage / Fiber Channel / Block I/O
```

```text
Ethernet
→ IEEE 802.3
→ CSMA/CD

Token Ring
→ IEEE 802.5
→ Token Passing

MAN
→ IEEE 802.6
→ DQDB
```

```text
HDLC
→ 같은 기종
→ 동기식 Serial

PPP
→ 다른 기종
→ Async / Sync
```

```text
X.25
→ DCE / DTE

Frame Relay
→ Frame

ATM
→ Cell 53B
→ Data 48B + Header 5B
```

## 시험 직전 암기

```text
802.3 → Ethernet → CSMA/CD
802.5 → Token Ring → Token Passing
802.6 → MAN → DQDB
```

```text
HDLC = 같은 기종
PPP = 다른 기종
```

```text
ATM = 53 Byte
48 Data + 5 Header
```

```text
SAN = Storage
Fiber Channel
Block I/O
```
