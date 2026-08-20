# System V Printer Commands

## 1. System V 계열 프린터 명령어

책에 나온 System V 계열 프린터 명령어는 다음과 같다.

```text
lp
lpstat
cancel
```

```text
lp      → 프린터 작업 요청
lpstat  → 프린터 큐 상태 확인
cancel  → 프린트 작업 취소
```

---

## 2. lp

`lp`는 **프린터 작업을 요청**하는 명령어이다.

책에서는 BSD 계열의 `lpr`과 유사한 기능이라고 설명한다.

형식:

```bash
lp [옵션] [파일명]
```

### 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-n 값` | 인쇄할 매수 지정(1~100) |
| `-d 프린터명` | 기본 설정 프린터 이외의 다른 프린터 지정 |

### 연상

```text
-n
→ number
→ 인쇄 매수

-d
→ 다른 프린터 지정
```

---

## 3. lpstat

`lpstat`는 **프린터 큐의 상태를 확인**하는 명령어이다.

형식:

```bash
lpstat [옵션]
```

### 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-p` | 프린터의 인쇄 가능 여부 출력 |
| `-t` | 프린터의 상태 정보 출력 |
| `-a` | 프린터가 허가(accept)된 상황 정보 출력 |

### 핵심

```text
-p
→ 인쇄 가능 여부

-t
→ 상태 정보

-a
→ accept 상태
```

---

## 4. cancel

`cancel`은 **프린트 작업을 취소**하는 명령어이다.

취소할 요청 ID를 먼저 `lpstat`로 확인한 후 삭제한다.

형식:

```bash
cancel 요청ID
```

### 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-a` | 프린터 큐에 있는 모든 작업 취소 |

### 사용 흐름

```text
lpstat
→ 요청 ID 확인

cancel 요청ID
→ 해당 인쇄 작업 취소
```

---

## 5. BSD 계열과 System V 계열 비교

```text
BSD 계열

lpr   → 인쇄 요청
lpq   → 큐 조회
lprm  → 작업 삭제
lpc   → 프린터 / 큐 제어
```

```text
System V 계열

lp      → 인쇄 요청
lpstat  → 상태 확인
cancel  → 작업 취소
```

---

# 핵심 정리

```text
lp
→ 프린터 작업 요청

lpstat
→ 프린터 큐 상태 확인

cancel
→ 프린트 작업 취소
```

```text
lp -n
→ 인쇄 매수 지정

lp -d
→ 다른 프린터 지정
```

```text
lpstat -p
→ 인쇄 가능 여부

lpstat -t
→ 상태 정보

lpstat -a
→ accept 상태
```

```text
cancel -a
→ 프린터 큐의 모든 작업 취소
```

## 시험 직전 암기

```text
BSD
→ lpr / lpq / lprm / lpc

System V
→ lp / lpstat / cancel
```

```text
lp = print
lpstat = status
cancel = 취소
```
