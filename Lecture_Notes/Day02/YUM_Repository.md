# YUM Repository

## Overview

YUM (Yellowdog Updater, Modified) is a package management tool for RPM-based Linux distributions such as CentOS.

A repository (Repo) is a server that stores software packages and updates.

---

## 1. Move to the Repository Directory

```bash
cd /etc/yum.repos.d
```

**Description**

YUM 저장소 설정 파일이 있는 디렉터리로 이동한다.

---

## 2. List Repository Files

```bash
ls
```

**Description**

현재 설정되어 있는 Repository 파일을 확인한다.

**Example Output**

```text
CentOS-Base.repo
CentOS-Media.repo
```

---

## 3. View the Repository Configuration

```bash
cat CentOS-Base.repo
```

**Description**

`CentOS-Base.repo` 파일의 내용을 출력하여 저장소 설정을 확인한다.

---

## Common Repository Sections

```text
[base]
[updates]
[addons]
[extras]
[centosplus]
```

**Description**

- `base`: 기본 패키지 저장소
- `updates`: 업데이트 패키지
- `addons`: 추가 기능 패키지
- `extras`: 추가 패키지
- `centosplus`: CentOS 확장 패키지

---

## Common Configuration Options

| Option | Description |
|--------|-------------|
| `name` | 저장소 이름 |
| `mirrorlist` | 미러 서버 목록 |
| `baseurl` | 저장소 주소 |
| `gpgcheck` | GPG 서명 검증 여부 |
| `gpgkey` | GPG 키 위치 |

---

## Notes

- Repository 설정 파일은 `/etc/yum.repos.d/`에 저장된다.
- `.repo` 파일을 수정하면 사용할 저장소를 변경할 수 있다.
- YUM은 Repository에서 필요한 패키지를 검색하고 설치한다.
