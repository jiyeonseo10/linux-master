# Tar

## Overview

`tar` (Tape Archive)는 여러 파일과 디렉터리를 하나의 아카이브 파일로 묶는 명령어이다.

- 아카이브 생성
- 아카이브 내용 확인
- 아카이브 압축
- 아카이브 해제

---

## Common Options

| Option | Description |
|--------|-------------|
| `-c` | Create a new archive |
| `-x` | Extract files |
| `-t` | List archive contents |
| `-v` | Verbose mode (show progress) |
| `-f` | Specify archive file |
| `-z` | Compress or decompress with gzip |

---

## 1. Create Test Files

```bash
mkdir /test
cd /test

cp /etc/services .

touch file1
touch file2
touch file3
```

**Description**

실습을 위한 테스트 파일을 생성한다.

---

## 2. Create a Tar Archive

```bash
tar -cvf doom.tar *
```

**Description**

현재 디렉터리의 모든 파일을 `doom.tar` 아카이브로 생성한다.

**Notes**

- `c`: Create
- `v`: Verbose
- `f`: Archive file

---

## 3. List Archive Contents

```bash
tar -tvf doom.tar
```

**Description**

아카이브를 해제하지 않고 내부 파일 목록을 확인한다.

---

## 4. Extract Archive

```bash
tar -xvf doom.tar
```

**Description**

`doom.tar` 파일을 현재 디렉토리에 압축 해제한다.

**Notes**

- `x`: Extract

---

## 5. Create a Compressed Archive

```bash
tar -czvf doom.tar.gz *
```

**Description**

gzip으로 압축된 tar 아카이브를 생성한다.

**Notes**

- `z` : gzip 압축 사용

---

## 6. List Compressed Archive Contents

```bash
tar -tvzf doom.tar.gz
```

**Description**

압축을 해제하지 않고 `tar.gz` 내부 파일 목록을 확인한다.

---

## 7. Remove Original Files

```bash
rm -f fi* services
```

**Description**

원본 파일을 삭제하여 복원 실습을 준비한다.

---

## 8. Extract Compressed Archive

```bash
tar -xzvf doom.tar.gz
```

**Description**

`doom.tar.gz` 파일을 압축 해제하여 원본 파일을 복원한다.

---

## Summary

| Command | Description |
|---------|-------------|
| `tar -cvf` | tar 파일 생성 |
| `tar -tvf` | tar 내용 확인 |
| `tar -xvf` | tar 압축 해제 |
| `tar -czvf` | tar.gz 생성 |
| `tar -tvzf` | tar.gz 내용 확인 |
| `tar -xzvf` | tar.gz 압축 해제 |
