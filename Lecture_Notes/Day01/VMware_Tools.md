# VMware Tools Installation

## 1. Create a Mount Directory

**Command**

```bash
mkdir /mnt/vmware
```

**Description**

VMware Tools CD를 마운트할 디렉터리를 생성한다.

---

## 2. Mount the VMware Tools CD

**Command**

```bash
mount -t iso9660 /dev/cdrom /mnt/vmware
```

**Description**

VMware Tools CD를 `/mnt/vmware` 디렉터리에 마운트한다.

**Notes**

- `mount` : 파일 시스템을 마운트하는 명령어
- `-t iso9660` : CD-ROM 파일 시스템 지정
- `/dev/cdrom` : CD-ROM 장치 파일
- `/mnt/vmware` : 마운트 위치

---

## 3. Check the Mounted Files

**Command**

```bash
cd /mnt/vmware
ls
```

**Description**

마운트된 VMware Tools 설치 파일이 정상적으로 존재하는지 확인한다.

---

## 4. Create a Working Directory

**Command**

```bash
mkdir /Vmware
```

**Description**

설치 파일을 복사하여 작업할 디렉터리를 생성한다.

---

## 5. Copy the Installation Package

**Command**

```bash
cp VMwareTools-10.3.26-22085142.tar.gz /Vmware/
```

**Description**

VMware Tools 설치 파일을 작업 디렉터리(`/Vmware`)로 복사한다.

**Notes**

- `cp` : 파일 복사 명령어
- `/Vmware` : 작업 디렉터리

---

## 6. Verify the Copied File

**Command**

```bash
cd /Vmware
ls
```

**Description**

설치 파일이 정상적으로 복사되었는지 확인한다.

---

## 7. Extract the Installation Package

**Command**

```bash
tar -zxvf VMwareTools-10.3.26-22085142.tar.gz
```

**Description**

압축 파일을 해제한다.

**Notes**

- `z` : gzip 압축 해제
- `x` : 압축 해제
- `v` : 진행 과정 출력
- `f` : 파일 지정

---

## 8. Move to the Installation Directory

**Command**

```bash
cd vmware-tools-distrib
ls
```

**Description**

압축 해제된 VMware Tools 설치 디렉터리로 이동하여 파일 목록을 확인한다.

---

## 9. Run the Installer

**Command**

```bash
./vmware-install.pl
```

**Description**

VMware Tools 설치 스크립트를 실행한다.

**Notes**

- `./` : 현재 디렉터리에서 실행
- `vmware-install.pl` : VMware Tools 설치 스크립트
