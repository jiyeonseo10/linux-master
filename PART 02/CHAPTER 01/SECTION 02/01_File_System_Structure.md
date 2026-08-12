# File System Structure

리눅스 파일 시스템은 디스크를 여러 **Block Group**으로 나누어 데이터를 관리한다.

## 1. 파일 시스템 기본 구조

각 Block Group은 다음과 같은 영역으로 구성된다.

```text
Block Group
├── Super Block
├── Group Descriptor Table
├── Block Bitmap
├── inode Bitmap
├── inode Table
└── Data Blocks
```

---

## 2. Super Block

파일 시스템의 **전체적인 정보**를 저장한다.

주요 정보:
- 블록의 크기
- 블록의 개수
- inode의 개수
- 파일 시스템 관련 정보

```text
Super Block = 파일 시스템 전체 정보
```

---

## 3. Group Descriptor Table

각 **Block Group을 관리하기 위한 정보**를 저장한다.

주요 정보:
- Block Bitmap 관련 정보
- inode Bitmap 관련 정보
- inode Table 관련 정보
- 그룹 내 빈 블록 수
- inode 관련 정보

```text
Super Block
→ 파일 시스템 전체 정보

Group Descriptor Table
→ 각 Block Group 관리 정보
```

---

## 4. Block Bitmap

각 데이터 블록의 **사용 여부**를 관리한다.

```text
Block Bitmap = 블록 사용 상태
```

---

## 5. inode Bitmap

각 inode의 **사용 여부**를 관리한다.

```text
inode Bitmap = inode 사용 상태
```

---

## 6. inode

파일에 대한 **정보(메타데이터)**를 저장한다.

주요 정보:
- 파일의 고유 번호
- 파일 형태
- 파일 크기
- 파일 소유자
- 데이터 블록의 위치

### 중요

**파일 이름은 inode에 저장되지 않는다.**

```text
inode
→ 파일에 대한 정보
→ 파일 이름은 저장하지 않음
```

---

## 7. inode Table

여러 inode에 대한 정보를 모아 관리하는 영역이다.

```text
inode Table
├── inode 1
├── inode 2
├── inode 3
└── ...
```

---

## 8. Data Blocks

파일의 **실제 데이터**가 저장되는 영역이다.

```text
inode       → 파일에 대한 정보
Data Block  → 파일의 실제 내용
```

---

## 핵심 정리

| 구조 | 역할 |
|---|---|
| Super Block | 파일 시스템 전체 정보 |
| Group Descriptor Table | 각 Block Group 관리 정보 |
| Block Bitmap | 블록 사용 여부 |
| inode Bitmap | inode 사용 여부 |
| inode Table | inode 정보 관리 |
| inode | 파일의 메타데이터 |
| Data Blocks | 파일의 실제 데이터 |

### 시험 포인트

```text
Super Block
→ 파일 시스템 전체 정보

Group Descriptor Table
→ 각 Block Group 관리 정보

Block Bitmap
→ 블록 사용 여부

inode Bitmap
→ inode 사용 여부

inode
→ 파일 정보
→ 파일 이름은 저장하지 않음

Data Block
→ 실제 데이터
```
