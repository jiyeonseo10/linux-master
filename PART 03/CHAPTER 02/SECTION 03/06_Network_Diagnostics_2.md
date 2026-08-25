# Network Diagnostic Commands 2

## 1. nslookup

`nslookup`은 **인터넷 도메인 네임서버에 특정 호스트에 대한 정보를 질의하는 대화식 명령어**이다.

형식:

```bash
nslookup [-type=레코드] [호스트명]
```

예:

```bash
nslookup youngjin.com
```

### 핵심

```text
nslookup
→ DNS 네임서버 질의
→ 특정 호스트 정보 확인
```

---

# netstat

## 2. netstat

`netstat`은 다음과 같은 네트워크 정보를 확인할 수 있는 명령어이다.

```text
전송 제어 프로토콜
라우팅 테이블
네트워크 인터페이스
네트워크 프로토콜 통계
네트워크 연결 상태
```

---

## 3. netstat 옵션

### `-r`

```text
라우팅 테이블 내용 표시
```

```text
-r = Routing
```

---

### `-e`

```text
랜카드에서 송신한 패킷의 용량 및 종류 확인
```

---

### `-n`

```text
IP 주소 형태로 주소와 포트번호 표시
```

```text
-n
→ 숫자 형태의 주소 / 포트
```

---

### `-i`

```text
인터페이스 정보 출력
```

```text
-i = Interface
```

---

### `-s`

```text
각종 프로토콜 상태 표시
IP, ICMP, TCP, UDP의 통계치 표시
```

```text
-s = Statistics
```

---

### `-c`

```text
1초 단위로 표시
```

---

### `-l`

```text
현재 LISTEN 중인 소켓 정보 표시
```

```text
-l = Listen
```

---

### `-a`

```text
현재 다른 호스트와 연결되어 있거나
대기 중인 모든 포트 번호 표시
```

```text
-a = All
```

---

# NIC 상태 확인

## 4. mii-tool

`mii-tool`은 **네트워크 인터페이스의 속도와 전송 모드 등을 확인**할 수 있다.

예:

```bash
mii-tool eth0
```

확인 예:

```text
속도
전송 모드
Link 상태
```

### 핵심

```text
mii-tool
→ NIC 속도
→ 전송 모드
```

---

## 5. ethtool

`ethtool`은 **네트워크 인터페이스의 물리적인 연결 여부**를 확인할 수 있다.

또한 책에서는 `mii-tool`보다 더 상세한 네트워크 인터페이스 상태 정보를 확인할 수 있다고 설명한다.

예:

```bash
ethtool eth0
```

확인 가능한 정보 예:

```text
Speed
Duplex
Port
Auto-negotiation
Link detected
```

### 핵심

```text
ethtool
→ NIC 물리적 연결 여부
→ 상세한 인터페이스 상태
→ mii-tool보다 상세
```

---

# ARP

## 6. arp

`arp` 명령어는 시스템이 가지고 있는 **ARP 테이블을 확인하고 추가·삭제**할 때 사용한다.

```text
arp
→ ARP Table 관리
```

---

## 7. arp -a

```bash
arp -a
```

기능:

```text
ARP 테이블 확인
```

### 핵심

```text
-a
→ ARP Table 확인
```

---

## 8. arp -s

형식:

```bash
arp -s IP주소 MAC주소
```

기능:

```text
지정한 IP 주소와 MAC 주소를
ARP 테이블에 추가
```

### 핵심

```text
-s
→ IP + MAC 추가
```

---

# 핵심 비교

```text
nslookup
→ DNS 조회
```

```text
netstat
→ 네트워크 연결 상태
→ 라우팅
→ 인터페이스
→ 프로토콜 통계
```

```text
mii-tool
→ NIC 속도 / 전송 모드
```

```text
ethtool
→ NIC 물리적 연결 여부
→ 상세 NIC 정보
```

```text
arp
→ ARP 테이블 관리
```

---

# netstat 옵션 암기

```text
-r → Routing Table
-e → 송신 패킷 용량 / 종류
-n → IP 주소 형태로 주소 / 포트 표시
-i → Interface
-s → Statistics
-c → 1초 단위
-l → Listen
-a → All
```

---

# 시험 직전 암기

```text
nslookup = DNS
```

```text
netstat

-r = Routing
-n = 숫자
-i = Interface
-s = Statistics
-l = Listen
-a = All
```

```text
mii-tool
→ 속도 / 전송 모드

ethtool
→ 물리 연결 / 상세 정보
```

```text
arp -a
→ ARP 테이블 확인

arp -s IP MAC
→ ARP 테이블에 추가
```
