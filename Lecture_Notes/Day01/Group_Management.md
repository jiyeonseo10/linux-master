# Group Management

## 1. Create a Group

```bash
groupadd example
```

**Description**

새로운 그룹 `example`을 생성한다.

**Notes**

- `groupadd`: 새로운 그룹 생성
- 그룹 정보는 `/etc/group` 파일에 저장된다.

---

## 2. Change Group Ownership

```bash
chgrp -R example ~user01
```

**Description**

`user01`의 홈 디렉토리와 하위 파일의 그룹 소유자를 `example`으로 변경한다.

**Notes**

- `chgrp`: 그룹 소유자 변경
- `-R`: 하위 디렉터리까지 재귀적으로 적용
- `~user01`: user01의 홈 디렉토리

---

## 3. Verify the Result

```bash
ls -la /home
```

**Description**

홈 디렉토리의 그룹 변경 결과를 확인한다.

---

## 4. Create an Existing Group

```bash
groupadd user01
```

**Description**

이미 존재하는 그룹을 생성하려고 하면 오류가 발생한다.

**Output**

```text
groupadd: group 'user01' already exists
```

---

## 5. Restore Group Ownership

```bash
chgrp -R user01 ~user01
```

**Description**

`user01` 홈 디렉토리의 그룹 소유자를 원래 그룹으로 변경한다.
