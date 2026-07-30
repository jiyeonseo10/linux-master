# Ping

## Overview

`ping` is a network utility used to test connectivity between two hosts.

It sends ICMP Echo Request packets and waits for Echo Reply packets.

---

## 1. Test Network Connectivity

```bash
ping mirror.nsc.liu.se
```

**Description**

Repository 서버(`mirror.nsc.liu.se`)와 네트워크 연결이 정상인지 확인한다.

**Notes**

- 서버가 응답하면 네트워크 연결이 정상이다.
- 응답이 없으면 네트워크 또는 서버 상태를 확인해야 한다.

---

## Example Output

```text
PING mirror.nsc.liu.se (130.xxx.xxx.xxx): 56 data bytes
64 bytes from 130.xxx.xxx.xxx: icmp_seq=1 ttl=52 time=220 ms
```

---

## Common Options

| Option | Description |
|--------|-------------|
| `-c` | 지정한 횟수만큼 Ping 전송 |
| `-i` | Ping 전송 간격 지정 |
| `-s` | 패킷 크기 지정 |

---

## Notes

- `ping`은 ICMP(Internet Control Message Protocol)를 사용한다.
- 네트워크 연결 상태를 가장 간단하게 확인할 수 있는 명령어이다.
- Repository 서버나 다른 서버의 연결 여부를 확인할 때 자주 사용한다.
