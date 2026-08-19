# File Compression

## 1. 압축 명령어와 확장자

리눅스에서 사용하는 주요 압축 명령어와 확장자는 다음과 같다.

```text
compress  ↔ uncompress → .Z
gzip      ↔ gunzip     → .gz
bzip2     ↔ bunzip2    → .bz2
xz        ↔ unxz       → .xz
```

---

## 2. compress / uncompress

### 압축

```bash
compress 파일명
```

```text
→ .Z 파일 생성
```

### 압축 해제

```bash
uncompress 파일명
```

```text
→ .Z 압축 해제
```

### compress 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-d` | 압축 해제 |
| `-c` | 기존 파일을 지우지 않고 지정 파일로 생성 |
| `-v` | 압축 진행 과정 표시 |
| `-V` | compress 버전 정보 출력 |

### 연상

```text
-d → decompress
-v → verbose
-V → Version
```

---

## 3. gzip / gunzip

### 압축

```bash
gzip 파일명
```

```text
→ .gz 파일 생성
```

### 압축 해제

```bash
gunzip 파일명
```

```text
→ .gz 압축 해제
```

### gzip 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-d` | 압축 해제 |
| `-l` | 압축된 파일 정보 표시 |
| `-v` | 압축 과정 표시 |

### 압축 파일 내용 출력

```bash
zcat 파일명
```

```text
→ .gz 압축 파일 내용 출력
```

---

## 4. bzip2 / bunzip2

### 압축

```bash
bzip2 파일명
```

```text
→ .bz2 파일 생성
```

### 압축 해제

```bash
bunzip2 파일명
```

```text
→ .bz2 압축 해제
```

책에서는 `bzip2`의 옵션이 `gzip`과 동일하다고 설명한다.

### 압축 파일 내용 출력

```bash
bzcat 파일명
```

```text
→ .bz2 압축 파일 내용 출력
```

---

## 5. xz / unxz

### 압축

```bash
xz 파일명
```

```text
→ .xz 파일 생성
```

### 압축 해제

```bash
unxz 파일명
```

```text
→ .xz 압축 해제
```

책에서는 `unxz`가 다음과 동일한 기능이라고 설명한다.

```bash
xz -d
```

### xz 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-z` | 강한 파일 압축 |
| `-d` | 강한 파일 압축 해제 |
| `-v` | 압축 과정 표시 |

---

## 6. 압축률

책 기준:

```text
압축률 가장 낮음
→ compress

압축률 가장 높음
→ xz
```

---

# 핵심 정리

```text
.Z
→ compress / uncompress

.gz
→ gzip / gunzip

.bz2
→ bzip2 / bunzip2

.xz
→ xz / unxz
```

```text
.gz 내용 보기
→ zcat

.bz2 내용 보기
→ bzcat
```

```text
compress
→ 압축률 가장 낮음

xz
→ 압축률 가장 높음
```

## 시험 직전 암기

```text
compress → uncompress → .Z
gzip → gunzip → .gz
bzip2 → bunzip2 → .bz2
xz → unxz → .xz
```
