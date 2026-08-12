# Mount & Umount

## 1. Mount

`mount`는 파일 시스템을 특정 **디렉토리에 연결하여 사용할 수 있도록 하는 것**이다.

리눅스에서는 저장 장치의 파일 시스템을 사용하기 위해 특정 디렉토리에 연결해야 한다.

```text
장치의 파일 시스템
       ↓
     Mount
       ↓
특정 디렉토리
```

### Mount Point

파일 시스템이 연결되는 디렉토리를 **마운트 포인트(Mount Point)**라고 한다.

예:

```text
/dev/sdb1 → /mnt
```

- `/dev/sdb1`: 장치
- `/mnt`: 마운트 포인트

---

## 2. Umount

`umount`는 마운트되어 있는 파일 시스템의 **연결을 해제**하는 것이다.

```text
mount
→ 파일 시스템 연결

umount
→ 파일 시스템 연결 해제
```

명칭은 `unmount`가 아니라 **`umount`**이다.

---

## 핵심 정리

```text
Mount
→ 파일 시스템을 특정 디렉토리에 연결

Mount Point
→ 파일 시스템이 연결되는 디렉토리

Umount
→ 마운트된 파일 시스템의 연결 해제
```
