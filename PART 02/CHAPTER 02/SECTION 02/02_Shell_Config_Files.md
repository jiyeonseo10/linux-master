# Shell Configuration Files

## 1. 셸 시작 파일

셸이 시작될 때 자동으로 실행되는 설정 파일을 통해 사용자의 셸 환경을 설정한다.

Bash 셸의 주요 시작 파일:

```text
/etc/profile
/etc/bashrc
~/.bash_profile
~/.bashrc
```

셸 설정 파일은 크게 **전역 설정 파일**과 **지역 설정 파일**로 구분한다.

---

## 2. 전역 설정 파일

모든 사용자에게 공통으로 영향을 주며 `/etc` 아래에 위치한다.

### `/etc/profile`

모든 사용자의 셸 환경을 제어하는 전역 설정 파일이다.

주요 기능:

- 모든 사용자의 셸 환경 제어
- 환경 변수 설정
- bash 실행 시 필요한 프로그램 제어
- 관리자만 설정 가능
- 모든 사용자에게 적용

```text
/etc/profile
→ 모든 사용자
→ 환경 변수 등 전역 환경 설정
```

---

### `/etc/bashrc`

별칭(alias)과 bash가 실행할 때 사용하는 함수 등을 전역적으로 설정한다.

```text
/etc/bashrc
→ 전역 alias 및 함수 설정
```

---

## 3. 지역 설정 파일

개별 사용자를 위한 설정 파일이다.

사용자의 **홈 디렉토리**에 숨김 파일 형태로 존재한다.

### `~/.bash_profile`

개인 사용자의 셸 환경을 설정한다.

주요 기능:

- PATH 설정
- 환경 변수 설정 및 변경
- 로그인 시 로딩

```text
~/.bash_profile
→ 개인 환경 설정
→ PATH / 환경 변수
→ 로그인 시 로딩
```

---

### `~/.bash_history`

사용자가 입력했던 명령어를 기록한다.

주요 기능:

- 이전에 사용한 명령어 저장
- 이전 명령어 검색
- 명령어 재사용

```text
~/.bash_history
→ 명령어 기록
```

---

### `~/.bashrc`

개인 사용자의 별칭(alias)과 bash 함수 등을 설정한다.

```text
~/.bashrc
→ 개인 alias 및 함수 설정
```

---

### `~/.bash_logout`

사용자가 **로그아웃하기 직전에 실행**되는 설정 파일이다.

```text
~/.bash_logout
→ 로그아웃 직전 실행
```

---

## 4. `/etc/profile.d`

추가적인 시작 스크립트를 저장하는 디렉토리이다.

- 응용 프로그램 시작 시 자동 실행할 스크립트 저장
- 지정된 경로의 스크립트가 자동 실행
- 일반 사용자의 alias 설정과 관련된 스크립트도 존재할 수 있음

```text
/etc/profile.d
→ 추가 시작 스크립트
→ 스크립트 자동 실행
```

---

# 전역 설정과 지역 설정 비교

```text
전역 설정
├── /etc/profile
└── /etc/bashrc

→ 모든 사용자에게 적용
```

```text
지역 설정
├── ~/.bash_profile
├── ~/.bash_history
├── ~/.bashrc
└── ~/.bash_logout

→ 개별 사용자에게 적용
```

---

# 핵심 정리

```text
/etc/profile
→ 모든 사용자 환경 설정

/etc/bashrc
→ 전역 alias / 함수

~/.bash_profile
→ 개인 환경 설정
→ PATH / 환경 변수
→ 로그인 시 로딩

~/.bashrc
→ 개인 alias / 함수

~/.bash_history
→ 사용했던 명령어 기록

~/.bash_logout
→ 로그아웃 직전 실행

/etc/profile.d
→ 추가 시작 스크립트
```
