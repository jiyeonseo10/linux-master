# Process Signals

## 1. Signal

시그널(Signal)은 **프로세스에게 이벤트 발생을 전달하는 소프트웨어 인터럽트**이다.

```text
Signal
→ 프로세스에게 이벤트 발생 전달
→ 소프트웨어 인터럽트
```

---

## 2. Signal 처리 방식

| 처리 방식 | 의미 |
|---|---|
| `SIG_IGN` | 시그널 무시 |
| `SIG_ERR` | 프로그램 강제 종료 |
| `SIG_DFL` | 기본 시그널 처리 루틴 실행 |
| `SIG_HOLD` | 시그널 블로킹 |

### 핵심

```text
SIG_IGN  → 무시
SIG_ERR  → 강제 종료
SIG_DFL  → 기본 처리
SIG_HOLD → 블로킹
```

---

## 3. Signal 목록 확인

```bash
kill -l
```

시스템에서 사용할 수 있는 시그널 목록을 확인한다.

---

## 4. 주요 Signal

| 번호 | 시그널 | 의미 |
|---|---|---|
| 1 | `SIGHUP` | 터미널 연결이 끊어졌을 때 |
| 2 | `SIGINT` | `Ctrl + C` 입력 |
| 3 | `SIGQUIT` | `Ctrl + \` 입력 |
| 6 | `SIGABRT` | `abort()` 함수에 의해 발생 |
| 9 | `SIGKILL` | 프로세스 강제 종료 |
| 13 | `SIGPIPE` | 종료된 소켓에 쓰기 시도 |
| 14 | `SIGALRM` | 알람 타이머 만료 |
| 15 | `SIGTERM` | 프로세스 종료 |
| 17 | `SIGCHLD` | 자식 프로세스 종료 |
| 18 | `SIGCONT` | 중지된 프로세스 실행 |
| 19 | `SIGSTOP` | 프로세스 중지 |
| 20 | `SIGTSTP` | `Ctrl + Z` 입력 |

---

## 5. 자주 나오는 Signal

```text
1  SIGHUP   → 터미널 연결 끊김
2  SIGINT   → Ctrl + C
3  SIGQUIT  → Ctrl + \
9  SIGKILL  → 강제 종료
15 SIGTERM  → 종료
20 SIGTSTP  → Ctrl + Z
```

---

## 6. Ctrl 키와 Signal

```text
Ctrl + C
→ SIGINT
→ 프로세스 종료

Ctrl + Z
→ SIGTSTP
→ 프로세스 대기/중지

Ctrl + \
→ SIGQUIT
→ Core Dump
```

---

## 7. Core Dump

프로그램이 비정상적으로 종료될 때 **당시의 메모리 상태를 저장하여 오류 원인을 분석할 수 있도록 하는 것**이다.

```text
Core Dump
→ 비정상 종료
→ 당시 메모리 상태 저장
→ 오류 원인 분석
```

---

# 핵심 정리

```text
Signal
→ 프로세스에게 이벤트 발생을 전달하는 소프트웨어 인터럽트

SIGINT  → 2  → Ctrl + C
SIGQUIT → 3  → Ctrl + \
SIGKILL → 9  → 강제 종료
SIGTERM → 15 → 종료
SIGTSTP → 20 → Ctrl + Z
```

```text
Ctrl + C = 종료
Ctrl + Z = 중지
```
