# X Remote Access

## 1. xhost

`xhost`는 **X 서버에 접속할 수 있는 클라이언트를 지정하거나 해제하는 명령어**이다.

X 서버에 디스플레이를 요청할 때 해당 요청의 허용 여부를 **호스트 단위로 제어**한다.

형식:

```bash
xhost [+|-] [IP|도메인명]
```

### 주요 사용법

```text
xhost +
→ X 서버에 모든 클라이언트 접속 허용

xhost -
→ X 서버에 모든 클라이언트 접속 금지

xhost + IP주소
→ 해당 IP 주소를 가진 호스트 접속 허용

xhost - IP주소
→ 해당 IP 주소를 가진 호스트 접속 금지
```

### 핵심 암기

```text
+ → 허용
- → 금지

xhost
→ 호스트 기반 인증
```

---

## 2. DISPLAY 환경 변수

`DISPLAY` 환경 변수는 **X 서버 프로그램이 실행될 때 표시되는 클라이언트 주소를 지정**한다.

```text
DISPLAY
→ X-윈도우의 Display 위치 지정
```

형식:

```bash
export DISPLAY=IP주소:디스플레이번호.스크린번호
```

---

## 3. xauth

`xauth`는 **.Xauthority 파일의 쿠키 내용을 관리하는 유틸리티**이다.

주요 기능:

```text
쿠키 추가
쿠키 삭제
쿠키 목록 출력
```

`xhost`가 호스트 기반 인증을 사용하는 것과 달리  
`xauth`는 **키(쿠키)를 이용한 인증 방식**을 사용한다.

### 핵심 비교

```text
xhost
→ 호스트 기반 인증

xauth
→ 쿠키(키) 기반 인증
```

---

## 4. .Xauthority

사용자 인증에 사용되는 파일:

```text
$HOME/.Xauthority
```

사용자는 해당 파일에 대한 읽기 및 쓰기 권한이 있어야 한다.

`.Xauthority` 파일에는 표시장치 인증을 위한  
**매직 쿠키(Magic Cookie)**가 존재한다.

책에 나온 쿠키 값:

```text
MIT-MAGIC-COOKIE-1
```

### 핵심

```text
$HOME/.Xauthority
→ 인증 쿠키 저장

MIT-MAGIC-COOKIE-1
→ 매직 쿠키
```

---

## 5. xauth list

```bash
xauth list
```

기능:

```text
현재 사용되는 쿠키 값 목록 확인
지정된 표시장치의 쿠키 값 확인
```

---

# 핵심 정리

```text
xhost
→ 호스트 기반 인증

xauth
→ 쿠키 기반 인증
→ .Xauthority 관리
```

```text
xhost +
→ 모두 허용

xhost -
→ 모두 금지

xhost + IP
→ 특정 호스트 허용

xhost - IP
→ 특정 호스트 금지
```

```text
.Xauthority
→ $HOME/.Xauthority

Magic Cookie
→ MIT-MAGIC-COOKIE-1
```

```text
xauth list
→ 쿠키 목록 확인
```

## 시험 직전 암기

```text
xhost = Host
xauth = Authority Cookie

+ = 허용
- = 금지

.Xauthority
→ MIT-MAGIC-COOKIE-1
```
