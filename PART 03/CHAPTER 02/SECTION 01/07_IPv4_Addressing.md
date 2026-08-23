# IPv4 Addressing

## 1. IPv4 주소 구조

IPv4 주소는 **4개의 옥텟(Octet)**으로 구성된다.

```text
1 Octet = 8bit
4 Octet = 32bit = 4Byte
```

예:

```text
192.168.5.2
```

### 핵심

```text
IPv4
→ 4 Octet
→ 각 Octet 8bit
→ 총 32bit
```

---

# IPv4 Class

## 2. Class A

첫 번째 옥텟 범위:

```text
1 ~ 126
```

`127`은 Loopback 주소로 사용된다.

구조:

```text
Network | Host | Host | Host
```

기본 서브넷 마스크:

```text
255.0.0.0
```

### 핵심

```text
Class A
→ 1~126
→ Network 1옥텟
→ Host 3옥텟
→ 255.0.0.0
```

---

## 3. Class B

첫 번째 옥텟 범위:

```text
128 ~ 191
```

구조:

```text
Network | Network | Host | Host
```

기본 서브넷 마스크:

```text
255.255.0.0
```

### 핵심

```text
Class B
→ 128~191
→ Network 2옥텟
→ Host 2옥텟
→ 255.255.0.0
```

---

## 4. Class C

첫 번째 옥텟 범위:

```text
192 ~ 223
```

구조:

```text
Network | Network | Network | Host
```

기본 서브넷 마스크:

```text
255.255.255.0
```

### 핵심

```text
Class C
→ 192~223
→ Network 3옥텟
→ Host 1옥텟
→ 255.255.255.0
```

---

## 5. Class D

범위:

```text
224 ~ 239
```

용도:

```text
Multicast Group
```

### 핵심

```text
Class D
→ 224~239
→ Multicast
```

---

## 6. Class E

범위:

```text
240 ~ 255
```

책에서는 IP 주소 부족을 위해 예약해 둔 영역이라고 설명한다.

```text
Class E
→ 240~255
→ 예약 영역
```

---

# 클래스 범위 암기

```text
A → 1~126
127 → Loopback
B → 128~191
C → 192~223
D → 224~239
E → 240~255
```

기본 서브넷 마스크:

```text
A → 255.0.0.0
B → 255.255.0.0
C → 255.255.255.0
```

### 암기

```text
A = 255 한 개
B = 255 두 개
C = 255 세 개
```

---

# Network ID / Host ID

## 7. IP 주소 구성

IP 주소는 다음 두 부분으로 구성된다.

```text
Network ID
+
Host ID
```

```text
Network ID
→ 네트워크 주소

Host ID
→ 네트워크 내부의 호스트 주소
```

---

## 8. Subnet Mask

서브넷 마스크는 **Network 부분과 Host 부분을 구분하는 값**이다.

```text
Subnet Mask
→ Network / Host 구분
→ 효율적인 네트워크 분리
```

---

# 특수 네트워크 주소

## 9. Network 주소

Host ID의 모든 비트가 `0`인 주소이다.

네트워크 자체를 나타낸다.

예:

```text
192.168.1.0
```

### 핵심

```text
Host 부분 모두 0
→ Network 주소
```

---

## 10. Direct Broadcast 주소

Host ID의 모든 비트가 `1`인 주소이다.

특정 네트워크의 모든 호스트에게 패킷을 전달할 때 사용한다.

예:

```text
192.168.1.255
```

### 핵심

```text
Host 부분 모두 1
→ Direct Broadcast
```

---

## 11. Limited Broadcast 주소

주소:

```text
255.255.255.255
```

책에서는 DHCP 클라이언트가 DHCP 서버를 찾을 때 사용한다고 설명한다.

```text
255.255.255.255
→ Limited Broadcast
→ DHCP 서버 탐색
```

---

## 12. Loopback 주소

범위:

```text
127.0.0.0
~
127.255.255.255
```

주요 용도:

```text
자기 자신 내부 시험
```

### 핵심

```text
127.x.x.x
→ Loopback
→ 자기 자신 테스트
```

---

## 13. 0.0.0.0

책에서는 다음 상황에서 사용한다고 설명한다.

```text
부팅 시 자신의 IP 주소를 모르는 경우
```

```text
0.0.0.0
→ 자신의 IP 주소를 모를 때
```

---

# 사설 IP 주소

## 14. 사설 IP

사설 IP 주소는 공식적인 승인 없이 사용할 수 있으며 인터넷에서 직접 라우팅할 수 없는 주소이다.

### Class A

```text
10.0.0.0
~
10.255.255.255
```

### Class B

```text
172.16.0.0
~
172.31.255.255
```

### Class C

```text
192.168.0.0
~
192.168.255.255
```

### 핵심 암기

```text
A → 10

B → 172.16 ~ 172.31

C → 192.168
```

---

# 핵심 정리

```text
IPv4
→ 4 Octet
→ 32bit
```

```text
A → 1~126
→ 255.0.0.0

B → 128~191
→ 255.255.0.0

C → 192~223
→ 255.255.255.0

D → 224~239
→ Multicast

E → 240~255
→ 예약
```

```text
Host 모두 0
→ Network 주소

Host 모두 1
→ Direct Broadcast
```

```text
255.255.255.255
→ Limited Broadcast
→ DHCP 서버 탐색
```

```text
127.x.x.x
→ Loopback
```

```text
0.0.0.0
→ 자신의 IP를 모를 때
```

```text
사설 IP

10.0.0.0 ~ 10.255.255.255

172.16.0.0 ~ 172.31.255.255

192.168.0.0 ~ 192.168.255.255
```

## 시험 직전 암기

```text
A 1~126
127 Loopback
B 128~191
C 192~223
D 224~239
E 240~255
```

```text
A = 255 한 개
B = 255 두 개
C = 255 세 개
```

```text
Host 0 → Network
Host 1 → Broadcast
```

```text
Private IP
→ 10
→ 172.16~31
→ 192.168
```
