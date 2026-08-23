# Mail Service

## 1. 전자 메일 시스템 구성

전자 메일 시스템은 다음 요소로 구성된다.

```text
MTA
MUA
MDA
```

---

## 2. MTA

`MTA`는 **Mail Transfer Agent**의 약자이다.

자신에 등록되어 있는 메일 서버에서 `SMTP`를 사용하여 메일을 전달한다.

### 핵심

```text
MTA
→ Mail Transfer Agent
→ 메일 전달
→ SMTP 사용
```

---

## 3. MUA

`MUA`는 **Mail User Agent**의 약자이다.

사용자가 메일을 작성하고 읽을 수 있도록 하는 사용자 인터페이스이다.

### 핵심

```text
MUA
→ Mail User Agent
→ 메일 작성
→ 메일 읽기
→ 사용자 인터페이스
```

---

## 4. MDA

`MDA`는 **Mail Delivery Agent**의 약자이다.

메일 서버에서 수신한 메일을 분류한 후 해당 수신자의 메일박스로 전달한다.

### 핵심

```text
MDA
→ Mail Delivery Agent
→ 수신 메일 분류
→ 수신자 메일박스로 전달
```

---

# 메일 프로토콜

## 5. SMTP

메일을 보내거나 메일 서버 사이에서 메시지를 교환할 때 사용한다.

```text
SMTP
→ 메일 송신
→ 메일 서버 간 메시지 전달
```

메일 흐름에서:

```text
MUA → MTA
MTA → MTA
```

구간에서 사용된다.

---

## 6. POP3 / IMAP

메일 서버에 도착한 메일을 사용자 컴퓨터에서 확인할 때 사용한다.

```text
POP3
IMAP
→ 메일 수신
→ 도착한 메일 확인
```

### 핵심 비교

```text
SMTP
→ 보내기

POP3 / IMAP
→ 받기
```

---

## 7. 메일 전송 흐름

```text
송신 사용자 MUA
        ↓
      SMTP
        ↓
       MTA
        ↓
      SMTP
        ↓
    상대방 MTA
        ↓
       MDA
        ↓
     메일박스
        ↓
   POP3 / IMAP
        ↓
수신 사용자 MUA
```

---

## 8. MIME

`MIME`은 **Multipurpose Internet Mail Extension**의 약자이다.

멀티미디어 전자우편을 위한 표준으로, SMTP의 확장 규격이다.

책에서는 멀티미디어 데이터를 ASCII 형식으로 변환할 필요 없이 인터넷 전자우편으로 송신할 수 있도록 하는 규격이라고 설명한다.

### 핵심

```text
MIME
→ Multipurpose Internet Mail Extension
→ 멀티미디어 전자우편
→ SMTP 확장 규격
```

---

# 핵심 정리

```text
MTA
→ Transfer
→ 메일 전달

MUA
→ User
→ 사용자가 메일 작성 / 읽기

MDA
→ Delivery
→ 수신자의 메일박스로 전달
```

```text
SMTP
→ 송신

POP3 / IMAP
→ 수신
```

```text
MIME
→ 멀티미디어 메일
→ SMTP 확장 규격
```

## 시험 직전 암기

```text
MTA = Transfer
MUA = User
MDA = Delivery
```

```text
SMTP = 보내기
POP3 / IMAP = 받기
```

```text
MIME = Multimedia Mail
```
