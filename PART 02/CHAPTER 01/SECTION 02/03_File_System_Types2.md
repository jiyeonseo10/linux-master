## 4. Network File Systems

### NFS

`NFS (Network File System)`는 네트워크를 통해 다른 시스템의 파일 시스템을 공유할 수 있도록 한다.

```text
NFS → UNIX/Linux 계열 → 네트워크 파일 공유
```

### SMB

`SMB (Server Message Block)`는 네트워크에서 파일이나 프린터 등의 자원을 공유하기 위한 프로토콜이다.

```text
SMB → Windows 계열 → 파일/프린터 공유
```

### CIFS

`CIFS (Common Internet File System)`는 SMB와 관련된 파일 공유 방식이다.

```text
SMB / CIFS → Windows 계열의 네트워크 파일 공유
```

### 핵심 비교

```text
UNIX/Linux → NFS
Windows    → SMB / CIFS
```

---

## 5. FAT 계열

### FAT

`FAT (File Allocation Table)`는 파일의 위치 정보를 File Allocation Table을 이용하여 관리하는 파일 시스템이다.

```text
FAT → File Allocation Table
```

### VFAT

기존 FAT를 확장한 형태로 **긴 파일명(Long File Name)**을 지원한다.

```text
VFAT → 긴 파일명 지원
```

### FAT32

FAT 계열을 확장한 파일 시스템이다.

```text
FAT → VFAT / FAT32
```

---

## 6. NTFS

`NTFS (New Technology File System)`는 Windows NT 계열에서 사용하는 파일 시스템이다.

```text
NTFS → Windows NT 계열
```

---

## 7. ISO9660

CD-ROM에서 사용하는 표준 파일 시스템이다.

```text
ISO9660 → CD-ROM
```

---

## 8. UDF

`UDF (Universal Disk Format)`는 광학 디스크에서 사용하는 파일 시스템이다.

```text
UDF → DVD
```

---

## 9. HPFS

`HPFS (High Performance File System)`는 OS/2에서 사용된 파일 시스템이다.

```text
HPFS → OS/2
```

---

# 파일 시스템 전체 핵심 정리

## ext 계열

```text
ext → ext2 → ext3 → ext4

ext2 → Journaling X
ext3 → Journaling O
ext4 → Journaling O
```

## 주요 Journaling 파일 시스템

```text
JFS      → IBM
XFS      → SGI
ReiserFS → Hans Reiser
```

## Network

```text
NFS       → UNIX/Linux
SMB/CIFS  → Windows
```

## Windows 관련

```text
FAT    → File Allocation Table
VFAT   → 긴 파일명 지원
FAT32  → FAT 계열 확장
NTFS   → Windows NT 계열
```

## 기타

```text
ISO9660 → CD-ROM
UDF     → DVD
HPFS    → OS/2
```

---

## 시험 직전 암기

| 파일 시스템 | 핵심 키워드 |
|---|---|
| `ext2` | Journaling X |
| `ext3` | Journaling O |
| `ext4` | ext3 발전, Journaling O |
| `JFS` | IBM |
| `XFS` | SGI |
| `ReiserFS` | Hans Reiser |
| `NFS` | UNIX/Linux 네트워크 공유 |
| `SMB/CIFS` | Windows 네트워크 공유 |
| `VFAT` | 긴 파일명 |
| `NTFS` | Windows NT |
| `ISO9660` | CD-ROM |
| `UDF` | DVD |
| `HPFS` | OS/2 |
