# Telnet & SSH Service

## 1. Telnet과 SSH의 공통점

Telnet과 SSH는 네트워크상의 다른 컴퓨터에 접속하여  
원격 시스템을 제어할 수 있는 서비스이다.

주요 기능:

```text
원격 로그인
명령 실행
파일 관리
Text Mode 환경
```

### 핵심

```text
Telnet / SSH
→ TCP/IP 기반 원격 접속
→ 원격 로그인
→ 명령 실행
```

---

# Telnet

## 2. Telnet의 특징

Telnet은 서버와 주고받는 정보를  
**Byte Stream 형식의 평문으로 전송**한다.

따라서 스니핑에 취약하다.

```text
Telnet
→ 평문 전송
→ Byte Stream
→ 스니핑에 취약
→ 보안 약함
```

기본 포트:

```text
23/tcp
```

---

## 3. Telnet 명령 형식

```bash
telnet [hostname]
```

책에 나온 옵션:

```text
-d
→ 디버깅 작동

-a
→ 자동 로그인 시도

-l user
→ 자동 로그인을 위해 사용자 이름을 원격 시스템으로 전송

port
→ 원격 시스템에 연결할 포트 번호 지정
```

포트를 지정하지 않으면:

```text
기본 Telnet Port
→ 23
```

---

## 4. Telnet을 이용한 서비스 확인

형식:

```bash
telnet 서버IP 포트번호
```

특정 인터넷 서비스의 활성화 여부를 확인할 수 있다.

예:

```bash
telnet 192.168.10.20 21
```

```text
21번 포트
→ FTP 서비스 활성 여부 확인
```

웹 서비스 확인:

```text
80번 포트
```

### 핵심

```text
telnet IP Port
→ 특정 서비스 포트의 활성 여부 확인
```

---

# SSH

## 5. SSH의 특징

SSH는 Telnet보다 안전한 원격 접속 서비스이다.

책에서는 DES, RSA 등의 암호화 기법을 사용한다고 설명한다.

주요 특징:

```text
세션 암호화
보안 강화
압축 기능 제공
```

기본 포트:

```text
22/tcp
```

### 핵심

```text
SSH
→ 암호화
→ 보안 강화
→ 압축 기능
→ 22/tcp
```

---

## 6. SSH 명령 형식

```bash
ssh [옵션] [서버IP주소|도메인명]
```

또는:

```bash
ssh [계정지정@서버IP주소]
```

예:

```bash
ssh target@192.168.10.20
```

---

## 7. SSH 옵션

### `-a`

```text
인증 에이전트의 전송을 불가능하게 함
```

### `-c`

```text
세션을 암호화하는 데 사용할 암호 해독기 선택
```

### `-p`

```text
원격 호스트에 연결할 포트 설정
```

### `-l`

```text
원격 시스템에서 사용할 로그인 이름 설정
```

### 시험 핵심

```text
-p
→ Port

-l
→ Login
```

---

# Telnet vs SSH

| 구분 | Telnet | SSH |
|---|---|---|
| 기본 포트 | 23/tcp | 22/tcp |
| 데이터 전송 | 평문 | 암호화 |
| 보안 | 약함 | 강함 |
| 원격 로그인 | 가능 | 가능 |
| 명령 실행 | 가능 | 가능 |
| 특징 | 스니핑에 취약 | 압축, 암호화 지원 |

---

# 핵심 정리

```text
Telnet
→ 평문
→ 보안 약함
→ 23/tcp
```

```text
SSH
→ 암호화
→ 보안 강함
→ 압축 지원
→ 22/tcp
```

```text
telnet IP Port
→ 특정 서비스 활성 여부 확인
```

```text
SSH 옵션

-a → 인증 에이전트 전송 금지
-c → 암호 방식 선택
-p → 포트 설정
-l → 로그인 이름 설정
```

## 시험 직전 암기

```text
SSH = 22
Telnet = 23
```

```text
Telnet = 평문
SSH = 암호화
```

```text
-p = Port
-l = Login
```
