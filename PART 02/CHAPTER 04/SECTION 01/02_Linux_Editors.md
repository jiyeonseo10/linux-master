# Linux Editors

## 1. Pico

Pico는 **워싱턴 대학의 Aboil Kasar가 개발한 유닉스 기반 텍스트 에디터**이다.

주요 특징:

- 메뉴 선택 방식의 텍스트 편집기
- 윈도우 메모장과 비슷한 인터페이스
- 초기 리눅스 배포판에서 사용
- 자유 소프트웨어 라이선스가 아니어서 소스 수정 불가
- 사용하기 쉽지만 기능이 부족하고 업데이트가 잘 되지 않음
- GNU 프로젝트에서 Pico의 복제 버전인 `nano`를 개발
- `vi`, `emacs`와 달리 입력모드와 명령모드 구분 없이 바로 입력 가능

### 핵심

```text
Pico
→ 사용 쉬움
→ 메뉴 방식
→ 모드 구분 없음
→ GNU에서 nano 개발
```

---

## 2. Emacs

Emacs는 **Richard Stallman이 개발한 텍스트 편집기**이다.

주요 특징:

- 매크로 기능 제공
- 이후 James Gosling이 다양한 기능 추가
- LISP 기반 환경 설정 언어 사용
- C, LISP, FORTRAN, HTML 등의 모드 설정 가능
- 단순 편집기를 넘어 통합 환경 제공
- LISP 코드를 불러오는 데 시간이 오래 걸릴 수 있음
- 문서 편집부터 프로그래밍까지 다양하게 사용
- 비모드형 편집기
- `Ctrl`, `Alt`과 다른 키를 조합하여 명령 수행

### 핵심

```text
Emacs
→ Richard Stallman
→ LISP 기반
→ 비모드형 편집기
→ Ctrl / Alt 조합 사용
```

---

## 3. vi

`vi`는 **1976년 Bill Joy가 초기 BSD 릴리즈에 포함될 편집기로 만든 에디터**이다.

주요 특징:

- 리눅스 배포판과 유닉스에 기본적으로 포함
- 유닉스 환경에서 많이 사용하는 문서 편집기
- 모드형 편집기
- 명령모드, 입력모드, 편집모드로 구성
- 한 줄 단위가 아니라 한 화면을 편집하는 비주얼 에디터
- 다양한 vi clone 존재

### 핵심

```text
vi
→ Bill Joy
→ 모드형 편집기
→ 명령모드 / 입력모드 / 편집모드
→ Visual Editor
```

---

## 4. vim

`vim`은 **Bram Moolenaar가 만든 편집기**이다.

주요 특징:

- `vi`와 호환
- 다양한 기능을 추가한 편집기
- 다양한 색상 사용 가능
- 패턴 검색 시 하이라이트 제공
- ex모드에서 history 기능 제공
- 확장 정규 표현식 문법 지원
- 강력한 문법 강조 기능
- 다중 되돌리기 기능
- 유니코드를 포함한 다국어 지원
- 문법 검사 기능 지원

### 핵심

```text
vim
→ Bram Moolenaar
→ vi 호환
→ vi보다 다양한 기능 추가
→ 하이라이트 / 문법 강조 / 다중 되돌리기
```

---

## 5. gedit

`gedit`은 **GNOME 데스크톱 환경용 자유 소프트웨어 텍스트 편집기**이다.

주요 특징:

- Microsoft Windows, Mac OS X에서도 사용 가능
- UTF-8과 호환
- 프로그램 코드와 마크업 언어 등 구조화된 텍스트 편집에 중점
- X-Window 시스템에 맞춰 개발
- GTK+와 GNOME 라이브러리 사용
- Nautilus와 드래그 앤 드롭 가능
- 텔넷 접속이나 텍스트 기반 콘솔에서는 사용 불가

### 핵심

```text
gedit
→ GNOME 데스크톱용
→ GUI 편집기
→ UTF-8 지원
→ GTK+ 사용
→ 텍스트 콘솔에서는 사용 불가
```

---

# 핵심 비교

```text
Pico
→ 쉽고 간단
→ 모드 구분 없음
→ nano

Emacs
→ Richard Stallman
→ LISP
→ 비모드형

vi
→ Bill Joy
→ 모드형
→ 명령 / 입력 / 편집 모드

vim
→ Bram Moolenaar
→ vi 호환 및 기능 확장

gedit
→ GNOME GUI
→ GTK+
→ 콘솔 사용 불가
```
