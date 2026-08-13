# Process Basics

## 1. 프로세스

프로세스(Process)는 **CPU와 메모리를 할당받아 실행되는 프로그램**이다.

```text
프로그램
→ CPU와 메모리를 할당받아 실행
→ Process
```

운영체제에서 디스패치 가능한 기본 단위이다.

---

## 2. PID

각 프로세스는 고유한 **PID(Process ID)**를 가진다.

```text
PID
→ 프로세스를 구분하는 고유 번호
```

---

## 3. init과 systemd

### init

- 가장 먼저 실행되는 프로세스
- PID는 `1`
- 다른 프로세스를 생성하는 부모 프로세스 역할

```text
init
→ PID 1
→ 최상위 부모 프로세스
```

### systemd

최근 리눅스에서는 `systemd`가 최상위 프로세스로서 기존 `init`의 역할을 대체한다.

```text
systemd
→ 최근 리눅스에서 init 역할 대체
```

---

## 4. Foreground Process

사용자와 **직접 상호작용하는 프로세스**이다.

주요 특징:

- 터미널에 직접 연결
- 사용자와 입출력을 주고받음
- 작업이 끝날 때까지 기다림
- 화면에서 실행 상태 확인 가능

```text
Foreground
→ 사용자와 직접 상호작용
→ 실행 종료까지 기다림
```

---

## 5. Background Process

사용자와 직접 대화하지 않고 **뒤에서 실행되는 프로세스**이다.

주요 특징:

- 사용자 입력과 관계없이 실행 가능
- 실행 중에도 다른 작업 가능
- 시스템 프로그램이나 데몬 등이 해당

```text
Background
→ 뒤에서 독립적으로 실행
→ 실행 중에도 다른 작업 가능
```

---

# 핵심 정리

```text
Process
→ CPU와 메모리를 할당받아 실행되는 프로그램

PID
→ 프로세스 고유 번호

init
→ PID 1

systemd
→ 최근 리눅스에서 init 역할 대체

Foreground
→ 사용자와 직접 상호작용

Background
→ 뒤에서 독립적으로 실행
```
