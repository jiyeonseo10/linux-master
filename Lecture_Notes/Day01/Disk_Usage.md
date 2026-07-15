# Disk Usage

## 1. Display Disk Usage

```bash
df
```

**Description**

현재 마운트된 파일 시스템의 디스크 사용량을 표시한다.

**Output**

- Filesystem
- 1K-blocks
- Used
- Available
- Use%
- Mounted on

---

## 2. Display Disk Usage (Human-readable)

```bash
df -h
```

**Description**

디스크 사용량을 사람이 읽기 쉬운 단위(KB, MB, GB)로 출력한다.

**Notes**

- `-h`: Human-readable

---

## 3. Display Inode Usage

```bash
df -i
```

**Description**

파일 시스템의 inode 사용량을 표시한다.

**Notes**

- `-i`: inode 정보 출력
- 디스크 용량이 남아 있어도 inode가 부족하면 파일을 생성할 수 없다.

---

## 4. Display Disk Usage with File System Type

```bash
df -hT
```

**Description**

디스크 사용량과 파일 시스템 종류를 함께 출력한다.

**Notes**

- `-T`: 파일 시스템 종류 표시
- `-h`: 사람이 읽기 쉬운 형식으로 출력

---

## 5. Display Directory Disk Usage

```bash
du -a /home
```

**Description**

`/home` 디렉토리의 파일 및 하위 디렉토리별 디스크 사용량을 출력한다.

**Notes**

- `du` : 디렉터리 사용량 확인
- `-a` : 파일과 디렉터리 모두 출력
