# NFS & RPC

## 1. NFS

`NFS`는 **Network File System**의 약자이다.

네트워크 기반으로 다른 시스템과 파일 시스템을 공유하기 위한 클라이언트/서버 프로그램이다.

주요 특징:

```text
원격 리눅스 서버의 특정 디렉토리를
로컬 시스템의 하위 디렉토리처럼 사용
```

다른 컴퓨터의 파일 시스템을 마운트하여 자신의 디렉토리처럼 사용할 수 있다.

책에서는 1984년 Sun Microsystems에서 개발되었다고 설명한다.

### 핵심

```text
NFS
→ Network File System
→ 원격 파일 시스템 공유
→ 원격 디렉토리를 로컬처럼 사용
```

---

## 2. NFS와 portmap

NFS 서비스가 실행되기 전에 `portmap`이 먼저 실행되어 있어야 한다.

`portmap`은 NIS, NFS 등의 RPC 연결에 관여하는 데몬이다.

```text
portmap
→ RPC 연결에 관여
→ NFS 실행 전에 먼저 동작
```

---

## 3. NFS 관련 데몬

책에 나온 NFS 관련 데몬:

```text
nfsd
rpc.mountd
rpc.statd
rpc.lockd
rpc.quotad
```

### NFS 서버

```text
nfsd
rpc.mountd
rpc.statd
rpc.lockd
```

### NFS 클라이언트

```text
rpc.statd
rpc.lockd
rpc.quotad
```

### 핵심

```text
NFS Server
→ nfsd
→ rpc.mountd
```

---

# RPC

## 4. RPC 개념

`RPC`는 **Remote Procedure Call**의 약자이다.

책에서는 **동적으로 서비스와 포트를 연결할 때 사용하는 방법**이라고 설명한다.

```text
RPC
→ Remote Procedure Call
→ 서비스와 포트를 동적으로 연결
```

---

## 5. 정적 포트와 동적 포트

서비스와 포트가 정적으로 구성된 경우:

```text
/etc/services
```

파일을 참조한다.

동적으로 포트를 할당받아 사용하는 경우:

```text
RPC
→ rpcbind
```

를 사용한다.

책에서는 SUN 계열에서 `sunrpc`라는 명칭도 사용한다고 설명한다.

---

## 6. rpcbind

동적으로 포트를 할당받으려는 원격 서비스는 `rpcbind`에 접속한다.

책에서 `rpcbind`의 포트 번호는:

```text
111
```

### 핵심

```text
rpcbind
→ Port 111
```

---

## 7. RPC 동작 과정

```text
1. 원격 서비스가 rpcbind(111)에 접속

2. 서비스용 포트 번호 할당 요청

3. rpcbind가 사용하지 않는 포트 번호를 찾아
   요청한 서비스에 할당

4. 할당받은 포트를 사용하여 서비스 요청

5. 시스템이 해당 포트의 서비스 프로그램에 패킷 전달
```

### 핵심 흐름

```text
서비스
→ rpcbind 111
→ 포트 요청
→ 포트 할당
→ 할당된 포트로 통신
```

---

# 핵심 비교

```text
NFS
→ 원격 파일 시스템 공유
→ 원격 디렉토리를 로컬처럼 사용
```

```text
RPC
→ 서비스와 포트의 동적 연결
```

```text
portmap
→ NFS / NIS 등의 RPC 연결에 관여
```

```text
rpcbind
→ Port 111
```

```text
정적 포트/서비스
→ /etc/services

동적 포트
→ RPC / rpcbind
```

## 시험 직전 암기

```text
NFS = 원격 파일 시스템 공유
```

```text
portmap = RPC 연결
```

```text
RPC = 동적 포트 연결
```

```text
rpcbind = 111
```

```text
/etc/services = 정적 서비스/포트
```
