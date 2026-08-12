# Special Permissions

리눅스의 특수 권한에는 **SetUID, SetGID, Sticky Bit**가 있다.

## 1. SetUID

실행 파일에 설정하면 해당 파일을 실행할 때 **파일 소유자(owner)의 권한으로 실행**된다.

### 설정

```bash
chmod u+s file
chmod 4755 file
```

- 숫자 값: `4`
- 표시 위치: user의 `x` 자리

```text
rwsr-xr-x
  ↑
```

- `s`: SetUID + 실행 권한(x) 있음
- `S`: SetUID 설정, 실행 권한(x) 없음

---

## 2. SetGID

실행 파일에 설정하면 **파일 소유 그룹(group)의 권한으로 실행**된다.

```bash
chmod g+s file
chmod 2755 file
```

- 숫자 값: `2`
- 표시 위치: group의 `x` 자리

```text
rwxr-sr-x
     ↑
```

- `s`: SetGID + 실행 권한(x) 있음
- `S`: SetGID 설정, 실행 권한(x) 없음

### 디렉터리에 설정한 경우

SetGID가 설정된 디렉토리 안에서 새 파일이나 디렉토리를 생성하면 **상위 디렉토리의 그룹을 상속**받는다.

---

## 3. Sticky Bit

주로 **공용 디렉토리**에 설정한다.

여러 사용자가 파일을 생성할 수 있어도 다른 사용자의 파일을 임의로 삭제하지 못하도록 제한한다.

대표적인 디렉토리:

```bash
/tmp
```

### 설정

```bash
chmod o+t directory
chmod 1777 directory
```

- 숫자 값: `1`
- 표시 위치: others의 `x` 자리

```text
rwxrwxrwt
        ↑
```

- `t`: Sticky Bit + 실행 권한(x) 있음
- `T`: Sticky Bit 설정, 실행 권한(x) 없음

---

## 핵심 정리

| 특수 권한 | 숫자 | 위치 | 의미 |
|---|---:|---|---|
| SetUID | `4` | user | 파일 소유자 권한으로 실행 |
| SetGID | `2` | group | 파일 소유 그룹 권한으로 실행 |
| Sticky Bit | `1` | others | 공용 디렉토리의 파일 삭제 제한 |

```text
4 → SetUID
2 → SetGID
1 → Sticky Bit
```

예:

```bash
chmod 4755 file    # SetUID
chmod 2755 file    # SetGID
chmod 1777 dir     # Sticky Bit
chmod 6755 file    # SetUID + SetGID
```
