# RPM Package Management

## 1. RPM

RPM은 **RedHat Package Manager**의 약자이다.

레드햇에서 만든 패키지 관리 도구로 다음 작업에 사용한다.

```text
설치
업그레이드
삭제
```

레드햇 계열 패키지 파일의 확장자는 다음과 같다.

```text
*.rpm
```

---

## 2. RPM 파일명 구조

예:

```text
sendmail-8.14.3-5.fc11.i586.rpm
```

구성:

```text
sendmail | 8.14.3 | 5 | fc11 | i586
```

| 구분 | 의미 |
|---|---|
| `sendmail` | 패키지명 |
| `8.14.3` | 버전 |
| `5` | 릴리즈 번호 |
| `fc11` | 페도라 버전 |
| `i586` | 아키텍처 |

### 버전

```text
8.14.3

8  → 주버전
14 → 부버전
3  → 패치번호
```

릴리즈 번호는 문제점을 개선할 때마다 붙는 번호이다.

---

## 3. 다른 RPM 파일명 예

```text
kernel-3.10.0-327.el7.x86_64.rpm
```

구성:

```text
kernel | 3.10.0 | 327 | el7 | x86_64
```

```text
kernel → 패키지명
3.10.0 → 버전
327 → 릴리즈 번호
el7 → CentOS / Enterprise Linux 7 계열
x86_64 → Intel 또는 AMD 계열 64비트 CPU
```

---

## 4. RPM 기본 형식

```bash
rpm [옵션] 패키지명
```

---

## 5. RPM 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-i` | 새로운 패키지 설치 |
| `-h` | 패키지를 풀 때 `#` 마크 표시 |
| `-U` | 기존 패키지 업그레이드 |
| `-e` | 패키지 제거 |
| `-q` | 패키지 설치 여부 확인 및 질의 |
| `-v` | 진행 과정을 메시지로 표시 |
| `-vv` | 메시지를 상세히 표시 |

### 연상 암기

```text
-i → install
-U → Upgrade
-e → erase
-q → query
-v → verbose
```

---

## 6. RPM 특수 옵션

| 옵션 | 기능 |
|---|---|
| `--nodeps` | 의존성 관계를 무시하고 설치 |
| `--oldpackage` | 구 버전으로 다운그레이드 |
| `--replacepkgs` | 패키지 재설치 |
| `--replacefiles` | 다른 패키지의 파일을 덮어쓰면서 강제 설치 |
| `--force` | 강제 설치 |

`--force`는 다음 옵션들을 모두 사용하는 것과 같다.

```text
--replacepkgs
--replacefiles
--oldpackage
```

### 핵심

```text
--nodeps
→ 의존성 무시

--oldpackage
→ 구 버전으로 다운그레이드

--replacepkgs
→ 패키지 재설치

--replacefiles
→ 파일 덮어쓰기

--force
→ 강제 설치
```

---

## 7. RPM 검증

설치된 패키지가 변조되었는지 등을 검사할 수 있다.

예:

```bash
rpm -V httpd
```

| 옵션 | 기능 |
|---|---|
| `-V` | verify 검증 기본 옵션 |
| `-a` | 모든 패키지 검사 |

```text
-V → Verify
-a → 모든 패키지
```

---

## 8. RPM 검증 코드

| 코드 | 기능 |
|---|---|
| `5` | MD5 체크섬 변경 |
| `S` | 파일 크기 변경 |
| `L` | 심볼릭 링크 변경 |
| `T` | 파일 수정일 변경 |
| `D` | 장치파일 변경 |
| `U` | 파일 사용자/소유자 변경 |
| `G` | 파일 그룹 변경 |
| `M` | 파일 모드 변경 |

### 연상 암기

```text
5 → MD5

S → Size
L → Link
T → Time
D → Device
U → User
G → Group
M → Mode
```

---

# 핵심 정리

```text
RPM
→ RedHat Package Manager
→ 확장자 .rpm
```

```text
-i → 설치
-U → 업그레이드
-e → 제거
-q → 질의
-h → # 표시
-v → 진행 정보
-vv → 상세 정보
```

```text
--nodeps → 의존성 무시
--oldpackage → 다운그레이드
--replacepkgs → 재설치
--replacefiles → 파일 덮어쓰기
--force → 강제 설치
```

```text
-V → 검증
-a → 모든 패키지 검사
```

```text
5 → MD5
S → Size
L → Link
T → Time
D → Device
U → User
G → Group
M → Mode
```
