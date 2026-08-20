# Printer Setup

## 1. LPRng

`LPRng`는 **Line Printer next generation**의 약자이다.

리눅스 초기에 사용되던 인쇄 시스템이다.

주요 특징:

- BSD 계열 유닉스에서 사용
- 라인 프린터 데몬 프로토콜 사용
- 프린터 스풀링 지원
- 네트워크 프린터 서버 지원

설정 파일:

```text
/etc/printcap
```

사용 포트:

```text
515
```

### 핵심

```text
LPRng
→ 초기 리눅스 인쇄 시스템
→ /etc/printcap
→ 515 포트
```

---

## 2. CUPS

`CUPS`는 **Common Unix Printing System**의 약자이다.

주요 특징:

- 오픈 소스 프린팅 시스템
- 유닉스 계열 운영체제의 프린터 서버로 사용 가능
- 다양한 프린터 지원
- HTTP 기반의 IPP 사용
- 웹 기반으로 프린터 제어
- 사용자 및 호스트 기반 인증 제공

사용 포트:

```text
631
```

설정 디렉토리:

```text
/etc/cups
```

### 핵심

```text
CUPS
→ Common Unix Printing System
→ IPP 사용
→ 631 포트
→ /etc/cups
```

---

## 3. CUPS 관련 파일

| 파일 | 기능 |
|---|---|
| `/etc/cups/cupsd.conf` | 프린터 데몬 환경 설정 |
| `/etc/cups/printers.conf` | 프린터 큐 관련 설정 |
| `/etc/cups/classes.conf` | 프린터 클래스 설정 |
| `cupsd` | CUPS 프린터 데몬 |

### 핵심

```text
cupsd.conf
→ 데몬 설정

printers.conf
→ 프린터 큐 설정

classes.conf
→ 클래스 설정

cupsd
→ 프린터 데몬
```

---

## 4. 프린터 설정 도구

X-Window에서 프린터 설정 도구를 사용할 수 있다.

```text
system-config-printer
```

프린터 설정 도구 사용 시 root 권한이 필요하다.

---

## 5. 로컬 프린터 연결

책에 나온 장치 파일:

```text
직렬 포트
→ /dev/lp0

USB 포트
→ /dev/usb/lp0
```

CUPS 웹 설정:

```text
http://localhost:631
```

---

## 6. 네트워크 프린터 연결

책에 나온 연결 방식:

```text
AppSocket / HP Jetdirect
LPD / LPR 호스트 또는 프린터
Windows Printer via SAMBA
인터넷 프린터 프로토콜(https)
인터넷 프린터 프로토콜(ipp)
```

특히 다음 연결을 기억한다.

```text
Windows Printer via SAMBA
→ SMB
```

```text
CUPS
→ IPP
→ 631
```

---

## 7. LPRng와 CUPS 비교

| 구분 | LPRng | CUPS |
|---|---|---|
| 특징 | 초기 리눅스 인쇄 시스템 | Common Unix Printing System |
| 설정 위치 | `/etc/printcap` | `/etc/cups` |
| 포트 | `515` | `631` |
| 관련 방식 | LPD/LPR | IPP |

---

# 핵심 정리

```text
LPRng
→ /etc/printcap
→ 515
```

```text
CUPS
→ /etc/cups
→ IPP
→ 631
```

```text
cupsd.conf
→ 데몬 설정

printers.conf
→ 프린터 큐

classes.conf
→ 클래스
```

```text
직렬
→ /dev/lp0

USB
→ /dev/usb/lp0
```

```text
Windows Printer via SAMBA
→ SMB
```

## 시험 직전 암기

```text
LPRng = 515
CUPS = 631

LPRng = /etc/printcap
CUPS = /etc/cups

CUPS = IPP
SAMBA = SMB
```
