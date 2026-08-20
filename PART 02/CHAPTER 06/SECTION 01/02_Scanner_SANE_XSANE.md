# Scanner Setup - SANE & XSANE

## 1. SANE

`SANE`은 **Scanner Access Now Easy**의 약자이다.

평판 스캐너, 핸드 스캐너, 비디오 캠 등 **이미지 관련 하드웨어를 제어하는 API**이다.

주요 특징:

- GPL 라이선스
- Linux 지원
- Unix 계열 지원
- OS2 지원
- Windows 지원

```text
SANE
→ Scanner Access Now Easy
→ 이미지 관련 하드웨어 제어 API
```

---

## 2. SANE 장치 파일

### SCSI 스캐너

```text
/dev/sg0
/dev/scanner
```

### USB 스캐너

```text
/dev/usb/scanner
/dev/usbscanner
```

### 핵심

```text
SCSI
→ /dev/sg0
→ /dev/scanner

USB
→ /dev/usb/scanner
→ /dev/usbscanner
```

---

## 3. XSANE

`XSANE`은 **X based interface for the SANE**의 약자이다.

SANE 스캐너 인터페이스를 이용하는 **X-Windows 기반 스캐너 프로그램**이다.

주요 특징:

- SANE 인터페이스 사용
- X-Windows 기반
- GTK+ 라이브러리로 개발
- 스캐너, 디지털 카메라, 디지털 캠 등에서 사용 가능
- 스캔뿐 아니라 캡처한 이미지 수정 가능
- GPL 라이선스
- Linux / Unix 계열 / OS2 / Windows 지원

실행:

```bash
xsane
```

---

## 4. SANE과 XSANE 비교

| 구분 | SANE | XSANE |
|---|---|---|
| 의미 | Scanner Access Now Easy | X based interface for the SANE |
| 역할 | 이미지 하드웨어 제어 API | X-Windows 기반 스캐너 프로그램 |
| 기반 | API | SANE |
| 라이브러리 | - | GTK+ |
| 실행 명령 | - | `xsane` |

---

# 핵심 정리

```text
SANE
→ Scanner Access Now Easy
→ 이미지 관련 하드웨어 제어 API
```

```text
XSANE
→ SANE 기반
→ X-Windows 기반 스캐너 프로그램
→ GTK+
→ xsane
```

```text
SCSI 스캐너
→ /dev/sg0
→ /dev/scanner

USB 스캐너
→ /dev/usb/scanner
→ /dev/usbscanner
```

## 시험 직전 암기

```text
SANE = API
XSANE = X-Windows 프로그램

SCSI = /dev/sg0
USB = /dev/usb/scanner
```
