# Package Management Basics

## 1. 패키지

패키지(Package)는 **각종 프로그램의 설치 파일**이다.

책에서는 패키지가 다음과 같이 구성된다고 설명한다.

```text
인스톨(설치) 파일
+
언인스톨(삭제) 파일
```

즉,

```text
Package
→ 프로그램 설치와 삭제에 필요한 파일 묶음
```

---

## 2. 패키지 관리

패키지 관리는 **패키지를 설치하고 삭제하는 일련의 활동**이다.

```text
Package Management
→ 패키지 설치
→ 패키지 삭제
```

---

## 3. 리눅스에서 소프트웨어 설치 방법

리눅스 시스템에서 소프트웨어를 설치하고 관리하는 방법은 다음과 같다.

```text
1. 배포업체의 패키지를 설치
2. 소스코드를 컴파일하여 설치
```

---

## 4. 리눅스 패키지 계열

일반적으로 리눅스는 다음 두 계열로 구분한다.

```text
데비안 계열
레드햇 계열
```

---

## 5. 데비안 계열

### 배포판

```text
Debian
Ubuntu
Xandros
Linspire
```

### 패키지 도구

```text
dpkg
apt-get
aptitude
```

### 핵심

```text
Debian 계열
→ Debian, Ubuntu, Xandros, Linspire
→ dpkg, apt-get, aptitude
```

---

## 6. 레드햇 계열

### 배포판

```text
Fedora
CentOS
RHEL
openSUSE
mandriva
```

### 패키지 도구

```text
rpm
yum
```

### 핵심

```text
Red Hat 계열
→ Fedora, CentOS, RHEL, openSUSE, mandriva
→ rpm, yum
```

---

# 핵심 비교

```text
데비안 계열
→ Debian / Ubuntu / Xandros / Linspire
→ dpkg / apt-get / aptitude

레드햇 계열
→ Fedora / CentOS / RHEL / openSUSE / mandriva
→ rpm / yum
```

## 시험 직전 암기

```text
Debian → dpkg
Ubuntu → apt-get

Red Hat → rpm
→ yum
```
