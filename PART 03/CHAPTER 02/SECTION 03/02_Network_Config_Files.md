# Network Configuration Files

## 1. /etc/sysconfig/network

시스템 전체의 **기본 네트워크 정보**를 설정하는 파일이다.

주요 항목:

```text
NETWORKING=yes|no
→ 네트워크 사용 여부

HOSTNAME=호스트명
→ 전체 도메인명 지정

GATEWAY=GWIP주소
→ 게이트웨이 주소

GATEWAYDEV=디바이스명
→ 게이트웨이로 연결된 장비명
```

### 핵심

```text
/etc/sysconfig/network
→ 시스템 전체 네트워크 설정
→ HOSTNAME
→ GATEWAY
```

---

## 2. /etc/sysconfig/network-scripts/ifcfg-ethX

지정된 **네트워크 인터페이스의 환경 설정 정보**가 저장되는 파일이다.

```text
ifcfg-eth0
→ 첫 번째 이더넷 카드 설정 파일

ifcfg-eth1
→ 두 번째 이더넷 카드 설정 파일
```

### 주요 항목

```text
DEVICE=디바이스명
→ 네트워크 장치명

BOOTPROTO=static|dhcp|none
→ IP 설정 방식

BROADCAST=브로드캐스트주소
→ 브로드캐스트 주소

IPADDR=IP주소
→ 할당받은 호스트 IP 주소

NETMASK=서브넷마스크
→ 할당받은 서브넷 마스크

NETWORK=네트워크주소
→ 네트워크 주소

ONBOOT=yes|no
→ 부팅 시 해당 장비 활성화 여부

TYPE=네트워크타입
→ 장치가 실행하는 네트워크 환경 지정
```

---

## 3. BOOTPROTO

```text
static
→ 고정 IP 주소 환경

dhcp
→ 유동 IP 주소 환경

none
→ IP 주소 지정하지 않음
```

### 핵심

```text
BOOTPROTO=static → 고정 IP
BOOTPROTO=dhcp   → 유동 IP
BOOTPROTO=none   → IP 지정 안 함
```

---

## 4. /etc/resolv.conf

기본적으로 사용할 **도메인명과 네임서버**를 설정한다.

주요 항목:

```text
domain
→ 도메인명

nameserver
→ 네임서버 주소
```

네임서버는 여러 개 지정할 수 있으며 첫 번째 네임서버가 작동하지 않으면 다음 네임서버가 동작한다.

### 핵심

```text
/etc/resolv.conf
→ DNS 설정
→ domain
→ nameserver
```

---

## 5. /etc/hosts

IP 주소와 도메인명을 **1:1로 매핑**한다.

DNS 질의를 거치지 않고 직접 IP 주소를 얻을 수 있다.

형식:

```text
IP주소 도메인명
```

예:

```text
192.168.10.30 youngjin
```

### 핵심

```text
/etc/hosts
→ IP 주소 ↔ 도메인명 직접 매핑
```

---

## 6. /etc/host.conf

DNS 서비스를 제공할 때 먼저 검사하는 파일이며 설정에 따라 **호스트 조회 순서**를 결정한다.

예:

```text
order hosts, bind
```

### 핵심

```text
/etc/host.conf
→ 호스트 조회 순서
```

---

# 파일별 핵심 비교

```text
/etc/sysconfig/network
→ 시스템 전체 네트워크 기본 설정
→ HOSTNAME / GATEWAY
```

```text
/etc/sysconfig/network-scripts/ifcfg-ethX
→ 개별 네트워크 인터페이스 설정
→ DEVICE / BOOTPROTO / IPADDR / NETMASK / ONBOOT
```

```text
/etc/resolv.conf
→ DNS 설정
→ domain / nameserver
```

```text
/etc/hosts
→ IP ↔ 도메인명 직접 매핑
```

```text
/etc/host.conf
→ 조회 순서
```

---

# 시험 직전 암기

```text
network
→ 전체 설정
```

```text
ifcfg-ethX
→ 랜카드 개별 설정
```

```text
resolv.conf
→ DNS 서버
```

```text
hosts
→ IP와 이름 직접 매핑
```

```text
host.conf
→ 조회 순서
```

```text
IPADDR  = IP 주소
NETMASK = 서브넷 마스크
ONBOOT  = 부팅 시 활성화 여부
GATEWAY = 게이트웨이 주소
```
