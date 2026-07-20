# Shell Environment

## Overview

The shell is a command-line interpreter that receives commands from the user and executes them.

Common shells include:

- Bash
- Zsh
- Sh
- Csh

---

## 1. Print Text

```bash
echo 1111
```

**Description**

화면에 문자열을 출력한다.

**Notes**

- `echo`는 문자열이나 변수 값을 출력할 때 사용한다.

---

## 2. Display Current Shell

```bash
echo $SHELL
```

**Description**

현재 사용 중인 로그인 셸을 확인한다.

**Example Output**

```text
/bin/bash
```

---

## 3. List Available Shells

```bash
chsh -l
```

**Description**

시스템에서 사용할 수 있는 셸 목록을 출력한다.

**Example Output**

```text
/bin/sh
/bin/bash
/bin/zsh
...
```

**Notes**

- `chsh`: Change Shell
- `-l`: 사용 가능한 셸 목록 출력

---

## 4. Display Environment Variables

```bash
env
```

**Description**

현재 환경 변수를 출력한다.

**Common Variables**

| Variable | Description |
|----------|-------------|
| HOME | 사용자 홈 디렉토리 |
| PATH | 명령어 검색 경로 |
| SHELL | 현재 로그인 셸 |
| USER | 현재 사용자 |
| PWD | 현재 작업 디렉토리 |
| LANG | 시스템 언어 |

---

## 5. Display Available Locales

```bash
locale -a
```

**Description**

시스템에 설치된 Locale 목록을 출력한다.

**Notes**

- Locale은 언어 및 지역 설정을 의미한다.
- 날짜, 시간, 숫자, 문자 인코딩 등에 영향을 준다.
