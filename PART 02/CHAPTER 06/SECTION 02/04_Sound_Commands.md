# Sound Commands

## 1. alsactl

`alsactl`은 **ALSA 사운드 카드를 제어하는 명령어**이다.

형식:

```bash
alsactl [옵션] [명령]
```

### 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-d` | 디버그 모드 사용 |
| `-f` | 환경 설정 파일 선택 |

### 주요 명령

| 명령 | 기능 |
|---|---|
| `store` | 사운드 카드 정보를 환경 설정 파일에 저장 |
| `restore` | 환경 설정 파일에서 선택된 사운드 카드 정보를 다시 읽어들임 |
| `init` | 사운드 장치 초기화 |

### 연상 암기

```text
store
→ 저장

restore
→ 복원

init
→ 초기화
```

---

## 2. alsamixer

`alsamixer`는 **커서(ncurses) 라이브러리 기반의 오디오 프로그램**이다.

```text
alsamixer
→ ncurses 기반 오디오 프로그램
```

---

## 3. cdparanoia

`cdparanoia`는 **오디오 CD로부터 음악 파일을 추출할 때 사용하는 명령어**이다.

형식:

```bash
cdparanoia [옵션]
```

### 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-w` | wav 파일 추출 |
| `-a` | Apple AIFF-C 포맷으로 추출 |
| `-B` | 모든 트랙을 cdda2wav 스타일로 추출 |

### 연상 암기

```text
-w
→ wav

-a
→ Apple AIFF-C

-B
→ 모든 트랙
```

---

# 핵심 정리

```text
alsactl
→ ALSA 사운드 카드 제어

-d → 디버그 모드
-f → 환경 설정 파일 선택

store → 저장
restore → 복원
init → 초기화
```

```text
alsamixer
→ ncurses 기반 오디오 프로그램
```

```text
cdparanoia
→ 오디오 CD 음악 파일 추출

-w → wav
-a → Apple AIFF-C
-B → 모든 트랙을 cdda2wav 스타일로 추출
```
