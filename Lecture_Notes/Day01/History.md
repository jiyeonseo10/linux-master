# History

## Overview

The `history` command displays the command history stored by the shell.

It allows users to review, reuse, and execute previously entered commands.

---

## 1. Display Command History

```bash
history
```

**Description**

현재 사용자의 명령어 실행 기록을 출력한다.

---

## 2. Repeat the Previous Command

```bash
!!
```

**Description**

바로 이전에 실행한 명령어를 다시 실행한다.

**Example**

```bash
history
!!
```

위 예제에서 `!!`를 입력하면 `history`가 다시 실행된다.

---

## 3. Execute a Previous Command

```bash
!-3
```

**Description**

현재 명령을 기준으로 세 번째 이전에 실행한 명령을 다시 실행한다.

**Notes**

- `!!`: 바로 이전 명령 실행
- `!-n`: n번째 이전 명령 실행

---

## 4. Incorrect Usage Example

```bash
history -3
```

**Description**

잘못된 사용 예시이다.

**Output**

```text
-bash: history: -3: invalid option
```

**Notes**

- 최근 3개의 명령을 보고 싶다면 `history 3`처럼 숫자를 옵션 없이 사용한다.

---

## Notes

- `history`는 사용자가 실행한 명령을 저장한다.
- 저장된 명령은 빠르게 다시 실행할 수 있다.
- Bash에서는 `~/.bash_history` 파일에 명령 기록이 저장된다.
