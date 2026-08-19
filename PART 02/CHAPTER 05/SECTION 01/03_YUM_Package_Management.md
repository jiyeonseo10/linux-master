# YUM Package Management

## 1. YUM

YUM은 **Yellowdog Updater Modified**의 약자이다.

네트워크를 통해 기존 RPM 패키지의 업데이트를 자동으로 수행하고, 새로운 패키지 설치 및 제거를 수행한다.

주요 특징:

- RPM의 의존성 문제를 해결하기 위한 유틸리티
- 인터넷 기반으로 설치하므로 네트워크 연결 필요
- Fedora 22 이후에는 YUM의 문제점을 보완한 `DNF`가 사용됨

```text
YUM
→ Yellowdog Updater Modified
→ RPM 의존성 문제 해결
→ 네트워크 기반
→ Fedora 22 이후 DNF
```

---

## 2. 설치 관련 명령어

### 패키지 설치

```bash
yum install 패키지명
```

설치 여부를 사용자에게 묻는다.

### 자동 설치

```bash
yum -y install 패키지명
```

설치 여부를 묻는 질문에 자동으로 `Yes`로 간주하여 설치한다.

### 패키지 그룹 설치

```bash
yum groupinstall 패키지명
```

지정한 패키지 그룹을 설치한다.

### 패키지 업데이트

```bash
yum update 패키지명
```

책에서는 `yum install`과 동일한 기능으로 설명한다.

### 로컬 RPM 설치

```bash
yum localinstall 패키지명
```

인터넷을 통해 다운로드하지 않고 현재 디렉토리 내의 `*.rpm` 파일을 설치한다.

---

## 3. 삭제 관련 명령어

### 패키지 제거

```bash
yum remove 패키지명
```

지정한 패키지를 제거한다.

### 패키지 그룹 제거

```bash
yum groupremove 패키지명
```

지정한 패키지 그룹을 제거한다.

---

## 4. 패키지 정보 확인

### 패키지 요약 정보

```bash
yum info 패키지명
```

패키지 요약 정보를 확인한다.

### 전체 패키지 정보

```bash
yum list
```

전체 패키지 정보를 출력한다.

### 패키지 그룹 정보

```bash
yum grouplist
```

패키지 그룹 정보를 출력한다.

---

## 5. 업데이트 확인

```bash
yum check update
```

패키지 중 업데이트가 가능한 패키지 목록을 출력한다.

```bash
yum check-update
```

업데이트가 필요한 패키지를 출력한다.

---

## 6. 패키지 검색

```bash
yum search 문자열
```

해당 문자열이 포함된 패키지를 검색한다.

---

## 7. 작업 이력 확인

```bash
yum history
```

패키지 설치, 삭제 등의 작업 이력을 확인한다.

---

# 핵심 정리

```text
yum install
→ 패키지 설치

yum -y install
→ 자동 Yes 설치

yum groupinstall
→ 패키지 그룹 설치

yum update
→ 패키지 업데이트

yum localinstall
→ 현재 디렉토리의 rpm 파일 설치
```

```text
yum remove
→ 패키지 제거

yum groupremove
→ 패키지 그룹 제거
```

```text
yum info
→ 패키지 요약 정보

yum list
→ 전체 패키지 정보

yum grouplist
→ 패키지 그룹 정보

yum search
→ 문자열이 포함된 패키지 검색

yum history
→ 설치/삭제 작업 이력
```

```text
YUM
→ RPM 의존성 문제 해결
→ 네트워크 기반
→ Fedora 22 이후 DNF
```
