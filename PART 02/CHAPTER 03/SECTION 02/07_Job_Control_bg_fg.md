# Job Control - bg & fg

## 1. bg

`bg`는 현재 실행 중인 작업을 **백그라운드 작업으로 전환**하는 명령어이다.

형식:

```bash
bg %작업번호
```

또는

```bash
bg 작업번호
```

포어그라운드에서 실행 중인 작업을 백그라운드로 전환하려면 먼저:

```text
Ctrl + Z
```

를 입력하여 작업을 일시 중지한 후 `bg`를 실행한다.

```text
Foreground
→ Ctrl + Z
→ 일시 중지
→ bg
→ Background
```

---

## 2. 처음부터 백그라운드로 실행

명령어 뒤에 `&`를 붙이면 처음부터 백그라운드로 실행된다.

예:

```bash
find / -name 'txt' > /txt.list &
```

```text
명령어 &
→ 처음부터 백그라운드 실행
```

---

## 3. fg

`fg`는 백그라운드에서 실행 중인 작업을 **포어그라운드로 전환**하는 명령어이다.

형식:

```bash
fg %작업번호
```

또는

```bash
fg 작업번호
```

작업번호를 지정하지 않으면 현재 수행 중인 작업을 포어그라운드로 전환한다.

```text
Background
→ fg
→ Foreground
```

---

## 4. 포어그라운드 작업 종료

포어그라운드 작업을 종료하려면:

```text
Ctrl + C
```

를 입력한다.

---

# 핵심 정리

```text
bg
→ Foreground → Background

fg
→ Background → Foreground
```

```text
Ctrl + Z
→ 작업 일시 중지

명령어 &
→ 처음부터 백그라운드 실행

Ctrl + C
→ 포어그라운드 작업 종료
```
