# Job Scheduling - crond & crontab

## 1. Scheduling

스케줄링(Scheduling)은 **주기적으로 반복되는 작업을 자동으로 실행하도록 설정하는 기능**이다.

스케줄링을 담당하는 데몬은 `crond`이다.

```text
Scheduling
→ 반복 작업 자동 실행

crond
→ 예약된 작업을 주기적으로 수행하는 데몬
```

---

## 2. /etc/crontab

`crond`의 설정 파일은 다음과 같다.

```text
/etc/crontab
```

시스템 전체에 공통으로 적용되는 작업을 정의한다.

`/etc/crontab`은 7개의 필드로 구성된다.

```text
분 / 시 / 날 / 달 / 요일 / 사용자 / 명령어
```

---

## 3. cron 관련 디렉토리

```text
/etc/cron.hourly/   → 시간별 작업
/etc/cron.daily/    → 일별 작업
/etc/cron.weekly/   → 주별 작업
/etc/cron.monthly/  → 월별 작업
```

---

## 4. 사용자 스케줄링 - crontab

사용자는 `crontab` 명령어를 통해 자신의 주기적인 작업을 등록하고 관리할 수 있다.

형식:

```bash
crontab [옵션] 파일명
```

---

## 5. crontab 주요 옵션

| 옵션 | 의미 |
|---|---|
| `-l` | crontab에 설정된 내용 출력 |
| `-e` | crontab 작성 또는 수정 |
| `-r` | crontab 내용 삭제 |
| `-u` | 특정 사용자의 일정 수정 |

### 핵심

```text
-l → 설정 내용 출력
-e → 작성 / 수정
-r → 삭제
-u → 특정 사용자 일정 수정
```

---

## 6. crontab 시간 형식

사용자 crontab의 기본 순서는 다음과 같다.

```text
분 / 시 / 날 / 달 / 요일 / 명령어
```

예:

```bash
* 4 * * 2,4 /etc/backup.sh
```

의미:

```text
분   → *
시   → 4
날   → *
달   → *
요일 → 2,4
명령 → /etc/backup.sh
```

따라서:

```text
매주 화요일과 목요일 오전 4시에
/etc/backup.sh 실행
```

---

# 핵심 정리

```text
Scheduling
→ 주기적 반복 작업 자동 실행

crond
→ 스케줄링 데몬

/etc/crontab
→ 시스템 전체 공통 작업 설정
```

```text
/etc/crontab 필드

분 / 시 / 날 / 달 / 요일 / 사용자 / 명령어
```

```text
crontab -l → 설정 내용 출력
crontab -e → 작성 / 수정
crontab -r → 삭제
crontab -u → 특정 사용자 일정 수정
```

```text
/etc/cron.hourly/   → 시간별
/etc/cron.daily/    → 일별
/etc/cron.weekly/   → 주별
/etc/cron.monthly/  → 월별
```

```text
* 4 * * 2,4 /etc/backup.sh
→ 매주 화요일과 목요일 오전 4시 실행
```
