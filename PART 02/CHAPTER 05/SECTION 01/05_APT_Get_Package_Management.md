# APT-GET Package Management

## 1. apt-get

`apt-get`은 **데비안 리눅스에서 소프트웨어 설치와 제거를 위한 패키지 관리 유틸리티**이다.

패키지 관련 정보를 확인하거나 설치 시 발생할 수 있는 **의존성 충돌 문제를 해결하기 위해** 다음 파일을 참조한다.

```text
/etc/apt/sources.list
```

### 핵심

```text
apt-get
→ Debian 계열
→ 패키지 설치 / 제거
→ 의존성 문제 해결
→ /etc/apt/sources.list 참조
```

---

## 2. /etc/apt/sources.list

`/etc/apt/sources.list` 파일은 다음 정보로 구성된다.

```text
패키지 유형
→ 바이너리 / 소스

저장소 주소
→ URL

우분투 버전 정보

카테고리
```

즉,

```text
/etc/apt/sources.list
→ 패키지를 가져올 저장소 정보
```

---

## 3. 기본 형식

```bash
apt-get [옵션] 명령어 패키지명
```

---

## 4. 주요 명령어

| 명령어 | 기능 |
|---|---|
| `install` | 새 패키지 설치 |
| `dist-upgrade` | 의존성을 검사하여 설치 |
| `update` | 새 패키지 목록 가져오기 및 `/etc/apt/sources.list`의 인덱스 정보 업데이트 |
| `upgrade` | 업그레이드 실행 |
| `remove` | 패키지 제거 |

---

## 5. update와 upgrade 구분

이 둘은 반드시 구분한다.

```text
apt-get update
→ 패키지 목록 / 인덱스 정보 갱신

apt-get upgrade
→ 실제 패키지 업그레이드
```

---

## 6. 주요 옵션

| 옵션 | 기능 |
|---|---|
| `-y` | 모든 질문을 표시하지 않고 자동으로 `예` 처리 |
| `-u` | 업그레이드할 패키지 목록 표시 |
| `-V` | 자세한 버전 표시 |

### 연상 암기

```text
-y
→ Yes
→ 자동 예

-u
→ Upgrade
→ 업그레이드할 패키지 목록

-V
→ Version
→ 자세한 버전 표시
```

---

# 핵심 정리

```text
apt-get
→ Debian 계열 패키지 관리
→ /etc/apt/sources.list 참조
```

```text
install
→ 새 패키지 설치

dist-upgrade
→ 의존성 검사하여 설치

update
→ 패키지 목록 / 인덱스 갱신

upgrade
→ 실제 업그레이드

remove
→ 패키지 제거
```

```text
-y → 자동 Yes
-u → 업그레이드할 패키지 목록
-V → 자세한 버전 표시
```

## 시험 직전 암기

```text
update = 목록 갱신
upgrade = 실제 업그레이드

-y = Yes
-u = Upgrade list
-V = Version
```
