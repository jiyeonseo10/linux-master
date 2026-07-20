# Umask

## Overview

`umask` is used to set the default permissions for newly created files and directories.

---

## Default Permissions

When a new file or directory is created, Linux applies default permissions and then subtracts the umask value.

| Type | Default Permission |
|------|-------------------:|
| File | 666 (rw-rw-rw-) |
| Directory | 777 (rwxrwxrwx) |

Example

```text
umask = 022

File      : 666 - 022 = 644
Directory : 777 - 022 = 755
```

---

## 1. Display Current Umask

```bash
umask
```

**Description**

현재 umask 값을 숫자 형식으로 출력한다.

**Example Output**

```text
0022
```

---

## 2. Display Symbolic Umask

```bash
umask -S
```

**Description**

현재 umask 값을 기호(Symbolic) 형식으로 출력한다.

**Example Output**

```text
u=rwx,g=rx,o=rx
```

---

## 3. Create a Test Directory

```bash
mkdir /test1
```

**Description**

새로운 디렉터리를 생성하여 기본 권한을 확인한다.

---

## 4. Create a Test File

```bash
touch c.txt
```

**Description**

새 파일을 생성하여 umask가 적용된 기본 권한을 확인한다.

---

## 5. Check File Permissions

```bash
ls -la
```

**Description**

새로 생성된 파일의 권한을 확인한다.

---

## 6. Change File Permissions

```bash
chmod ugo+rwx c.txt
```

**Description**

모든 사용자(User, Group, Others)에게 Read, Write, Execute 권한을 부여한다.

**Notes**

- `u`: User (Owner)
- `g`: Group
- `o`: Others
- `+`: 권한 추가
- `rwx`: Read, Write, Execute

---

## Notes

- `umask`는 **새로 생성되는 파일과 디렉토리의 기본 권한**에만 영향을 준다.
- 기존 파일의 권한은 변경하지 않는다.
- 기존 파일의 권한을 변경하려면 `chmod`를 사용한다.
