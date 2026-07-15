# Create a Mount Directory

## Command

```bash
mkdir /mnt/vmware
```

## Description

Creates a directory that will be used as the mount point for the VMware Tools CD.

> VMware Tools CD를 마운트할 디렉토리를 생성한다.

## Syntax

```bash
mkdir [OPTION] DIRECTORY
```

## Notes

- `mkdir`: 새로운 디렉토리를 생성하는 명령어
- `/mnt`: 임시로 파일 시스템을 마운트할 때 사용하는 디렉토리
- `/mnt/vmware`: VMware Tools CD를 연결할 마운트 지점

## Example

```bash
mkdir /mnt/vmware
ls /mnt
```

Output

```text
vmware
```
