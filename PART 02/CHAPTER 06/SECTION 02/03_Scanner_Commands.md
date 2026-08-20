# Scanner Commands

## 1. sane-find-scanner

`sane-find-scanner`는 **SCSI 스캐너와 USB 스캐너 관련 장치 파일을 찾아주는 명령어**이다.

형식:

```bash
sane-find-scanner [옵션] [장치파일명]
```

### 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-q` | 스캐너 장치만 출력 |
| `-v` | 자세한 정보 출력 |
| `-p` | 직렬 포트에 연결된 스캐너만 찾음 |

### 핵심

```text
-q → 스캐너 장치만 출력
-v → 자세한 정보 출력
-p → 직렬 포트 스캐너만 찾기
```

---

## 2. scanimage

`scanimage`는 **이미지를 스캔하는 명령어**이다.

### 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-d` | SANE 장치 파일명 입력 |
| `--format` | 이미지 형식 지정 |
| `-L` | 사용 가능한 스캐너 장치 목록 출력 |

`--format`으로 지정할 수 있는 형식:

```text
pnm
tiff
```

옵션을 지정하지 않으면 기본적으로:

```text
pnm
```

형식으로 지정된다.

### 핵심

```text
scanimage
→ 이미지 스캔

-d
→ 장치 지정

--format
→ 이미지 형식 지정

-L
→ 사용 가능한 스캐너 목록
```

---

## 3. scanadf

`scanadf`는 **자동 문서 공급 장치가 장착된 스캐너에서 여러 개의 사진을 스캔할 때 사용하는 명령어**이다.

형식:

```bash
scanadf [옵션]
```

### 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-d` | SANE 장치 파일명 입력 |
| `-L` | 사용 가능한 스캐너 장치 목록 출력 |

### 핵심

```text
scanadf
→ 자동 문서 공급 장치
→ 여러 장 스캔
```

---

## 4. xcam

`xcam`은 **GUI 기반으로 평판 스캐너나 카메라로부터 이미지를 스캔하는 프로그램**이다.

```text
xcam
→ GUI 기반
→ 평판 스캐너 / 카메라
→ 이미지 스캔
```

---

# 핵심 비교

```text
sane-find-scanner
→ 스캐너 장치 찾기

scanimage
→ 이미지 스캔

scanadf
→ 자동 문서 공급 장치에서 여러 장 스캔

xcam
→ GUI 기반 이미지 스캔
```

## 시험 직전 암기

```text
sane-find-scanner
-q → 장치만
-v → 자세히
-p → 직렬 포트

scanimage
-d → 장치 지정
--format → 형식 지정
-L → 장치 목록

scanadf
-d → 장치 지정
-L → 장치 목록

xcam
→ GUI
```
