# FTP Service

## 1. FTP 개념

`FTP`는 **File Transfer Protocol**의 약자이다.

TCP/IP에 의해 제공되며 **호스트 간 파일 복사**를 위한 프로토콜이다.

```text
FTP
→ File Transfer Protocol
→ 호스트 간 파일 전송
```

---

## 2. FTP 포트 번호

책에서는 FTP가 다음 두 포트를 사용한다고 설명한다.

```text
20번
→ 일반 데이터 전송용

21번
→ 제어 데이터 전송용
```

### 핵심

```text
FTP
20 = Data
21 = Control
```

---

# FTP 통신 모드

## 3. Passive Mode

패시브 모드는 **FTP 서버가 지정해 준 포트로 클라이언트가 접속**하는 방식이다.

흐름:

```text
Client
→ Server의 21번 포트로 접속 요청

Server
→ Data 전송을 위한 임의 포트 정보 제공

Client
→ 서버가 지정한 포트로 접속
→ Data 전송
```

### 핵심

```text
Passive
→ 서버가 포트 지정
→ Client → Server
```

---

## 4. Active Mode

액티브 모드는 **클라이언트가 요청한 포트로 FTP 서버가 데이터를 전송**하는 방식이다.

흐름:

```text
Client
→ Server의 21번 포트로 접속 요청

Client
→ Data 전송을 위한 임의 포트 정보 제공

Server
→ 제공받은 포트로 접속
→ 20번 포트를 이용하여 Data 전송
```

### 핵심

```text
Active
→ 클라이언트가 포트 제공
→ Server → Client
→ 서버의 20번 포트 사용
```

---

## 5. Passive와 Active 비교

```text
Passive
→ 서버가 데이터 포트 지정
→ 클라이언트가 서버로 접속
```

```text
Active
→ 클라이언트가 데이터 포트 지정
→ 서버가 클라이언트로 접속
→ 서버 20번 포트 사용
```

### 시험 암기

```text
Passive
→ Client가 찾아감

Active
→ Server가 찾아감
```

---

# Anonymous FTP

## 6. 익명 로그인

FTP는 계정을 가진 사용자뿐 아니라 **Anonymous 로그인**도 허용할 수 있다.

책에서는 공개 소프트웨어를 제공하는 FTP 서버에 접속할 때 사용할 수 있는 계정이라고 설명한다.

```text
Name:
anonymous
```

책의 예에서는 Password 부분에서:

```text
Enter
```

를 입력한다.

### 핵심

```text
Anonymous FTP
→ 익명 로그인
→ 공개 소프트웨어 제공 FTP 서버 등에 사용
```

---

# FTP 명령어

## 7. open

호스트 이름이나 IP 주소를 사용하여 FTP 서버에 접속한다.

```bash
open 192.168.10.20
```

```text
open
→ FTP 서버 접속
```

---

## 8. close

현재 접속 중인 연결을 끊고 FTP 명령어 모드로 돌아간다.

```text
close
→ 접속 종료
```

---

## 9. ascii

ASCII 형태로 파일을 송수신한다.

```text
ascii
→ ASCII 전송
```

---

## 10. binary

Binary 형태로 파일을 송수신한다.

```text
binary
→ Binary 전송
```

---

## 11. (m)get

FTP 서버로부터 파일을 전송받는다.

```text
get
→ 서버에서 받기

mget
→ 여러 파일 받기
```

---

## 12. (m)put

자신의 시스템에 있는 파일을 FTP 서버로 전송한다.

```text
put
→ 서버로 보내기

mput
→ 여러 파일 보내기
```

---

## 13. hash

파일의 전송 상태를 `#` 문자로 확인한다.

```text
hash
→ #로 전송 상태 표시
```

---

## 14. delete

FTP 서버의 파일을 삭제한다.

```text
delete
→ 서버 파일 삭제
```

---

# 핵심 정리

```text
FTP
→ 파일 전송
→ TCP/IP 기반
```

```text
20
→ Data

21
→ Control
```

```text
Passive
→ 서버가 포트 지정
→ Client → Server

Active
→ 클라이언트가 포트 지정
→ Server → Client
→ 20번 포트
```

```text
anonymous
→ 익명 로그인
```

```text
open
→ 접속

close
→ 접속 종료

ascii
→ ASCII 전송

binary
→ Binary 전송

get / mget
→ 받기

put / mput
→ 보내기

hash
→ #로 상태 확인

delete
→ 서버 파일 삭제
```

## 시험 직전 암기

```text
FTP = 20 Data / 21 Control

Passive = Client가 Server로
Active = Server가 Client로

get = 받기
put = 보내기

hash = #
```
