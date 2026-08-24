# Network Interface & Kernel Modules

## 1. 네트워크 인터페이스 종류

책에 나온 리눅스 네트워크 인터페이스:

```text
lo
eth
ppp
dl
plip
sl
```

### lo

```text
lo
→ 루프백(Loopback) 인터페이스
```

### eth

```text
eth
→ 이더넷(Ethernet) 인터페이스
→ 인터페이스 번호는 0부터 시작
```

예:

```text
eth0
eth1
```

### ppp

```text
ppp
→ PPP 인터페이스
```

### dl

```text
dl
→ D-Link DE-600 포켓 어댑터 시리즈 인터페이스
```

### plip

```text
plip
→ 병렬(Parallel) 라인 인터페이스
```

### sl

```text
sl
→ SLIP 인터페이스
```

---

# 네트워크 인터페이스 설정

## 2. 자동 인식과 수동 설정

일반적으로 네트워크 인터페이스는 자동으로 인식된다.

자동으로 인식되지 않을 경우:

```text
수동으로 설정
```

네트워크 인터페이스의 수동 설정은 컴파일된 인터페이스 모듈을  
**수동 또는 자동으로 커널에 적재**하는 방식이다.

---

# 수동 모듈 적재

## 3. lsmod

```bash
/sbin/lsmod
```

현재 적재되어 있는 모듈의 정보를 확인한다.

```text
lsmod
→ List
→ 현재 적재 모듈 확인
```

---

## 4. insmod

```bash
/sbin/insmod
```

적재하려는 모듈을 삽입한다.

```text
insmod
→ Insert
→ 모듈 삽입
```

---

## 5. rmmod

```bash
/sbin/rmmod
```

현재 적재되어 있는 모듈을 제거한다.

```text
rmmod
→ Remove
→ 모듈 제거
```

---

## 6. modprobe

```bash
/sbin/modprobe
```

모듈을 적재하거나 제거할 수 있다.

```text
modprobe
→ 모듈 적재
→ 모듈 제거
```

---

# 자동 모듈 적재

## 7. /etc/modprobe.conf

부팅 시 자동으로 적재할 모듈 정보를 읽어 자동 적재한다.

책에 나온 자동 적재 모듈 파일:

```text
/etc/modprobe.conf
```

### 핵심

```text
자동 모듈 적재
→ 부팅 시
→ /etc/modprobe.conf
```

---

# 핵심 정리

```text
lo
→ Loopback

eth
→ Ethernet

ppp
→ PPP

dl
→ D-Link DE-600

plip
→ Parallel Line

sl
→ SLIP
```

```text
lsmod
→ 현재 모듈 확인

insmod
→ 모듈 삽입

rmmod
→ 모듈 제거

modprobe
→ 모듈 적재 / 제거
```

```text
자동 적재
→ /etc/modprobe.conf
```

## 시험 직전 암기

```text
ls = list
ins = insert
rm = remove
```

```text
lsmod = 확인
insmod = 삽입
rmmod = 제거
modprobe = 적재 + 제거
```

```text
lo = Loopback
eth = Ethernet
ppp = PPP
```
