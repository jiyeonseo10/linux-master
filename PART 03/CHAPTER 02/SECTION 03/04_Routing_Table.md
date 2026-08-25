# Routing Table

## 1. 라우팅(Routing)

라우팅은 **송신 패킷이 목적지까지 전송될 수 있도록 경로를 설정하는 작업**이다.

송신 패킷의 목적지 경로 정보가 라우팅 테이블에 존재하면 해당 경로로 패킷을 전송한다.

```text
Routing
→ 목적지까지의 경로 설정

Routing Table
→ 목적지 경로 정보 저장
```

---

## 2. route 명령어

`route` 명령어는 **라우팅 테이블을 설정하거나 확인**할 때 사용한다.

책의 형식:

```bash
route {add|del} [-net|-host NETaddr] [netmask MASKaddr] [[dev] 인터페이스명]
```

### 주요 항목

```text
add
→ 경로 추가

del
→ 경로 삭제

-net
→ 특정 네트워크 경로 지정

-host
→ 특정 호스트 경로 지정

netmask
→ 서브넷 마스크 지정

dev
→ 사용할 인터페이스 지정
```

---

## 3. 특정 네트워크 경로 추가

책의 예:

```bash
route add -net 192.168.10.0 mask 255.255.255.0 dev eth0
```

의미:

```text
192.168.10.0/24 네트워크로 향하는 트래픽
→ eth0 인터페이스로 전송
```

### 핵심

```text
route add -net
→ 특정 네트워크 경로 추가
```

---

## 4. Default Gateway

라우팅 테이블에 목적지 경로가 없는 경우  
**디폴트 게이트웨이(Default Gateway)**로 트래픽을 전달하도록 설정할 수 있다.

책의 형식:

```bash
route add default gw <GW> dev <인터페이스명>
```

책의 예:

```bash
route add default gw 192.168.10.2 dev eth0
```

의미:

```text
Default Gateway
→ 192.168.10.2

사용 인터페이스
→ eth0
```

### 핵심 흐름

```text
라우팅 테이블에 목적지 경로 있음
→ 해당 경로로 전송

목적지 경로 없음
→ Default Gateway로 전송
```

---

# 핵심 정리

```text
route
→ 라우팅 테이블 설정 / 확인
```

```text
add
→ 경로 추가

del
→ 경로 삭제
```

```text
-net
→ 네트워크 경로

-host
→ 호스트 경로

dev
→ 인터페이스 지정
```

```text
route add -net ...
→ 특정 네트워크 경로 추가
```

```text
route add default gw ...
→ 기본 게이트웨이 설정
```

---

## 시험 직전 암기

```text
Routing
= 목적지까지 경로 설정
```

```text
add = 추가
del = 삭제
```

```text
-net = Network
-host = Host
dev = Interface
```

```text
목적지 경로 없음
→ Default Gateway
```

```text
route add default gw 192.168.10.2 dev eth0
→ 기본 게이트웨이 192.168.10.2
→ eth0 사용
```
