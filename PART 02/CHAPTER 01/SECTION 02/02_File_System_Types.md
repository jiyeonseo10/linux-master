# File System Types

## 1. ext 계열 파일 시스템

리눅스의 ext 계열 파일 시스템은 다음과 같이 발전하였다.

```text
ext → ext2 → ext3 → ext4
```

### ext

- Extended File System
- 리눅스 초기 파일 시스템

### ext2

- ext를 개선한 파일 시스템
- **Journaling을 지원하지 않음**

```text
ext2 → Journaling X
```

### ext3

- ext2를 기반으로 발전
- **Journaling 기능 지원**

```text
ext2 + Journaling → ext3
```

### ext4

- ext3를 발전시킨 파일 시스템
- Journaling 지원
- ext3에 비해 성능 및 기능 개선

---

## 2. Journaling

Journaling은 파일 시스템의 변경 작업과 관련된 정보를 기록하여  
시스템 장애 발생 시 **파일 시스템의 복구를 돕는 기능**이다.

```text
파일 변경 작업
      ↓
Journal에 관련 정보 기록
      ↓
시스템 장애 발생
      ↓
빠른 복구에 활용
```

### ext 계열 비교

| 파일 시스템 | Journaling |
|---|---|
| ext2 | X |
| ext3 | O |
| ext4 | O |

```text
ext2 → Journaling X
ext3 → Journaling O
ext4 → Journaling O
```

---

## 3. 주요 Journaling 파일 시스템

### JFS

- Journaling File System
- IBM에서 개발

```text
JFS → IBM
```

### XFS

- 저널링 파일 시스템
- SGI에서 개발

```text
XFS → SGI
```

### ReiserFS

- 저널링 파일 시스템
- Hans Reiser가 개발

```text
ReiserFS → Hans Reiser
```

---

## 핵심 정리

```text
ext → ext2 → ext3 → ext4

ext2 → Journaling X
ext3 → Journaling O
ext4 → Journaling O
```

Journaling:

```text
변경 작업 관련 정보를 기록
→ 장애 발생 시 파일 시스템 복구에 도움
```

주요 저널링 파일 시스템:

```text
JFS      → IBM
XFS      → SGI
ReiserFS → Hans Reiser
```
