# DNS Service

## 1. DNS 개념

`DNS`는 **Domain Name System**의 약자이다.

주요 기능:

```text
호스트 이름 → IP 주소 변환(조회)
IP 주소 → 호스트 이름 변환(조회)
```

### 핵심

```text
DNS
→ Host Name ↔ IP Address
```

---

## 2. DNS 구조

DNS에서는 도메인명을 **분산된 트리 형태의 계층적 구조**로 관리한다.

```text
Root Domain
    ↓
Top-Level Domain
    ↓
하위 도메인
    ↓
호스트
```

### 핵심

```text
DNS
→ 분산 구조
→ Tree 구조
→ 계층적 구조
```

---

# 최상위 도메인

## 3. 주요 최상위 도메인

| 도메인 | 의미 |
|---|---|
| `.org` | 비영리기관 |
| `.net` | 네트워크기관 |
| `.com` | 영리를 목적으로 하는 기관 |
| `.edu` | 교육기관 |
| `.gov` | 정부기관 |
| `.mil` | 군사기관 |
| `.int` | 국제 조약 등으로 만들어진 국제기관 |
| `.kr`, `.jp`, `.fr` | 국가기관 |

### 암기

```text
org → 비영리
net → 네트워크
com → 영리
edu → 교육
gov → 정부
mil → 군사
int → 국제기관
kr / jp / fr → 국가
```

---

## 4. gTLD

`gTLD`는 **generic Top-Level Domain**이다.

책에서는 특정 조직 계열에 따라 사용한다고 설명한다.

예:

```text
.org
.net
.com
.edu
.gov
.mil
.int
```

---

# DNS 조회 관련 파일

## 5. /etc/host.conf

호스트 이름에 대한 IP 주소 조회 시  
책의 흐름에서는 먼저 `/etc/host.conf`를 확인한다.

예:

```text
order hosts, bind
```

### 핵심

```text
/etc/host.conf
→ 조회 순서 확인
```

---

## 6. /etc/hosts

로컬에서 호스트 이름과 IP 주소 정보를 확인한다.

```text
/etc/hosts
→ 로컬 호스트 정보
```

책의 흐름:

```text
/etc/hosts에 정보 있음
→ IP 주소 획득
```

---

## 7. /etc/resolv.conf

`/etc/hosts`에서 정보를 찾지 못하면  
책의 흐름에서는 `/etc/resolv.conf`를 통해 네임서버 설정을 확인한다.

```text
/etc/resolv.conf
→ 네임서버 설정
```

---

# DNS 확인 명령어

## 8. nslookup / dig

DNS 설정 정보나 질의응답을 점검하기 위한 명령어:

```text
nslookup
dig
```

### 핵심

```text
nslookup
→ DNS 조회

dig
→ DNS 조회
```

---

# 핵심 정리

```text
DNS
→ Host Name ↔ IP Address
```

```text
DNS 구조
→ 분산
→ Tree
→ 계층 구조
```

```text
.org → 비영리
.net → 네트워크
.com → 영리
.edu → 교육
.gov → 정부
.mil → 군사
.int → 국제기관
.kr / .jp / .fr → 국가
```

```text
/etc/host.conf
→ 조회 순서

/etc/hosts
→ 로컬 호스트 정보

/etc/resolv.conf
→ 네임서버 설정
```

```text
DNS 확인
→ nslookup
→ dig
```

## 시험 직전 암기

```text
DNS = 이름 ↔ IP
```

```text
host.conf = 순서
hosts = 로컬
resolv.conf = DNS 서버
```

```text
nslookup / dig
= DNS 조회
```
