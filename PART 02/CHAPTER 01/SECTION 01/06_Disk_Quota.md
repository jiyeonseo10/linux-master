# Disk Quota

디스크 쿼터(Disk Quota)는 사용자 또는 그룹이 사용할 수 있는 **디스크 사용량을 제한**하는 기능이다.

## 1. Disk Quota의 제한 대상

디스크 쿼터는 크게 **Block**과 **Inode**를 제한한다.

| 구분 | 의미 |
|---|---|
| Block | 사용할 수 있는 디스크 용량 제한 |
| Inode | 생성할 수 있는 파일 및 디렉토리 개수 제한 |

---

## 2. Soft Limit / Hard Limit

### Soft Limit

일정 기간 동안 초과할 수 있는 제한값이다.

Soft Limit을 초과하면 **Grace Period**가 적용된다.

### Hard Limit

사용자가 **초과할 수 없는 최대 제한값**이다.

### Grace Period

Soft Limit을 초과한 상태로 사용할 수 있는 **유예 기간**이다.

```text
Soft Limit
    ↓
일정 기간 초과 가능
    ↓
Grace Period
    ↓
유예기간 만료 시 제한

Hard Limit
    ↓
초과 불가능
```

---

## 3. Quota 관련 파일 시스템 옵션

`/etc/fstab`에서 디스크 쿼터 관련 옵션을 설정할 수 있다.

| 옵션 | 의미 |
|---|---|
| `quota` | 사용자 할당량 사용 |
| `gquota` | 그룹 할당량 사용 |
| `usrquota` | 사용자 할당량 사용 |
| `grpquota` | 그룹 할당량 사용 |
| `usrjquota=파일명` | 저널 사용자 할당량 |
| `grpjquota=파일명` | 저널 그룹 할당량 |
| `jqfmt=format` | 저널 쿼터 형식 지정 |

예:

```text
defaults,usrjquota=aquota.user,jqfmt=vfsv0
```

---

## 4. Disk Quota 설정 과정

기본적인 설정 순서:

```text
/etc/fstab 설정
       ↓
remount
       ↓
quotacheck
       ↓
quotaon
       ↓
edquota
```

### remount

변경한 파일 시스템 설정을 적용한다.

```bash
mount -o remount /QUOTA
```

---

## 5. quotacheck

파일 시스템의 디스크 사용 상태를 검사하고  
**쿼터 관련 정보를 갱신**한다.

```bash
quotacheck [옵션]
```

주요 옵션:

- `-a`: 모든 파일 시스템 검사
- `-u`: 사용자 쿼터 검사
- `-g`: 그룹 쿼터 검사

예:

```bash
quotacheck -augmn
```

---

## 6. quotaon / quotaoff

### quotaon

디스크 쿼터 기능을 활성화한다.

```bash
quotaon
```

### quotaoff

디스크 쿼터 기능을 비활성화한다.

```bash
quotaoff
```

---

## 7. edquota

사용자 또는 그룹의 디스크 할당량을 **편집기를 이용하여 설정**한다.

### 사용자 설정

```bash
edquota -u username
```

### 그룹 설정

```bash
edquota -g groupname
```

### 주요 옵션

| 옵션 | 의미 |
|---|---|
| `-u` | 사용자 쿼터 설정 |
| `-g` | 그룹 쿼터 설정 |
| `-t` | Grace Period 설정 |
| `-p` | 특정 사용자의 쿼터 설정을 다른 사용자에게 적용 |

`edquota` 화면에서는 Block과 Inode 각각에 대해  
Soft Limit과 Hard Limit을 설정할 수 있다.

```text
Filesystem  blocks  soft  hard  inodes  soft  hard
```

- `blocks`: 현재 사용 중인 디스크 블록
- Block `soft / hard`: 디스크 용량 제한
- `inodes`: 현재 사용 중인 inode
- Inode `soft / hard`: 파일 및 디렉토리 개수 제한

---

## 8. setquota

`edquota`와 달리 **편집기를 사용하지 않고 명령행에서 직접** 디스크 할당량을 설정한다.

```text
edquota  → 편집기를 이용하여 설정
setquota → 명령행에서 직접 설정
```

---

## 핵심 정리

```text
Block       → 디스크 용량
Inode       → 파일/디렉토리 개수

Soft Limit  → 일정 기간 초과 가능
Hard Limit  → 초과 불가능
Grace Period → Soft Limit 초과 유예기간
```

주요 명령어:

```text
quotacheck → 쿼터 관련 검사
quotaon    → 쿼터 활성화
quotaoff   → 쿼터 비활성화
edquota    → 편집기로 쿼터 설정
setquota   → 명령행에서 직접 쿼터 설정
```

설정 순서:

```text
fstab → remount → quotacheck → quotaon → edquota
```
