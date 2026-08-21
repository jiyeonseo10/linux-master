# X Window Execution

## 1. X-윈도우 실행

그래픽 환경이 아닌 터미널 윈도우로 로그인한 경우  
X-윈도우를 실행하려면 `startx` 명령어를 사용한다.

형식:

```bash
startx -- [인자값]
```

---

## 2. startx

`startx`는 **X-윈도우를 실행하는 스크립트**이다.

주요 기능:

```text
시스템 환경 초기화
→ xinit 호출
→ X-윈도우 실행
```

### 인자 전달

`startx` 실행 시 `xinit`에 인자값을 전달하는 옵션은:

```text
--
```

예:

```bash
startx -- 인자값
```

---

## 3. X-윈도우 관련 키 조합

### 터미널 변경

```text
Ctrl + Alt + F1 ~ F4
```

각각:

```text
F1 → tty1
F2 → tty2
F3 → tty3
F4 → tty4
```

### X-윈도우 상태 전환

```text
Ctrl + Alt + F7
```

### X-윈도우 강제 종료

```text
Ctrl + Alt + Back Space
```

---

## 4. DISPLAY 환경 변수

`DISPLAY`는 **현재 X-윈도우 Display 위치를 지정하는 환경 변수**이다.

형식:

```bash
export DISPLAY=IP주소:디스플레이번호.스크린번호
```

구조:

```text
IP주소
:
디스플레이번호
.
스크린번호
```

### 핵심

```text
DISPLAY
→ X-윈도우 Display 위치 지정
```

---

# 핵심 정리

```text
startx
→ X-윈도우 실행 스크립트
→ 시스템 환경 초기화
→ xinit 호출
```

```text
startx -- 인자값
→ xinit에 인자값 전달
```

```text
Ctrl + Alt + F1~F4
→ 터미널 변경

Ctrl + Alt + F7
→ X-윈도우 상태 전환

Ctrl + Alt + Back Space
→ X-윈도우 강제 종료
```

```text
DISPLAY
→ 현재 X-윈도우 Display 위치 지정
```

```bash
export DISPLAY=IP주소:디스플레이번호.스크린번호
```

## 시험 직전 암기

```text
startx → X 실행
-- → xinit에 인자 전달

F1~F4 → 터미널
F7 → X-윈도우
Back Space → 강제 종료

DISPLAY → 화면 위치 지정
```
