# Process Daemon

## 1. 데몬(Daemon)

데몬은 리눅스 시스템이 부팅될 때 자동으로 실행되는 **백그라운드 프로세스**이다.

주요 특징:

- 메모리에 상주
- 사용자의 특정 요청이 오면 즉시 실행
- 주기적이고 지속적인 서비스 요청을 처리
- 일반 사용자는 이 프로세스를 볼 수 있는 권한이 없음

```text
Daemon
→ 백그라운드 프로세스
→ 메모리에 상주
→ 서비스 요청 처리
```

---

## 2. standalone 데몬

서비스 요청이 들어오기 전부터 **항상 메모리에 상주**하는 방식이다.

- 독립적으로 수행
- 요청에 빠르게 응답 가능
- 빠른 응답 속도가 필요한 경우 사용
- 항상 메모리에 있어 메모리 점유로 인한 서버 부하가 큼

관련 서비스:

```text
http
mysql
nameserver
sendmail
```

책의 실행 스크립트 위치:

```text
/etc/inetd.d/
```

### 핵심

```text
standalone
→ 항상 메모리에 상주
→ 응답 빠름
→ 메모리 점유 큼
```

---

## 3. inetd 데몬

`inetd`는 다른 데몬들의 상위에 존재하는 **슈퍼 데몬(Super Daemon)**이다.

- 자체적으로는 하나의 독립 데몬
- 여러 서비스들을 제어하고 관리
- 리눅스 커널 2.4 버전부터 보안상의 이유로 `xinetd`가 inetd 역할을 수행

```text
inetd
→ 여러 서비스 데몬 관리
→ Super Daemon
```

---

## 4. inetd 타입 데몬

inetd 타입 데몬은 직접 서비스를 가동하지 못하고  
`inetd` 데몬이 활성화되어 있어야 서비스를 제공한다.

관련 서비스:

```text
Telnet
FTP
rlogin
```

- 서비스 요청이 종료되면 inetd 타입 데몬도 자동 종료
- 실행 스크립트 위치:

```text
/etc/xinetd.d/
```

---

## 핵심 비교

| 구분 | standalone | inetd 타입 |
|---|---|---|
| 실행 방식 | 항상 메모리에 상주 | 요청 시 서비스 실행 |
| 응답 속도 | 빠름 | 상대적으로 느림 |
| 메모리 사용 | 큼 | 상대적으로 적음 |
| 예 | http, mysql, nameserver, sendmail | Telnet, FTP, rlogin |

```text
standalone = 항상 상주
inetd = 여러 데몬을 관리하는 슈퍼 데몬
inetd 타입 = 요청 시 서비스 제공
```
