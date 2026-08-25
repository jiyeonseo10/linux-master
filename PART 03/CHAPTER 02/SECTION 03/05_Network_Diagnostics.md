# Network Diagnostics

## 1. ifconfig

`ifconfig`는 네트워크 인터페이스의 설정 또는 상태를 확인하는 시스템 관리 유틸리티이다.

```bash
ifconfig -a
```

주요 확인 항목:

```text
eth0
→ 이더넷 인터페이스명

lo
→ 루프백 인터페이스명

HWaddr
→ MAC 주소

inet addr
→ IP 주소

Bcast
→ 브로드캐스트 주소

Mask
→ 서브넷 마스크

UP / DOWN
→ 인터페이스 운영 상태

TX
→ 송신 패킷 수

RX
→ 수신 패킷 수
```

### 핵심

```text
ifconfig
→ 네트워크 인터페이스 설정 / 확인
```

---

## 2. ping

`ping`은 특정 호스트 또는 네트워크 장비까지  
**통신 가능 여부를 점검하는 ICMP 기반 명령어**이다.

예:

```bash
ping youngjin.com
```

확인 가능한 내용:

```text
통신 가능 여부
응답 시간
패킷 손실
```

### 핵심

```text
ping
→ 통신 가능 여부
→ ICMP 기반
```

---

## 3. traceroute

`traceroute`는 특정 호스트나 네트워크 장비까지  
패킷이 어떤 통신 경로를 거쳐 전달되는지 확인한다.

예:

```bash
traceroute youngjin.com
```

확인 가능한 내용:

```text
목적지까지의 통신 경로
Hop 수
통신 장애 구간
```

### 핵심

```text
traceroute
→ 경로 확인
→ Hop 수 확인
→ 장애 구간 확인
```

---

## 4. route

`route`는 라우팅 테이블을 확인하거나 변경할 때 사용한다.

주요 기능:

```text
라우팅 테이블 확인
게이트웨이 주소 확인
라우팅 정보 확인 / 변경
```

### 핵심

```text
route
→ Routing Table
→ Gateway 확인
```

---

# 핵심 비교

```text
ifconfig
→ 인터페이스 상태 / 설정

ping
→ 통신 가능한가?

traceroute
→ 어떤 경로로 가는가?

route
→ 어떤 경로가 설정되어 있는가?
```

---

# 책의 네트워크 진단 명령어 분류

```text
TCP/IP 주소 설정 정보 확인
→ ifconfig, nslookup

네트워크 경로 상태 확인
→ ping, traceroute

네트워크 연결 상태 확인
→ netstat

라우팅 테이블 확인
→ route

NIC 상태 확인
→ ethtool, mii-tool, arp
```

---

## 시험 직전 암기

```text
ifconfig = 인터페이스
ping = 통신 여부 + ICMP
traceroute = 경로 + Hop
route = 라우팅 테이블 + Gateway
```

```text
TX = 송신
RX = 수신
HWaddr = MAC 주소
```
