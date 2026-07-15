# File Permissions

## 1. Create Test Files

```bash
touch a.txt
touch b.txt
touch c.txt
touch d.txt
```

**Description**

권한 변경 실습을 위한 테스트 파일을 생성한다.

---

## 2. Remove Files

```bash
rm c.txt
rm d.txt
```

**Description**

테스트 파일을 삭제한다.

---

## 3. Set Permission (755)

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

## 4. Set SUID Permission

```bash
chmod 4755 a.txt
```

**Description**

SUID(Set User ID) 권한을 설정한다.

**Notes**

- 앞자리 `4`는 SUID를 의미한다.
- 실행 시 파일 소유자의 권한으로 실행된다.

---

## 5. Set SGID Permission

```bash
chmod 2755 a.txt
```

**Description**

SGID(Set Group ID) 권한을 설정한다.

**Notes**

- 앞자리 `2`는 SGID를 의미한다.
- 실행 시 파일 그룹의 권한으로 실행된다.

---

## 6. Set Sticky Bit

```bash
chmod 1755 a.txt
```

**Description**

Sticky Bit를 설정한다.

**Notes**

- 앞자리 `1`은 Sticky Bit를 의미한다.
- 주로 `/tmp` 디렉터리에서 사용된다.

---

## 7. Set Multiple Special Permissions

```bash
chmod 4655 b.txt
```

**Description**

SUID와 일반 권한을 함께 설정하는 예제이다.

**Notes**

- 특수 권한은 숫자(1, 2, 4)를 조합하여 설정할 수 있다.

---

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

## Permission Values

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

## Viewing Permissions

```bash
ls -l
```

**Description**

파일 및 디렉토리의 권한을 확인한다.

---

## Create Test Files

```bash
touch a.txt
touch b.txt
touch c.txt
touch d.txt
```

**Description**

권한 변경 실습을 위한 테스트 파일을 생성한다.

---

## Remove Files

```bash
rm c.txt
rm d.txt
```

**Description**

테스트 파일을 삭제한다.

---

## Change File Permissions

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

## Set SUID

```bash
chmod 4755 a.txt
```

**Description**

SUID(Set User ID) 권한을 설정한다.

**Notes**

- 앞자리 `4`는 SUID를 의미한다.
- 실행 시 파일 소유자의 권한으로 실행된다.

---

## Set SGID

```bash
chmod 2755 a.txt
```

**Description**

SGID(Set Group ID) 권한을 설정한다.

**Notes**

- 앞자리 `2`는 SGID를 의미한다.
- 실행 시 파일 그룹의 권한으로 실행된다.

---

## Set Sticky Bit

```bash
chmod 1755 a.txt
```

**Description**

Sticky Bit를 설정한다.

**Notes**

- 앞자리 `1`은 Sticky Bit를 의미한다.
- 주로 `/tmp` 디렉터리에서 사용된다.
