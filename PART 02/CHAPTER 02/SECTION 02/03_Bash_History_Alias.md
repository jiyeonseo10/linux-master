# Bash History & Alias

## 1. History 기능

Bash의 History 기능은 이전에 사용했던 명령어를 저장해 두었다가 다시 사용할 수 있게 하는 기능이다.

주요 특징:

- 이전에 입력한 명령어를 저장
- 위/아래 방향키로 과거 명령어 재사용 가능
- 길거나 복잡한 명령어를 다시 입력하지 않아도 됨
- History 파일은 사용자 홈 디렉토리의 `~/.bash_history`

```text
History
→ 이전 명령어 저장 및 재사용
→ ~/.bash_history
```

---

## 2. History 관련 명령어 표현

| 표현 | 의미 |
|---|---|
| `!!` | 마지막으로 실행했던 명령어 실행 |
| `!n` | n번째 명령어 실행 |
| `!-n` | 현재 명령행에서 n개 이전 명령어 실행 |
| `!string` | 가장 최근에 `string`으로 시작하는 명령어 실행 |
| `!$` 또는 `!!$` | 마지막 명령어의 마지막 argument |
| `!*` | 마지막 명령어에 사용된 모든 argument |
| `!?string?` | 가장 최근에 `string`을 포함하는 명령어 실행 |

### 핵심

```text
!!      → 직전 명령어
!n      → n번째 명령어
!-n     → n개 이전 명령어
!string → string으로 시작하는 최근 명령어
!$      → 직전 명령어 마지막 인자
!*      → 직전 명령어 모든 인자
```

---

## 3. History 관련 환경 변수

| 변수 | 의미 |
|---|---|
| `HISTSIZE` | 히스토리 스택에 저장할 명령어 개수 |
| `HISTFILE` | 히스토리 파일 위치 |
| `HISTFILESIZE` | 물리적인 히스토리 파일 크기 |
| `HISTTIMEFORMAT` | 히스토리 명령어 수행 시간 출력 형식 |
| `HISTCONTROL` | 중복 명령어 기록 여부 설정 |

### 예시

현재 History 크기 확인:

```bash
echo $HISTSIZE
```

History 크기 변경:

```bash
export HISTSIZE=500
```

History에 실행 시간 표시:

```bash
export HISTTIMEFORMAT="%Y. %m. %d %T"
```

---

# 4. Alias 기능

`alias`는 자주 사용하는 명령어를 짧은 별명으로 등록하여 사용하는 기능이다.

### 현재 설정된 alias 확인

```bash
alias
```

### 새로운 alias 설정

```bash
alias 별명='명령어'
```

예:

```bash
alias ld='ls -l | grep "^d"'
```

### alias 해제

```bash
unalias 별명
```

예:

```bash
unalias ld
```

---

## 5. Alias 유지

명령 프롬프트에서 직접 설정한 alias는 **현재 셸에서만 유지**된다.

영구적으로 사용하려면 셸 설정 파일에 저장해야 한다.

```text
~/.bashrc
```

---

# 핵심 정리

```text
History
→ 과거 명령어 저장 및 재사용
→ ~/.bash_history
```

```text
!!      → 직전 명령어
!n      → n번째
!-n     → n개 이전
!$      → 직전 명령어 마지막 인자
!*      → 직전 명령어 모든 인자
```

```text
HISTSIZE       → 저장 명령어 개수
HISTFILE       → History 파일 위치
HISTFILESIZE   → History 파일 크기
HISTTIMEFORMAT → 실행 시간 출력 형식
HISTCONTROL    → 중복 명령어 기록 여부
```

```text
alias
→ 별명 확인

alias 별명='명령어'
→ 별명 생성

unalias 별명
→ 별명 해제
```
