# Network Setup & Routing

## 1. IP 주소 설정 방법

책에서는 IP 주소 설정 방법을 다음 3가지로 설명한다.

```text
1. 네트워크 설정 파일 이용
2. ifconfig 명령어 이용
3. 유틸리티 이용
```

---

## 2. 네트워크 설정 파일 이용

책에 나온 파일:

```text
/etc/sysconfig/network
```

또는

```text
/etc/sysconfig/network-scripts/ifcfg-ethX
```

이 파일들을 이용하여 IP 주소와 네트워크 환경을 설정할 수 있다.

---

## 3. ifconfig를 이용한 IP 주소 설정

형식:

```bash
ifconfig 인터페이스명 [IPaddr] netmask [addr] [broadcast [addr]] [up|down]
```

책의 예:

```bash
ifconfig eth0 192.168.10.30 netmask 255.255.255.0 up
```

또는:

```bash
ifconfig eth0 192.168.10.30 netmask 255.255.255.0 broadcast 255.255.255.0 up
```

### 주요 항목

```text
인터페이스명
→ eth0 등

IPaddr
→ IP 주소

netmask
→ 서브넷 마스크

broadcast
→ 브로드캐스트 주소

up
→ 인터페이스 활성화

down
→ 인터페이스 비활성화
```

### 핵심

```text
ifconfig
→ IP 주소 설정

up
→ 활성화

down
→ 비활성화
```

---

# 네트워크 설정 유틸리티

## 4. nmtui

`nmtui`는 다음의 약자이다.

```text
Network Manager Text User Interface
```

텍스트 기반으로 네트워크 설정을 수행한다.

책 화면에서 설정 가능한 항목:

```text
IPv4 주소
게이트웨이
DNS 서버
검색 도메인
라우팅
```

### 핵심

```text
nmtui
→ Text 기반
→ 네트워크 설정
```

---

## 5. gnome-control-center

X 윈도 그래픽 모드에서 사용하는 네트워크 설정 도구이다.

책의 예:

```bash
gnome-control-center network
```

### 핵심

```text
gnome-control-center
→ GUI 기반 네트워크 설정
```

---

## 6. nm-connection-editor

X 윈도 그래픽 모드에서 사용하는 네트워크 연결 설정 도구이다.

책 화면에서는 다음 등을 설정한다.

```text
IP 주소
넷마스크
게이트웨이
DNS 서버
```

### 핵심

```text
nm-connection-editor
→ GUI 기반 네트워크 설정
```

---

# systemctl을 이용한 네트워크 관리

## 7. network 시작

```bash
systemctl start network
```

```text
→ 네트워크 시작
```

---

## 8. network 중지

```bash
systemctl stop network
```

```text
→ 네트워크 중지
```

---

## 9. network 재시작

```bash
systemctl restart network
```

변경된 네트워크 설정을 시스템에 적용할 때 사용한다.

```text
restart
→ 네트워크 재시작
→ 변경 설정 적용
```

---

## 10. network 상태 확인

```bash
systemctl status network
```

활성화 또는 비활성화된 네트워크 상태를 확인한다.

```text
status
→ 네트워크 상태 확인
```

---

# 핵심 정리

```text
IP 설정 방법

1. 설정 파일
2. ifconfig
3. 설정 유틸리티
```

```text
ifconfig
→ IP 주소 설정

netmask
→ 서브넷 마스크

broadcast
→ 브로드캐스트 주소

up
→ 활성화

down
→ 비활성화
```

```text
nmtui
→ Network Manager Text User Interface
→ Text 기반
```

```text
gnome-control-center
nm-connection-editor
→ GUI 기반
```

```text
systemctl start network
→ 시작

systemctl stop network
→ 중지

systemctl restart network
→ 재시작 / 설정 적용

systemctl status network
→ 상태 확인
```

## 시험 직전 암기

```text
nmtui = Text

gnome-control-center
nm-connection-editor
= GUI
```

```text
up = 활성화
down = 비활성화
```

```text
restart = 설정 적용
status = 상태 확인
```
