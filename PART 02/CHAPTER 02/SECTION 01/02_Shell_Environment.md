# Shell Environment

## 1. Login Shell과 Sub Shell

### Login Shell

사용자가 로그인할 때 자동으로 실행되는 셸이다.

주요 특징:

- 시스템과의 기본 인터페이스 역할
- 사용자 환경 설정 파일을 읽어 초기 환경 구성
- 시스템 부팅 후 가장 먼저 실행되는 셸

대표적인 환경 설정 파일:

```text
.bash_profile
.bash_login
```

```text
Login Shell
→ 로그인 시 자동 실행
→ 사용자 환경 초기화
```

---

### Sub Shell

로그인 셸 내부에서 사용자가 작업을 실행하거나 다른 셸로 전환할 때 생성되는 임시 셸이다.

주요 특징:

- 로그인 셸로부터 파생
- 스크립트 실행이나 환경 테스트 등에 사용
- 종료하면 상위 셸의 환경으로 복귀

```text
Login Shell
    ↓
Sub Shell
    ↓
작업 수행
    ↓
종료
    ↓
상위 셸로 복귀
```

---

## 2. 사용 가능한 셸 확인

### `/etc/shells`

시스템에서 사용할 수 있는 셸의 목록을 확인할 수 있다.

```bash
cat /etc/shells
```

예:

```text
/bin/sh
/bin/bash
/bin/tcsh
/bin/csh
```

```text
/etc/shells
→ 사용 가능한 셸 목록
```

---

## 3. 계정별 로그인 셸 확인

### `/etc/passwd`

각 계정에 할당된 로그인 셸을 확인할 수 있다.

예:

```text
youngjin:x:1001:1001::/home/youngjin:/bin/bash
```

마지막 필드의 `/bin/bash`가 해당 사용자의 로그인 셸이다.

```text
/etc/passwd
→ 계정별 로그인 셸 확인
```

---

## 4. 현재 사용자의 셸 확인

```bash
echo $SHELL
```

예:

```text
/bin/bash
```

```text
echo $SHELL
→ 현재 로그인한 사용자가 사용하는 셸 확인
```

---

## 5. chsh

`chsh`는 일반 사용자가 로그인 셸을 변경할 때 사용하는 명령어이다.

### 기본 형식

```bash
chsh [옵션] 계정명
```

### 주요 옵션

| 옵션 | 의미 |
|---|---|
| `-s` | 지정한 셸을 로그인 셸로 변경 |
| `-l` | `/etc/shells`에 등록된 셸 목록 출력 |

예:

```bash
chsh -s /bin/csh
```

로그인 셸을 `/bin/csh`로 변경한다.

```bash
chsh -l
```

사용 가능한 셸 목록을 확인한다.

---

## 6. usermod

관리자가 특정 사용자의 계정 정보를 변경할 때 사용하는 명령어이다.

셸 변경 시 `-s` 옵션을 사용한다.

```bash
usermod -s /bin/csh youngjin
```

`youngjin` 사용자의 로그인 셸을 `/bin/csh`로 변경한다.

```text
chsh
→ 일반 사용자가 자신의 로그인 셸 변경

usermod -s
→ 관리자가 사용자의 로그인 셸 변경
```

---

# 핵심 정리

```text
Login Shell
→ 로그인 시 자동 실행
→ 사용자 환경 초기화

Sub Shell
→ 로그인 셸에서 파생된 임시 셸
→ 종료하면 상위 셸로 복귀
```

셸 확인:

```text
/etc/shells
→ 사용 가능한 셸 목록

/etc/passwd
→ 계정별 로그인 셸

echo $SHELL
→ 현재 사용자의 셸
```

셸 변경:

```text
chsh -s
→ 로그인 셸 변경

chsh -l
→ /etc/shells 목록 출력

usermod -s
→ 관리자가 사용자 셸 변경
```
