# Network Protocols

## 1. 프로토콜의 개념

프로토콜(Protocol)은 **특정 통신 기능을 수행하기 위한 통신 규약**이다.

두 노드 사이에서 정보를 교환할 때 통신 오류를 줄이기 위한 규칙이다.

프로토콜의 구성 요소:

```text
Syntax
Semantic
Timing
```

### Syntax

```text
형식
→ 데이터 포맷
→ 부호화
→ 신호 레벨
```

### Semantic

```text
의미
→ 데이터를 어떻게 해석할지 결정
→ 어떤 동작을 할지 결정
→ 오류 처리 및 제어 정보
```

### Timing

```text
순서
→ 속도 일치
→ 순서 제어
```

---

# 인터넷 / 네트워크 계층 프로토콜

## 2. IP

IP의 주요 특징:

```text
비연결형
비신뢰성
논리 주소 지정
단편화 및 재조립
```

MTU보다 큰 데이터는 단편화하여 처리한다.

```text
IP
→ 논리 주소
→ 비연결
→ 비신뢰
→ Fragmentation / Reassembly
```

---

## 3. ICMP

`ICMP`는 **Internet Control Message Protocol**이다.

주요 기능:

```text
오류 상황 보고
질의 메시지
Echo / Reply
```

```text
ICMP
→ IP 전송 과정의 오류 및 문제 보고
```

---

## 4. IGMP

`IGMP`는 **Internet Group Management Protocol**이다.

주요 기능:

```text
멀티캐스트 그룹 제어
라우터와 호스트의 그룹 관리
TTL 제공
```

```text
IGMP
→ Multicast Group 관리
```

---

## 5. ARP

`ARP`는 **Address Resolution Protocol**이다.

```text
IP 주소
→ MAC 주소
```

### ARP 통신

```text
ARP Request
→ Broadcast

ARP Reply
→ Unicast
```

### 핵심

```text
ARP
→ IP → MAC
```

---

## 6. RARP

`RARP`는 **Reverse Address Resolution Protocol**이다.

```text
MAC 주소
→ IP 주소
```

### ARP와 비교

```text
ARP
→ IP → MAC

RARP
→ MAC → IP
```

---

# 전송 계층 프로토콜

## 7. TCP

`TCP`는 **Transmission Control Protocol**이다.

주요 특징:

```text
연결 지향
신뢰성 있는 전송
송수신 전 연결 필요
UDP보다 상대적으로 느림
```

동작:

```text
연결 설정
→ 데이터 전송
→ 연결 해제
```

---

## 8. TCP 3-Way Handshaking

TCP 연결 설정 과정:

```text
SYN
→ SYN + ACK
→ ACK
```

### 상태

```text
LISTEN
→ 서버가 요청을 기다리는 상태

SYN_SENT
→ 클라이언트가 SYN 전송

SYN_RECEIVED
→ 서버가 요청을 받고 응답

ESTABLISHED
→ 연결 완료
```

### 핵심

```text
TCP 연결
→ 3-Way Handshaking
```

---

## 9. TCP 4-Way Handshaking

TCP 연결 해제 과정:

```text
FIN
→ ACK
→ FIN
→ ACK
```

주요 상태:

```text
FIN_WAIT1
FIN_WAIT2
TIME_WAIT
LAST_ACK
CLOSED
```

### 핵심

```text
TCP 연결 해제
→ 4-Way Handshaking
```

---

## 10. UDP

`UDP`는 **User Datagram Protocol**이다.

주요 특징:

```text
비연결 지향
비신뢰성
연결 설정 없이 데이터 송신
수신측 승인 없이 연속 전송
빠른 전송 속도
소량 데이터 송신에 적합
Multicast / Broadcast에 적합
```

### 핵심

```text
UDP
→ 비연결
→ 비신뢰
→ 빠름
```

---

## 11. TCP와 UDP 비교

| 구분 | TCP | UDP |
|---|---|---|
| 연결 | 연결 지향 | 비연결 지향 |
| 신뢰성 | 높음 | 낮음 |
| 속도 | 상대적으로 느림 | 빠름 |
| 연결 설정 | 필요 | 불필요 |

```text
TCP
→ 연결 + 신뢰성

UDP
→ 비연결 + 빠른 속도
```

---

# 응용 계층 프로토콜

## 12. SMTP

`SMTP`는 **Simple Mail Transfer Protocol**이다.

```text
전자우편 송신
→ Port 25
```

---

## 13. POP

`POP`는 **Post Office Protocol**이다.

```text
전자우편 수신 / 보관
→ Port 110
```

---

## 14. Telnet

주요 특징:

```text
원격 컴퓨터 접속
CUI 기반
보안 기능이 약함
```

```text
Telnet
→ Port 23
```

---

## 15. SSH

주요 특징:

```text
Telnet보다 보안 강화
원격 접속
전송 데이터 암호화
```

```text
SSH
→ Port 22
```

---

## 16. FTP

FTP는 서버/클라이언트 기반 파일 전송 프로토콜이다.

```text
FTP
→ Port 20, 21
```

---

## 17. HTTP

WWW에서 서버와 클라이언트 사이의 정보 교환을 담당한다.

```text
HTTP
→ Port 80
```

---

## 18. SNMP

`SNMP`는 **Simple Network Management Protocol**이다.

주요 기능:

```text
네트워크 장비 관리
네트워크 장비 감시
장비 상태 확인
원격 관리
```

```text
SNMP
→ Port 161, 162
```

---

## 19. TFTP

TFTP는 FTP보다 단순화된 파일 전송 프로토콜이다.

주요 특징:

```text
UDP 기반
데이터 손실 가능
```

```text
TFTP
→ Port 69
```

---

## 20. DHCP

`DHCP`는 **Dynamic Host Configuration Protocol**이다.

호스트에 다음과 같은 네트워크 정보를 할당한다.

```text
IP 주소
Gateway 주소
DNS 주소
```

```text
DHCP
→ Port 67, 68
```

---

# 핵심 정리

```text
Syntax → 형식
Semantic → 의미
Timing → 순서
```

```text
IP
→ 비연결 / 비신뢰 / 논리주소 / 단편화

ICMP
→ 오류 보고

IGMP
→ Multicast Group

ARP
→ IP → MAC

RARP
→ MAC → IP
```

```text
TCP
→ 연결 지향
→ 신뢰성
→ 3-Way 연결
→ 4-Way 해제

UDP
→ 비연결
→ 비신뢰
→ 빠름
```

## 포트번호 암기

```text
SSH     → 22
Telnet  → 23
SMTP    → 25
FTP     → 20, 21
DHCP    → 67, 68
TFTP    → 69
HTTP    → 80
POP     → 110
SNMP    → 161, 162
```

## 시험 직전 암기

```text
ARP  = IP → MAC
RARP = MAC → IP
```

```text
TCP 연결
SYN → SYN/ACK → ACK

TCP 해제
FIN → ACK → FIN → ACK
```

```text
22 SSH
23 Telnet
25 SMTP
69 TFTP
80 HTTP
110 POP
161/162 SNMP
67/68 DHCP
20/21 FTP
```
