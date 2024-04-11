---
title: Python
layout: upj_design
permalink: /resource/python/
---

#### Table Of Contents

- TOC
{:toc}

## 기초 문법
{: #upj_1681813114384}

### 자료형
{: #upj_1678580221202}

- [List, Set, Dict 복잡도](https://ics.uci.edu/~pattis/ICS-33/lectures/complexitypython.txt)

```python
# 자료형 체크 
if type(n) is not int:
  is_validated = False
```

### 입출력
{: #upj_1678585647623}

```python
# 정수 2개 입력받기
n, m = map(int, input().split(' '))
# 포메팅
print(f'{a:3d} {b:.6f}')
```

### 제어문
{: #upj_1678585717123}

```python
```
### 파일 읽고 쓰기
{: #upj_1678585567762}

```python
```

### 함수
{: #upj_1678585620407}

```python
```

### 클래스
{: #upj_1679789498515}

```python
```

<!--
{: #upj_1681813148708}
{: #upj_1678585744512}
{: #upj_1678585740155}
{: #upj_1678585735668}
{: #upj_1678585731028}
### 리스트
### 튜플
### 딕셔너리
{: #upj_1678585726814}
{: #upj_1678585721556}
{: #upj_1678585712852}
{: #upj_1678585707459}
{: #upj_1678585653130}
{: #upj_1678585577989}
{: #upj_1679789507715}

### 모듈
{: #upj_1679789512665}

### 예외처리
{: #upj_1679789520367}

### 라이브러리
{: #upj_1679789525288}
-->

## 활용: 증권데이터분석
{: #upj_1679789531651}

```text
팬더스를 활용한 데이터 분석
웹 스크래이핑을 사용한 데이터 분석
시세 DB 구축 및 시세 조회 API 개발
트레이딩 전략과 구현
장고 웹 서버 구축 및 자동화
변동성 돌파 전략과 자동매매
딥러닝을 이용한 주가 예측

!pip install yfinance
!pip install pandas-datareader
```

**참고**
- [Github](https://github.com/Investar/StockAnalysisInPython)
  [(소스코드)](https://github1s.com/Investar/StockAnalysisInPython)

### Numpy + Pandas 데이터 분석
{: #upj_1679791272311}

```python
import numpy as np
A = np.array([[1, 2], [3, 4]])
print(A)
print(A.max(), A.min(), A.mean(), A.sum())
print(A[0], A[1])
```


