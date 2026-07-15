# File Permissions

## Overview

Linux uses a permission system to control access to files and directories.

There are three permission categories:

- Owner (User)
- Group
- Others

Each category can have the following permissions:

- Read (r)
- Write (w)
- Execute (x)

---

## 1. Permission Values

| Permission | Value |
|------------|------:|
| r | 4 |
| w | 2 |
| x | 1 |

### Examples

| Number | Permission |
|--------:|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 0 | --- |

---

## 2. Viewing Permissions

```bash
ls -l
```

**Description**

파일 및 디렉토리의 권한을 확인한다.

---

## 3. Create Test Files

```bash
touch a.txt
touch b.txt
touch c.txt
touch d.txt
```

**Description**

권한 변경 실습을 위한 테스트 파일을 생성한다.

---

## 4. Remove Files

```bash
rm c.txt
rm d.txt
```

**Description**

테스트 파일을 삭제한다.

---

## 5. Change File Permissions

```bash
chmod 755 a.txt
```

**Description**

파일 권한을 `755`로 변경한다.

**Notes**

- Owner: rwx
- Group: r-x
- Others: r-x

---

## 6. Set SUID

```bash
chmod 4755 a.txt
```

**Description**

SUID(Set User ID) 권한을 설정한다.

**Notes**

- 앞자리 `4`는 SUID를 의미한다.
- 실행 시 파일 소유자의 권한으로 실행된다.

---

## 7. Set SGID

```bash
chmod 2755 a.txt
```

**Description**

SGID(Set Group ID) 권한을 설정한다.

**Notes**

- 앞자리 `2`는 SGID를 의미한다.
- 실행 시 파일 그룹의 권한으로 실행된다.

---

## 8. Set Sticky Bit

```bash
chmod 1755 a.txt
```

**Description**

Sticky Bit를 설정한다.

**Notes**

- 앞자리 `1`은 Sticky Bit를 의미한다.
- 주로 `/tmp` 디렉터리에서 사용된다.
