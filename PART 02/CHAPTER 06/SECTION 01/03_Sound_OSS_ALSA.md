# Sound Device - OSS & ALSA

## 1. OSS

`OSS`는 **Open Sound System**의 약자이다.

리눅스 및 유닉스 계열 운영체제에서 **사운드를 만들고 캡처하는 인터페이스**이다.

주요 특징:

- 표준 유닉스 장치 시스템 콜인 `READ`, `WRITE`, `IOCTL` 등에 기반
- 현재 리눅스 커뮤니티에서는 ALSA로 대체됨

```text
OSS
→ Open Sound System
→ 사운드 생성 / 캡처 인터페이스
→ 현재 ALSA로 대체
```

---

## 2. ALSA

`ALSA`는 **Advanced Linux Sound Architecture**의 약자이다.

사운드 카드용 장치 드라이버를 제공하기 위한 **리눅스 커널 요소**이다.

주요 특징:

- 1998년 Jaroslav Kysela에 의해 시작
- GPL 및 LGPL 라이선스 기반
- 사운드 카드를 자동으로 구성
- 시스템의 여러 사운드 장치를 관리

```text
ALSA
→ Advanced Linux Sound Architecture
→ 사운드 카드용 장치 드라이버 제공
→ 여러 사운드 장치 관리
```

---

## 3. ALSA 주요 지원 기능

책에 나온 기능:

```text
하드웨어 기반 MIDI 합성
다중 채널 하드웨어 믹싱
전이중 통신
다중 프로세서와의 조화
스레드 안정 장치 드라이버
```

---

## 4. ALSA 환경 설정 파일

```text
/etc/asound.state
```

```text
ALSA 설정 파일
→ /etc/asound.state
```

---

## 5. OSS와 ALSA 비교

| 구분 | OSS | ALSA |
|---|---|---|
| 풀네임 | Open Sound System | Advanced Linux Sound Architecture |
| 역할 | 사운드 생성/캡처 인터페이스 | 사운드 카드 장치 드라이버 제공 |
| 상태 | ALSA로 대체됨 | 현재 리눅스에서 사용 |
| 설정 파일 | 책에 별도 제시 없음 | `/etc/asound.state` |

---

# 핵심 정리

```text
OSS
→ Open Sound System
→ 사운드 생성 / 캡처
→ ALSA로 대체
```

```text
ALSA
→ Advanced Linux Sound Architecture
→ 사운드 카드 장치 드라이버 제공
→ 여러 사운드 장치 관리
→ /etc/asound.state
```

## 시험 직전 암기

```text
OSS → 예전
ALSA → 현재
```

```text
ALSA 설정 파일
→ /etc/asound.state
```
