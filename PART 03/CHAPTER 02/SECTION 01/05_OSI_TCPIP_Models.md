# OSI 7 Layer & TCP/IP Model

## 1. OSI 참조 모델

OSI는 **Open System Interconnection**의 약자이다.

ISO가 서로 다른 시스템 간 통신을 위해 정의한 참조 모델이다.

네트워크 기능을 7개의 계층으로 나눈다.

```text
7 응용 계층
6 표현 계층
5 세션 계층
4 전송 계층
3 네트워크 계층
2 데이터링크 계층
1 물리 계층
```

아래에서 위로:

```text
물리
→ 데이터링크
→ 네트워크
→ 전송
→ 세션
→ 표현
→ 응용
```

---

## 2. 7계층 - 응용 계층

사용자에게 다양한 네트워크 서비스를 제공한다.

주요 기능:

```text
User Interface 제공
데이터 생성
네트워크 서비스 제공
```

### 핵심

```text
Application
→ 사용자 서비스
→ User Interface
```

---

## 3. 6계층 - 표현 계층

데이터의 표현 방식을 담당한다.

주요 기능:

```text
부호화(Encoding)
압축(Compression)
암호화(Encryption)
```

### 핵심

```text
Presentation
→ Encoding
→ Compression
→ Encryption
```

---

## 4. 5계층 - 세션 계층

종단 간 애플리케이션의 연결을 관리한다.

```text
연결 설정
연결 유지
연결 해제
```

### 핵심

```text
Session
→ 설정
→ 유지
→ 해제
```

---

## 5. 4계층 - 전송 계층

종단 간 연결을 담당한다.

주요 기능:

```text
End-to-End Connection
응용 계층 사이의 논리적 통로 제공
Virtual Circuit
```

### 핵심

```text
Transport
→ End-to-End
→ 논리적 통로
```

---

## 6. 3계층 - 네트워크 계층

논리적인 주소와 경로를 관리한다.

주요 기능:

```text
논리적 주소 사용
IP
경로 관리
최적 경로 결정
```

### 핵심

```text
Network
→ IP
→ 논리 주소
→ Routing
→ 최적 경로
```

---

## 7. 2계층 - 데이터링크 계층

데이터 전송 형식과 미디어 접근을 담당한다.

주요 기능:

```text
데이터 전송 형식 결정
미디어 접근 방식 제공
오류 검출 기능 제공
```

### 핵심

```text
Data Link
→ 데이터 형식
→ MAC
→ Media Access
→ 오류 검출
```

---

## 8. 1계층 - 물리 계층

물리적인 연결을 담당한다.

주요 기능:

```text
물리적 연결
전기적 수단
기계적 수단
기능적 수단
절차적 수단
```

### 핵심

```text
Physical
→ 실제 연결
→ 전기적 / 기계적
```

---

# TCP/IP Model

## 9. TCP/IP 4계층

책에서 TCP/IP 모델은 다음 4계층으로 구성된다.

```text
Application
Transport
Internet
Network Access
```

---

## 10. OSI와 TCP/IP 대응

| OSI 7계층 | TCP/IP 모델 |
|---|---|
| 응용 계층 | Application |
| 표현 계층 | Application |
| 세션 계층 | Application |
| 전송 계층 | Transport |
| 네트워크 계층 | Internet |
| 데이터링크 계층 | Network Access |
| 물리 계층 | Network Access |

### 핵심

```text
OSI 7 + 6 + 5
→ TCP/IP Application

OSI 4
→ TCP/IP Transport

OSI 3
→ TCP/IP Internet

OSI 2 + 1
→ TCP/IP Network Access
```

---

# 핵심 정리

```text
7 응용
→ 사용자 서비스

6 표현
→ 부호화 / 압축 / 암호화

5 세션
→ 설정 / 유지 / 해제

4 전송
→ End-to-End

3 네트워크
→ IP / 경로 / 최적 경로

2 데이터링크
→ MAC / 미디어 접근 / 오류 검출

1 물리
→ 실제 연결
```

```text
TCP/IP

Application
→ OSI 7, 6, 5

Transport
→ OSI 4

Internet
→ OSI 3

Network Access
→ OSI 2, 1
```

## 시험 직전 암기

```text
6계층
→ Encoding / Compression / Encryption

5계층
→ 설정 / 유지 / 해제

4계층
→ End-to-End

3계층
→ IP + Routing

2계층
→ MAC + 오류 검출

1계층
→ 물리 연결
```

```text
7,6,5 → Application
4 → Transport
3 → Internet
2,1 → Network Access
```
