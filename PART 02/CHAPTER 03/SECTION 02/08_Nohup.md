# Job Control - nohup

## 1. nohup

`nohup`은 **프로세스가 중단되지 않고 백그라운드로 작업을 계속 수행할 수 있도록 하는 명령어**이다.

사용자가 로그아웃하거나 작업 중인 터미널 창이 닫혀도 실행 중인 프로세스를 계속 작업할 수 있게 한다.

```text
nohup
→ 로그아웃 후에도 계속 실행
→ 터미널이 닫혀도 계속 실행
```

---

## 2. 백그라운드 실행

백그라운드로 실행하려면 명령어 뒤에 `&`를 붙인다.

예:

```bash
nohup tar cvf source.tar /opt/src &
```

```text
nohup → 터미널 종료 후에도 계속 실행
&     → 백그라운드 실행
```

---

## 3. 출력 파일

실행 중인 프로세스의 표준 출력 결과는 기본적으로 다음 파일에 기록된다.

```text
nohup.out
```

예:

```bash
nohup echo Welcome to Youngjin
```

출력 확인:

```bash
cat nohup.out
```

---

## 4. 작업 디렉토리에 쓰기가 불가능한 경우

현재 작업 디렉토리에 쓰기가 불가능하면 다음 파일을 자동으로 생성하여 기록한다.

```text
$HOME/nohup.out
```

---

# 핵심 정리

```text
nohup
→ 로그아웃/터미널 종료 후에도 프로세스 계속 실행
```

```text
nohup 명령어 &
→ 백그라운드로 계속 실행
```

```text
기본 출력 파일
→ nohup.out

현재 작업 디렉토리에 쓰기 불가
→ $HOME/nohup.out
```
