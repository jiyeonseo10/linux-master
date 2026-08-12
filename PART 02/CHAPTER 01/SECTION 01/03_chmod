# chmod

`chmod`는 **change mode**의 약자로, 파일이나 디렉터리의 접근 권한(permission)을 변경하는 명령어이다.

## 1. 파일 유형과 권한 확인

```bash
ls -l
```

예시:

```text
-rwxr-xr--
```

첫 번째 문자는 **파일 유형**, 이후 9자리는 **접근 권한**을 나타낸다.

```text
- | rwx | r-x | r--
↑    ↑     ↑     ↑
유형 소유자  그룹  기타 사용자
     (u)   (g)    (o)
```

### 파일 유형

| 문자 | 파일 유형 | 의미 |
|---|---|---|
| `-` | Regular File | 일반 파일 |
| `d` | Directory | 디렉토리 |
| `b` | Block Device | 블록 단위로 처리하는 장치 파일 |
| `c` | Character Device | 문자(바이트) 단위로 처리하는 장치 파일 |
| `l` | Symbolic Link | 심볼릭 링크 |
| `p` | Named Pipe | 프로세스 간 통신에 사용하는 파이프 |
| `s` | Socket | 프로세스 간 통신에 사용하는 소켓 |

## 2. 접근 권한

| 권한 | 의미 | 숫자 |
|---|---|---:|
| `r` | Read (읽기) | 4 |
| `w` | Write (쓰기) | 2 |
| `x` | Execute (실행) | 1 |

## 3. 숫자 방식

```bash
chmod 755 file
```

각 숫자는 다음 사용자의 권한을 의미한다.

```text
7   5   5
↓   ↓   ↓
u   g   o
```

- `7` = 4 + 2 + 1 = `rwx`
- `5` = 4 + 1 = `r-x`
- `5` = 4 + 1 = `r-x`

따라서:

```text
755 = rwxr-xr-x
```

자주 보는 예:

```text
644 = rw-r--r--
755 = rwxr-xr-x
777 = rwxrwxrwx
```

## 4. 기호 방식

```bash
chmod u+x file
chmod g-w file
chmod o+r file
```

### 사용자 구분

- `u`: user (소유자)
- `g`: group
- `o`: others (기타 사용자)
- `a`: all (모든 사용자)

### 권한 변경

- `+`: 권한 추가
- `-`: 권한 제거
- `=`: 권한 지정

예:

```bash
chmod u+x file
```

소유자에게 실행 권한을 추가한다.

```bash
chmod g-w file
```

그룹의 쓰기 권한을 제거한다.

## 핵심 정리

- `chmod`: 파일/디렉토리의 접근 권한 변경
- `r = 4`, `w = 2`, `x = 1`
- 권한 순서: `user → group → others`
- `755 = rwxr-xr-x`
- `644 = rw-r--r--`
- `777 = rwxrwxrwx`
