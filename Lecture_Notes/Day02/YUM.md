# YUM

## Overview

YUM (Yellowdog Updater, Modified) is a package management tool for RPM-based Linux distributions.

It is used to install, update, remove, and manage software packages.

---

## 1. Clean the YUM Cache

```bash
yum clean all
```

**Description**

YUM의 캐시 데이터를 모두 삭제한다.

**Notes**

- 오래된 캐시를 제거할 때 사용한다.
- Repository를 변경한 후 자주 실행한다.

---

## 2. Display YUM Help

```bash
yum
```

**Description**

YUM에서 사용할 수 있는 명령어와 옵션을 확인한다.

---

## Common Commands

| Command | Description |
|---------|-------------|
| `install` | 패키지 설치 |
| `update` | 패키지 업데이트 |
| `upgrade` | 시스템 업그레이드 |
| `remove` / `erase` | 패키지 삭제 |
| `list` | 패키지 목록 조회 |
| `search` | 패키지 검색 |
| `info` | 패키지 상세 정보 |
| `repolist` | Repository 목록 확인 |
| `clean` | 캐시 삭제 |
| `makecache` | Repository 캐시 생성 |

---

## Common Options

| Option | Description |
|--------|-------------|
| `-y` | 모든 질문에 Yes로 응답 |
| `-q` | 조용한(Quiet) 모드 |
| `-v` | 자세한 정보 출력 |
| `--nogpgcheck` | GPG 서명 검사 생략 |
| `--enablerepo` | Repository 활성화 |
| `--disablerepo` | Repository 비활성화 |

---

## Notes

- YUM은 Repository에서 패키지를 검색하고 설치한다.
- Repository 설정이 올바르지 않으면 패키지를 설치할 수 없다.
- `yum clean all` 실행 후 `yum makecache`를 사용하면 새로운 Repository 정보를 다시 생성할 수 있다.
