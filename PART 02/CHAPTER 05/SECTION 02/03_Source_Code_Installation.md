# Source Code Installation

## 1. 소스 코드의 개념

소스 코드는 **고급 언어로 작성된 프로그램**이다.

책에서는 리눅스의 소스 코드가 대부분 **C 언어**로 작성된다고 설명한다.

소스 코드는 바로 실행하는 것이 아니라 **컴파일** 과정을 거쳐야 한다.

```text
소스 코드
→ 고급 언어로 작성

컴파일
→ 고급 언어를 기계어로 변환
```

---

## 2. 소스 코드 설치 순서

소스 코드는 다음 순서로 설치한다.

```text
./configure
→ make
→ make install
```

즉,

```text
환경 설정
→ 컴파일
→ 파일 설치
```

---

## 3. 1단계: ./configure

```bash
./configure
```

프로그램 설치 과정에서 필요한 환경 파일인 `makefile`을 생성한다.

주요 기능:

- 시스템 파일 위치 지정
- 설치 파일 위치 지정
- `configure` 뒤에 옵션 지정 가능

```text
./configure
→ 환경 설정
→ makefile 생성
```

---

## 4. 2단계: make

```bash
make
```

`makefile`을 기반으로 소스 파일을 컴파일한다.

컴파일된 소스 파일은 실행 파일로 변환된다.

```text
make
→ 컴파일
→ 실행 파일 생성
```

---

## 5. 3단계: make install

```bash
make install
```

컴파일된 실행 파일을 지정된 디렉토리에 설치한다.

```text
make install
→ 컴파일된 실행 파일 설치
```

---

## 6. make && make install

```bash
make && make install
```

책에서는 컴파일과 파일 설치를 이어서 처리할 수 있다고 설명한다.

```text
make
→ 컴파일

make install
→ 설치
```

---

# CMake

## 7. CMake의 개념

CMake는 **Cross Platform Make**이다.

여러 플랫폼에서 사용할 수 있는 Make의 대용품을 만들기 위한 오픈소스 프로젝트이다.

주요 특징:

- Kitware와 Insight Consortium에서 개발
- 운영체제에 맞는 Make 파일 생성
- Meta Make라고도 부름
- 유닉스 계열뿐 아니라 Microsoft Windows 계열 프로그래밍 도구도 지원

```text
CMake
→ Cross Platform Make
→ Meta Make
→ 운영체제에 맞는 Make 파일 생성
```

---

## 8. CMake 주요 특징

책에 나온 주요 특징:

- 소프트웨어 빌드에 특화된 독자적인 설정 스크립트 사용
- C, C++, Java, Fortran 의존 관계 분석 가능
- SWIG, QT 지원
- Microsoft Visual Studio 지원
- Eclipse 빌드 파일 생성 가능
- 타임스탬프로 파일 내용 변화 확인 가능
- 병행 빌드 가능
- 크로스 컴파일 가능
- 다양한 플랫폼 지원

---

# 핵심 정리

```text
소스 코드
→ 고급 언어로 작성
→ 리눅스에서는 대부분 C 언어
→ 컴파일 필요
```

```text
소스 코드 설치 순서

./configure
→ 환경 설정 + makefile 생성

make
→ 컴파일

make install
→ 설치
```

```text
CMake
→ Cross Platform Make
→ Meta Make
→ 운영체제에 맞는 Make 파일 생성
→ 다양한 플랫폼 지원
→ 크로스 컴파일 가능
```

## 시험 직전 암기

```text
configure → 설정
make      → 컴파일
install   → 설치
```

```text
./configure
→ make
→ make install
```

```text
CMake
→ Cross Platform
→ Meta Make
```
