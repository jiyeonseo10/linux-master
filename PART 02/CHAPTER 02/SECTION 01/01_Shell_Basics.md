# Shell Basics

## 1. Shell의 개념

셸(Shell)은 **명령어 해석기(Command Interpreter)**이다.

사용자가 입력한 명령어를 해석하여 **커널(Kernel)에 전달**한다.

```text
응용 프로그램
    ↓
Shell
    ↓
Kernel
    ↓
Hardware
```

### 주요 기능

- 사용자가 입력한 명령어를 해석하여 커널에 전달
- 사용자와 커널 사이의 대화식 인터페이스 제공
- 로그인 시 실행되어 사용자별 환경 설정 가능
- 스크립트 언어 기능 제공
- Redirection과 Pipe 기능 제공
- Foreground / Background 프로세스 실행

```text
Shell = 사용자와 Kernel 사이의 명령어 해석기
```

---

## 2. Shell의 계열

셸은 크게 다음 두 계열로 나뉜다.

```text
Bourne Shell 계열
C Shell 계열
```

사용자 프롬프트:

```text
$ → Bourne Shell 계열
% → C Shell 계열
```

---

# 3. Bourne Shell 계열

## Bourne Shell

실행 파일:

```bash
/bin/sh
```

특징:

- Bell 연구소의 Stephen Bourne이 1979년에 개발
- UNIX에서 기본 셸로 사용

```text
Bourne Shell → /bin/sh
```

---

## Korn Shell

실행 파일:

```bash
/bin/ksh
```

특징:

- AT&T의 David Korn이 1986년에 개발
- Bourne Shell을 확장
- 명령어 완성 기능
- 히스토리 기능

```text
Korn Shell → /bin/ksh
```

---

## Bash Shell

실행 파일:

```bash
/bin/bash
```

특징:

- Brian Fox가 1989년에 개발
- Bourne Shell을 기반으로 개발
- GNU 프로젝트
- Linux 표준 셸
- 명령어 완성 기능
- 히스토리 기능
- 명령어 치환
- 편집 기능
- POSIX와 호환

```text
Bash → /bin/bash
→ GNU
→ Linux 표준 셸
```

---

## Z Shell

실행 파일:

```bash
/bin/zsh
```

특징:

- Paul Falstad가 1990년에 개발
- 확장형 Bourne Shell
- Korn Shell의 재작성 셸
- 강력한 history 기능
- 향상된 명령행 편집 기능
- 자동 완성 기능

```text
Z Shell → /bin/zsh
```

---

# 4. C Shell 계열

## C Shell

실행 파일:

```bash
/bin/csh
```

특징:

- Berkeley 대학의 Bill Joy가 1981년에 개발
- C 언어의 특징을 많이 포함
- history 기능
- alias 기능
- 작업 제어 기능
- 프로그래밍 기능

```text
C Shell → /bin/csh
→ Bill Joy
```

---

## tcsh

실행 파일:

```bash
/bin/tcsh
```

특징:

- Ken Greer가 1982년에 개발
- 확장 C Shell
- BSD 계열에서 많이 사용
- 명령어 편집 기능
- emacs
- history explorer
- 자동 완성 기능
- 자동 로그아웃 기능

```text
tcsh → /bin/tcsh
→ 확장 C Shell
```

---

# 핵심 정리

## Bourne Shell 계열

```text
sh   → /bin/sh
ksh  → /bin/ksh
bash → /bin/bash
zsh  → /bin/zsh
```

## C Shell 계열

```text
csh  → /bin/csh
tcsh → /bin/tcsh
```

## 프롬프트

```text
$ → Bourne Shell 계열
% → C Shell 계열
```

## 개발자 연결

```text
Bourne Shell → Stephen Bourne
Korn Shell   → David Korn
Bash         → Brian Fox
Z Shell      → Paul Falstad
C Shell      → Bill Joy
tcsh         → Ken Greer
```

## 시험 포인트

```text
Shell
→ 명령어 해석기
→ 사용자와 커널 사이의 인터페이스
→ Redirection / Pipe 지원
→ Foreground / Background 프로세스 실행

Bash
→ GNU
→ Linux 표준 셸
```
