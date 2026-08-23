# Subnetting & IPv6

## 1. 서브넷팅(Subnetting)

서브넷팅은 **하나의 네트워크를 여러 개의 네트워크로 분리하여 브로드캐스트 도메인을 나누는 것**이다.

주요 목적:

```text
하나의 네트워크를 여러 네트워크로 분리
브로드캐스트 도메인 분리
IP 주소 부족 현상 완화
```

### 핵심 원리

기본 서브넷 마스크를 기준으로:

```text
Network ID 비트 수 증가
Host ID 비트 수 감소
```

기존 Host 영역에서 빌려온 비트가 **Subnet ID**가 된다.

```text
Subnetting
→ Network bit ↑
→ Host bit ↓
→ Subnet ID 생성
```

---

## 2. 서브넷팅 예제

책의 예:

```text
IP 주소
207.46.230.0

기본 서브넷 마스크
255.255.255.0
```

서브넷팅 후:

```text
255.255.255.224
```

마지막 옥텟:

```text
224
→ 11100000
```

앞의 `1`이 3개이므로:

```text
Subnet ID bit
→ 3bit
```

네트워크 개수:

```text
2³
→ 8개
```

### 핵심

```text
255.255.255.224
→ 11100000
→ Subnet bit 3개
→ 2³ = 8개 네트워크
```

---

# IPv4와 IPv6 비교

## 3. 주소 길이

```text
IPv4
→ 32bit

IPv6
→ 128bit
```

---

## 4. 주소 방식

책의 비교표 기준:

### IPv4

```text
지정 주소 방식
일반주소
브로드캐스트 주소
```

### IPv6

```text
자동 설정 주소 방식
유니캐스트
멀티캐스트
애니캐스트
```

---

## 5. IP 헤더 길이

### IPv4

```text
20Byte
~
60Byte
```

### IPv6

```text
기본 헤더 40Byte
+
확장 필드
```

IPv6의 확장 필드를 이용한 기능:

```text
압축
인증
QoS
보안
```

---

# IPv6 주소 표현

## 6. IPv6 기본 구조

IPv6 주소는:

```text
128bit
```

이며 `:`으로 구분된 16진수 8개 그룹으로 표현한다.

형식:

```text
X:X:X:X:X:X:X:X
```

예:

```text
21DA:00D3:0000:2F3B:02AA:00FF:FE28:9C5A
```

또한:

```text
대소문자를 구별하지 않음
```

### 핵심

```text
IPv6
→ 128bit
→ 16진수
→ 8개 그룹
→ : 로 구분
```

---

## 7. 앞자리 0 생략

각 그룹에서 앞쪽의 `0`은 생략할 수 있다.

예:

```text
21DA:00D3:0000:2F3B:02AA:00FF:FE28:9C5A
```

↓

```text
21DA:D3:0:2F3B:2AA:FF:FE28:9C5A
```

---

## 8. 연속된 0 축약

연속된 `0` 필드는:

```text
::
```

로 줄여 쓸 수 있다.

중요:

```text
:: 는 하나의 IPv6 주소에서 한 번만 사용 가능
```

### 핵심

```text
연속된 0
→ ::

:: 사용
→ 한 주소에서 한 번만
```

---

# IPv6 Prefix

## 9. Prefix 표현

IPv6는 IPv4처럼 점으로 표현된 서브넷 마스크를 사용하지 않는다.

대신 Prefix 길이를 표시한다.

형식:

```text
IPv6주소/Prefix길이
```

예:

```text
21DA:00D3:0000:2F3B::/64
```

### 핵심

```text
IPv6
→ Subnet Mask 대신 Prefix 길이 사용
```

---

# IPv6 특수 주소

## 10. Unspecified 주소

형식:

```text
0:0:0:0:0:0:0:0
```

축약:

```text
::
```

IPv4의 다음 주소와 같은 의미이다.

```text
0.0.0.0
```

### 핵심

```text
::
→ Unspecified
→ IPv4의 0.0.0.0
```

---

## 11. Loopback 주소

형식:

```text
0:0:0:0:0:0:0:1
```

축약:

```text
::1
```

IPv4의 다음 주소와 같은 의미이다.

```text
127.0.0.1
```

### 핵심

```text
::1
→ Loopback
→ IPv4의 127.0.0.1
```

---

# 핵심 정리

```text
Subnetting
→ Network bit 증가
→ Host bit 감소
→ Subnet ID 생성
```

```text
255.255.255.224
→ 11100000
→ Subnet bit 3개
→ 8개 네트워크
```

```text
IPv4
→ 32bit

IPv6
→ 128bit
```

```text
IPv6
→ 16진수
→ : 구분
→ 8개 그룹
→ 대소문자 구분 안 함
```

```text
연속 0
→ ::

:: 는 한 주소에서 한 번만 사용
```

```text
IPv6
→ 서브넷 마스크 대신 Prefix 사용
```

```text
::
→ Unspecified
→ 0.0.0.0

::1
→ Loopback
→ 127.0.0.1
```

## 시험 직전 암기

```text
서브넷팅
= Host bit 빌려서 Network bit 증가
```

```text
224
= 11100000
= Subnet 3bit
= 2³ = 8
```

```text
IPv6
= 128bit
= 16진수 8그룹
= 콜론(:)
```

```text
::  = Unspecified
::1 = Loopback
```
