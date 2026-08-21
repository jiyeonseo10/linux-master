# Desktop Environments

## 1. 데스크톱 환경의 개념

데스크톱 환경(Desktop Environment 또는 Desktop Manager)은  
GUI 사용자에게 제공되는 **인터페이스 스타일**이다.

다음과 같은 도구와 기능을 패키지 형태로 제공한다.

```text
윈도우 매니저
파일 관리자
도움말
제어판
아이콘
창
도구 모음
폴더
배경화면
데스크톱 위젯
```

또한 다음 기능을 지원한다.

```text
Drag & Drop
프로세스 간 통보 기능
```

---

## 2. KDE

`KDE`는 **Kool Desktop Environment**의 약자이다.

주요 특징:

- 독일을 중심으로 한 국제 개발팀이 개발
- 오픈 소스 데스크톱 환경
- 파일 매니저, 윈도우 매니저, 헬프 시스템, configuration 시스템 등의 집합체
- `QT` 툴킷 기반

### KDE 구성

```text
그래픽 라이브러리 → QT
기본 텍스트 에디터 → kate
기본 브라우저 → Konqueror
파일 탐색기 → Konqueror
윈도우 매니저 → Kwin
```

### 핵심

```text
KDE
→ QT
→ kate
→ Konqueror
→ Kwin
```

---

## 3. GNOME

`GNOME`은 **GNU Network Object Model Environment**의 약자이다.

주요 특징:

- GNU에서 만든 공개형 데스크톱
- 소스 공개 자유 소프트웨어
- `GTK+` 라이브러리 기반
- 전용 윈도우 관리자가 없고 윈도우 관리자를 선택하여 사용
- 세션 매니저가 이전 설정을 저장
- Drag & Drop 프로토콜 지원

### GNOME 구성

```text
그래픽 라이브러리 → GTK+
기본 텍스트 에디터 → gedit
기본 브라우저 → Web
파일 탐색기 → Nautilus
윈도우 매니저 → Mutter 또는 Metacity
```

### 핵심

```text
GNOME
→ GTK+
→ gedit
→ Nautilus
→ Mutter / Metacity
```

---

## 4. KDE와 GNOME 비교

| 구분 | KDE | GNOME |
|---|---|---|
| 그래픽 라이브러리 | QT | GTK+ |
| 기본 텍스트 에디터 | kate | gedit |
| 기본 브라우저 | Konqueror | Web |
| 파일 탐색기 | Konqueror | Nautilus |
| 윈도우 매니저 | Kwin | Mutter / Metacity |

### 암기

```text
KDE = QT = K 계열
→ kate / Konqueror / Kwin

GNOME = GTK+
→ gedit / Nautilus / Mutter
```

---

## 5. LXDE

`LXDE`는 **Light X11 Desktop Environment**의 약자이다.

주요 특징:

- 2006년부터 개발
- Ubuntu, Peppermint OS, Raspbian 등에서 기본 데스크톱으로 채택
- 가볍고 빠른 성능과 에너지 절약을 위해 개발
- CPU 성능이 낮고 메모리가 적은 PC와 모바일 장치에 적합

### 구성

```text
윈도우 매니저 → Openbox
툴킷 → GTK 2
파일 브라우저 → PCMANFM
```

### 핵심

```text
LXDE
→ Light
→ Openbox
→ GTK 2
→ PCMANFM
→ 가볍고 빠름
```

---

## 6. XFCE

`XFCE`는 **XForms Common Environment**의 약자이다.

주요 특징:

- 유닉스 및 유닉스 계열 플랫폼용 자유 소프트웨어 데스크톱 환경
- `GTK+ 2` 툴킷 기반
- KDE, GNOME보다 적은 시스템 자원 사용
- 모듈 간 의존성이 낮음
- 하드디스크 공간을 적게 사용

### 구성

```text
윈도우 매니저 → Xfwm
툴킷 → GTK+ 2
```

### 핵심

```text
XFCE
→ GTK+ 2
→ Xfwm
→ 적은 시스템 자원 사용
```

---

# 핵심 정리

```text
KDE
→ QT
→ kate
→ Konqueror
→ Kwin
```

```text
GNOME
→ GTK+
→ gedit
→ Nautilus
→ Mutter / Metacity
```

```text
LXDE
→ Openbox
→ GTK 2
→ PCMANFM
→ 가볍고 빠름
```

```text
XFCE
→ GTK+ 2
→ Xfwm
→ 적은 자원 사용
```

## 시험 직전 암기

```text
KDE = QT
GNOME = GTK+

KDE = kate / Konqueror / Kwin
GNOME = gedit / Nautilus / Mutter

LXDE = Openbox
XFCE = Xfwm
```
