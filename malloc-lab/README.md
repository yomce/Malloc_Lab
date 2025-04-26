#####################################################################
# CS:APP Malloc Lab
# Handout files for students
#
# Copyright (c) 2002, R. Bryant and D. O'Hallaron, All rights reserved.
# May not be used, modified, or copied without permission.
#
######################################################################

***********
Main Files:
***********

mm.{c,h}	
	Your solution malloc package. mm.c is the file that you
	will be handing in, and is the only file you should modify.

mdriver.c	
	The malloc driver that tests your mm.c file

short{1,2}-bal.rep
	Two tiny tracefiles to help you get started. 

Makefile	
	Builds the driver

**********************************
Other support files for the driver
**********************************

config.h	Configures the malloc lab driver
fsecs.{c,h}	Wrapper function for the different timer packages
clock.{c,h}	Routines for accessing the Pentium and Alpha cycle counters
fcyc.{c,h}	Timer functions based on cycle counters
ftimer.{c,h}	Timer functions based on interval timers and gettimeofday()
memlib.{c,h}	Models the heap and sbrk function

*******************************
Building and running the driver
*******************************
To build the driver, type "make" to the shell.

To run the driver on a tiny test trace:

	unix> mdriver -V -f short1-bal.rep

The -V option prints out helpful tracing and summary information.

To get a list of the driver flags:

	unix> mdriver -h

# CS:APP Malloc Lab

## 과정 설명

- 이후는 **CS:APP Malloc Lab** 학생용 패키지를 설명한 것입니다.
- 저작권은 R. Bryant와 D. O'Hallaron에게 있고, 허가 없이 사용·수정·복제할 수 없습니다.

---

## 포함 파일

### 특히 중요한 파일

- **mm.{c,h}**  
  » 당장 구현할 malloc 패키지.  
  » `mm.c`를 수정하고, 이 파일만 제출합니다.

- **mdriver.c**  
  » 구현한 `mm.c`를 테스트하는 드라이버 파일.

- **short{1,2}-bal.rep**  
  » 시작할 때 사용할 가능성이 있는 트레이스 파일 2개.

- **Makefile**  
  » 빌드(컴파일)를 자동화하는 작업 스크립트.

### 기타 지원 파일

- **config.h**  
  » 드라이버의 환경을 설정.

- **fsecs.{c,h}**  
  » 다양한 타이머 패키지를 다루는 래퍼 함수.

- **clock.{c,h}**  
  » Pentium, Alpha 프로세서의 사이클 카운터 접근 구현.

- **fcyc.{c,h}**  
  » 사이클 카운터 기반 타이머 함수.

- **ftimer.{c,h}**  
  » gettimeofday()를 사용한 시간 측정 함수.

- **memlib.{c,h}**  
  » 가상 힙(heap)을 모델링하고, `sbrk` 함수를 흉내냅니다.

---

## 건설 및 실행 방법

### 빌드 하기

bash
```
make
```

시험 파일들을 자랑적으로 컴파일합니다.

작은 트레이스 파일로 테스트 시작하기
bash
```
mdriver -V -f short1-bal.rep
```

-V : 해당 과정을 자세히 표시해주고, 합계 정보도 나옵니다.

-f : 시작할 트레이스 파일을 지정합니다.

드라이버 옵션 목록 보기
bash
```
mdriver -h
```
쓰일 수 있는 가능한 옵션을 목록으로 보여줍니다.