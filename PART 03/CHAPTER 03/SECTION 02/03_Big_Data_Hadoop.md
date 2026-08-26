# Big Data & Hadoop

## 1. 빅데이터(Big Data) 정의

빅데이터는 기존 데이터베이스 관리 도구의  
**데이터 수집, 저장, 관리, 분석 역량을 넘어서는 데이터**이다.

다양한 종류의 대규모 데이터로부터 저렴한 비용으로 가치를 추출하고  
데이터를 빠르게 수집, 발굴, 분석할 수 있도록 지원하는 차세대 기술 및 아키텍처이다.

```text
Big Data
→ 기존 DB 관리 도구의 처리 한계를 넘어서는 데이터
→ 대규모 데이터
→ 가치 추출
→ 빠른 수집 / 발굴 / 분석
```

---

# 빅데이터 3대 요소

## 2. 3V

책에서는 다음 3가지 요소 중 **두 가지 이상의 요소를 충족하면 빅데이터라고 볼 수 있다**고 설명한다.

```text
Volume
Velocity
Variety
```

---

## 3. Volume

`Volume = 규모`

수십 테라바이트(Terabyte) 또는  
수십 페타바이트(Petabyte) 이상의 데이터가 빅데이터의 범위에 해당한다.

```text
Volume
→ 데이터의 규모
→ 수십 TB 또는 수십 PB 이상
```

### 핵심

```text
Volume = 양 / 규모
```

---

## 4. Velocity

`Velocity = 속도`

빅데이터의 속도적 특징은 크게 다음과 같이 나눌 수 있다.

```text
실시간 처리
장기적인 접근
```

데이터의 수집, 저장, 분석 등이 실시간으로 처리되어야 할 수 있다.

하지만 모든 데이터가 실시간 처리만을 요구하는 것은 아니다.

수집된 대량의 데이터를 다양한 분석 기법과 표현 기술을 이용하여  
장기적이고 전략적으로 분석하는 것도 필요하다.

책에 나온 분석 기법:

```text
데이터 마이닝
기계 학습
자연어 처리
패턴 인식
```

### 핵심

```text
Velocity
→ 데이터 처리 속도
→ 실시간 처리
→ 장기적 분석
```

---

## 5. Variety

`Variety = 다양성`

데이터는 정형화 정도에 따라 다음과 같이 구분한다.

```text
정형(Structured)
반정형(Semi-Structured)
비정형(Unstructured)
```

---

## 6. 정형 데이터

고정된 필드에 저장되며 일정한 형식을 갖는 데이터이다.

```text
Structured
→ 고정된 필드
→ 일정한 형식
```

---

## 7. 반정형 데이터

고정된 필드에 저장되지는 않지만  
메타데이터나 스키마 등을 포함하는 데이터이다.

책에 나온 예:

```text
XML
HTML
```

### 핵심

```text
Semi-Structured
→ 반정형
→ XML / HTML
→ 메타데이터 / 스키마 포함
```

---

## 8. 비정형 데이터

고정된 필드에 저장되지 않는 데이터이다.

책에 나온 예:

```text
사진
동영상
메신저로 주고받은 대화 내용
스마트폰에 기록되는 위치 정보
통화 내용
```

빅데이터는 이러한 비정형 데이터도 처리할 수 있어야 한다.

### 핵심

```text
Unstructured
→ 비정형
→ 사진 / 동영상 / 메신저 / 위치정보 / 통화내용
```

---

# Hadoop

## 9. Hadoop 정의

Hadoop은 **대용량 데이터를 분산 처리할 수 있는 자바 기반의 오픈 소스 프레임워크**이다.

```text
Hadoop
→ Java 기반
→ Open Source
→ 대용량 데이터 분산 처리
```

---

## 10. HDFS

Hadoop은 분산 파일 시스템인 `HDFS`에 데이터를 저장한다.

`HDFS`는 다음의 약자이다.

```text
Hadoop Distributed File System
```

### 핵심

```text
HDFS
→ 분산 파일 시스템
→ 데이터 저장
```

---

## 11. MapReduce

분산 처리 시스템에서는 `MapReduce`를 이용하여 데이터를 처리한다.

```text
Hadoop
→ HDFS에 데이터 저장
→ MapReduce로 데이터 처리
```

### 핵심

```text
HDFS = 저장
MapReduce = 처리
```

---

# Hadoop 특징

## 12. 오픈 소스

Hadoop은 오픈 소스 프로젝트이므로 소프트웨어 라이선스 비용에 대한 부담이 없다.

```text
Open Source
→ 라이선스 비용 부담 없음
```

---

## 13. x86 Linux 서버 사용

값비싼 UNIX 장비를 사용하지 않고  
x86 CPU의 Linux 서버 여러 대를 이용하여 설치하고 운영할 수 있다.

```text
비싼 UNIX 장비 X
→ x86 CPU
→ Linux 서버 여러 대 사용
```

---

## 14. 확장성

데이터 저장 용량이 부족한 경우 필요한 만큼 Linux 서버를 추가하면 된다.

```text
저장 용량 부족
→ Linux 서버 추가
→ 확장 가능
```

---

## 15. 데이터 복구

Hadoop은 데이터의 복제본을 저장한다.

따라서 데이터 유실이나 장애가 발생해도 데이터를 복구할 수 있다.

```text
데이터 복제본 저장
→ 장애 / 유실 발생
→ 복구 가능
```

---

## 16. 분산 처리

여러 대의 서버에 데이터를 저장하고  
각 서버에서 동시에 데이터를 처리하는 방식이다.

```text
여러 서버
→ 데이터 분산 저장
→ 동시에 데이터 처리
```

---

# 핵심 정리

```text
Big Data 3V

Volume
→ 규모

Velocity
→ 속도

Variety
→ 다양성
```

```text
Structured
→ 정형
→ 고정된 필드

Semi-Structured
→ 반정형
→ XML / HTML

Unstructured
→ 비정형
→ 사진 / 동영상 / 메신저 / 위치정보 / 통화내용
```

```text
Hadoop
→ Java 기반
→ Open Source
→ 대용량 데이터 분산 처리
```

```text
HDFS
→ 저장

MapReduce
→ 처리
```

```text
Hadoop 특징
→ 라이선스 비용 부담 없음
→ x86 Linux 서버 사용
→ 서버 추가로 용량 확장
→ 복제본으로 데이터 복구
→ 여러 서버에서 동시 처리
```

---

# 시험 직전 암기

```text
3V

Volume = 규모
Velocity = 속도
Variety = 다양성
```

```text
반정형
→ XML / HTML
```

```text
Hadoop
→ Java
→ Open Source
→ Distributed Processing
```

```text
HDFS = 분산 저장
MapReduce = 분산 처리
```
