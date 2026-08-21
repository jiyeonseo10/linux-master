# Display Managers

## 1. 디스플레이 매니저의 개념

디스플레이 매니저(Display Manager)는  
**X Window System 상에서 동작하는 프로그램**이다.

주요 역할:

```text
로컬 또는 리모트 컴퓨터의 X Server 접속
그래픽 로그인 화면 제공
사용자 ID / Password 인증
세션 시작
```

### 핵심

```text
Display Manager
→ 그래픽 로그인
→ 사용자 인증
→ X 세션 시작
```

---

## 2. 디스플레이 매니저의 역사

책 기준:

```text
1988년 X11R3
→ xdm 도입

1989년 X11R4
→ xdmcp 도입
```

`xdmcp`는 다음의 약자이다.

```text
X Display Manager Control Protocol
```

원격에서 제어할 수 있도록 도입되었다.

---

## 3. xdm

`xdm`은 **X Display Manager**이다.

주요 특징:

- 초기 X11에 도입된 디스플레이 매니저
- 그래픽 로그인 화면 제공
- 세션 관리
- 현재는 거의 사용되지 않음

### 핵심

```text
xdm
→ 초기 X Display Manager
→ 그래픽 로그인
→ 세션 관리
```

---

## 4. dtlogin

`dtlogin`은 **CDE 환경에서 사용하는 디스플레이 매니저**이다.

주요 특징:

- 유닉스 계열 데스크톱 환경인 CDE에서 사용
- AIX, HP-UX, Unixware, 구 Solaris에서 사용
- Motif 라이브러리를 사용하여 구현
- Red Hat Linux에도 있었으나 GNOME과 KDE에 밀림
- Solaris도 이후 GNOME으로 이동하면서 CDE 사용 감소

### 핵심

```text
dtlogin
→ CDE
→ Motif
```

---

## 5. kdm

`kdm`은 **KDE Display Manager**이다.

KDE 데스크톱에서 사용되는 디스플레이 매니저이다.

```text
kdm
→ KDE
```

---

## 6. gdm

`gdm`은 **GNOME의 디스플레이 매니저**이다.

주요 특징:

- 그래픽 로그인 프로그램
- GTK 라이브러리 사용
- xdm 기반이 아니라 독립적으로 새로 작성
- GNU GPL 기반 라이선스

### 핵심

```text
gdm
→ GNOME
→ GTK
→ 그래픽 로그인 프로그램
```

---

# 디스플레이 매니저 비교

| 디스플레이 매니저 | 특징 |
|---|---|
| `xdm` | 초기 X Display Manager |
| `dtlogin` | CDE / Motif |
| `kdm` | KDE |
| `gdm` | GNOME / GTK |

---

# 핵심 정리

```text
Display Manager
→ 그래픽 로그인
→ 사용자 인증
→ 세션 시작
```

```text
xdm
→ 초기 X Display Manager

dtlogin
→ CDE
→ Motif

kdm
→ KDE

gdm
→ GNOME
→ GTK
```

```text
X11R3
→ xdm

X11R4
→ xdmcp
```

## 시험 직전 암기

```text
xdm = 초기

dtlogin = CDE + Motif

kdm = KDE

gdm = GNOME + GTK
```
