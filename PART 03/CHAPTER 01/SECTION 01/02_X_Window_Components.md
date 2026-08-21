# X Window Components

## 1. XProtocol

`XProtocol`은 **X 서버와 X 클라이언트 사이의 메시지 타입과 메시지 교환 방법을 규정**한다.

메시지 유형:

```text
request → 요구
reply   → 응답
error   → 오류
event   → 입력 발생
```

### 핵심

```text
XProtocol
→ X Server ↔ X Client 메시지 교환 규칙
```

---

## 2. Xlib

`Xlib`는 **XProtocol을 지원하는 클라이언트 라이브러리**이다.

책에서는 C나 Lisp 언어로 만들어졌다고 설명한다.

주요 기능:

```text
윈도우 생성
이벤트 처리
창 조회
키보드 처리
```

### 핵심

```text
Xlib
→ XProtocol 지원 클라이언트 라이브러리
```

---

## 3. XCB

`XCB`는 **Xlib를 대체하기 위해 등장한 클라이언트 라이브러리**이다.

주요 특징:

- Xlib보다 향상된 스레드 기능 지원
- 확장성이 뛰어남
- 라이브러리 크기가 작고 단순
- XProtocol에 직접 접근 가능

### 핵심

```text
XCB
→ Xlib 대체
→ 작고 단순
→ 향상된 스레드 기능
→ XProtocol 직접 접근
```

---

## 4. Xtoolkit

`Xtoolkit`은 Xlib로 스크롤바, 메뉴, 버튼 등의 GUI를 직접 만들 때 발생하는 비효율성을 줄이기 위해 사용하는 도구이다.

고급 레벨의 GUI 생성 시 사용한다.

### Widget

```text
Widget
→ 스크롤바, 메뉴 등 GUI를 구성하는 객체(Object)
```

### Xt Intrinsic

```text
Xt Intrinsic
→ Widget과 Xlib의 기본 함수 집합
```

책에 나온 다른 툴킷:

```text
XView
Xaw
Motif
Qt
GTK
```

### 핵심

```text
Xtoolkit
→ 고급 GUI 생성

Widget
→ GUI 구성 객체
```

---

## 5. XFree86

`XFree86`은 **Intel x86 계열의 유닉스 운영체제에서 동작하는 X 서버**이다.

```text
XFree86
→ Intel x86 계열
→ X Server
```

---

## 6. XF86Config

`XF86Config`는 **XFree86의 설정 파일**이다.

X 서버는 `XF86Config` 파일을 찾아 읽는다.

책에 나온 파일 위치:

```text
/etc/X11
또는
/usr/X11R6/lib/X11
```

설정 정보:

```text
폰트
키보드
모니터
마우스
비디오 카드
색상
```

### 핵심

```text
XF86Config
→ XFree86 설정 파일
```

---

## 7. X 환경 설정 도구

### Xconfigurator

```text
Xconfigurator
→ 텍스트 터미널에서 사용하는 X 환경 설정
```

### XF86Config

```text
XF86Config
→ X를 위한 기본 환경 설정
→ 텍스트 터미널에서 실행
```

### XF86Setup

```text
XF86Setup
→ X-윈도우 환경 설정
```

---

# 핵심 정리

```text
XProtocol
→ 서버 ↔ 클라이언트 메시지 교환 규칙

Xlib
→ XProtocol 지원 클라이언트 라이브러리

XCB
→ Xlib 대체 라이브러리

Xtoolkit
→ 고급 GUI 생성

Widget
→ GUI 구성 객체

XFree86
→ x86 계열 X 서버

XF86Config
→ XFree86 설정 파일
```

## 시험 직전 암기

```text
XProtocol = 통신 규칙
Xlib = 기존 라이브러리
XCB = Xlib 대체
Xtoolkit = GUI
Widget = GUI 객체
```

```text
XFree86
→ X Server

XF86Config
→ XFree86 설정 파일
```

```text
Xconfigurator
→ 텍스트 터미널 설정

XF86Setup
→ X-윈도우 환경 설정
```
