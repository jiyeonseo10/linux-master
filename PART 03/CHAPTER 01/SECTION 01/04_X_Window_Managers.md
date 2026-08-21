# X Window Managers

## 1. 윈도우 매니저

윈도우 매니저는 **X-Window에서 창(Window)의 배치와 표현을 담당하는 시스템 프로그램**이다.

주요 기능:

```text
창 열기 / 닫기
창 생성 위치 결정
창 크기 조정
창 외양과 테두리 변경
```

사용 라이브러리:

```text
Xlib
XCB
```

---

## 2. fvwm

`fvwm`은 `twm`에서 파생된 윈도우 매니저이다.

주요 특징:

- 안정적이고 일반화되어 오랜 기간 많이 사용
- Virtual Window Manager의 약자
- 가상 데스크톱 지원

```text
fvwm
→ twm에서 파생
→ Virtual Window Manager
→ 가상 데스크톱 지원
```

---

## 3. twm

`twm`은 X-Window 시스템의 초창기 창 관리자이다.

주요 특징:

- X-Window 개발에 큰 영향을 줌
- C로 만들어짐
- 간단한 텍스트 형식의 윈도우 매니저
- GTK+, Qt 같은 별도 툴킷을 사용하지 않음
- Xlib 사용

```text
twm
→ 초창기 윈도우 매니저
→ C
→ Xlib 사용
```

---

## 4. AfterStep

`AfterStep`은 `fvwm`을 기반으로 만들어진 윈도우 매니저이다.

주요 특징:

- NeXTSTEP의 GUI와 유사한 사용자 인터페이스 제공
- 여러 사용자의 요구사항을 반영하며 기능적으로 발전

```text
AfterStep
→ fvwm 기반
→ NeXTSTEP GUI와 유사
```

---

## 5. Window Maker

`Window Maker`는 OpenStep 호환 환경으로 NeXTSTEP의 GUI를 구현한 윈도우 매니저이다.

주요 특징:

- 그래픽 응용 프로그램을 유닉스 계열 운영체제에서 실행 가능
- GNU 데스크톱 지원
- 책에서는 현재 GNOME과 KDE에 통합된 것으로 설명

```text
Window Maker
→ OpenStep 호환
→ NeXTSTEP GUI 구현
→ GNU 데스크톱 지원
```

---

## 6. Blackbox

```text
Blackbox
→ NeXTSTEP 인터페이스를 기반으로 하는 윈도우 매니저
```

---

## 7. kwm

```text
kwm
→ KDE 1.x의 기본 윈도우 매니저
```

---

## 8. Enlightenment

```text
Enlightenment
→ GNOME의 기본 윈도우 매니저
```

---

# 핵심 정리

```text
윈도우 매니저
→ 창의 배치와 표현 담당
→ Xlib / XCB 사용
```

```text
fvwm
→ twm에서 파생
→ 가상 데스크톱

twm
→ 초창기
→ C
→ Xlib
```

```text
AfterStep
→ fvwm 기반
→ NeXTSTEP

Window Maker
→ OpenStep
→ NeXTSTEP GUI

Blackbox
→ NeXTSTEP 인터페이스
```

```text
kwm
→ KDE 1.x

Enlightenment
→ GNOME
```

## 시험 직전 암기

```text
fvwm ← twm에서 파생

AfterStep ← fvwm 기반

kwm = KDE
Enlightenment = GNOME
```
