---
layout: post
title:  "밑바닥부터 시작하는 딥러닝3 - STEP 1"
date:   2020-12-15 19:58:15
author: Hoon
categories: 딥러닝
---

### 변수

-------

변수는 가장 기본적인 요소이고 밑의 상자 그림을 통해 직관적으로 바라볼 수 있다.

![프로그래밍에서 변수(variable)란? 자료형이란? 데이터 타입 종류 및 크기](https://t1.daumcdn.net/cfile/tistory/993671415C62E8F11D)

여기서 15와 10은 data에 해당되고 eggs와 fizz가 변수에 해당됩니다. 

* 상자와 데이터는 별개다.
* 상자에는 데이터가 들어간다(대입 혹은 할당한다).
* 상자 속을 들여다보면 데이터를 알 수 있다(참조한다).



### Variable 클래스 구현

------

파이썬을 이용하여 변수를 Variable이라는 이름의 클래스로 구현.

```python
class Variable:
    def __init__(self, data):
        self.data = data
```

초기화 함수 `__init__` 에 주어진 인수를 인스턴스 변수 `data`에 대입하여 Variable 클래스를 상자처럼 사용할 수 있게 되었다.

```python
import numpy as np

data = np.array(1.0)
x = Variable(data)
print(x.data)
```

실행 결과

```python
1.0
```

위의 코드에서 `x`는 Variable 인스턴스이고 실제 데이터는 `x`안에 존재한다.



### 넘파이의 다차원 배열

-----

다차원 배열은 숫자 등의 원소가 일정하게 모여 있는 데이터 구조이다. 0차원 배열은 스칼라(scalar), 1차원 배열은 벡터(vector), 2차원 배열은 행렬(matrix)라고 한다.

```python
import numpy as np
x = np.array(1)
print("x의 차원:", x.ndim)

y = np.array([1,2,3])
print("y의 차원:", y.ndim)

z = np.array([[1,2,3],
              [4,5,6]])
print("z의 차원:", z.ndim)
```

실행 결과

```python
x의 차원: 0
y의 차원: 1
z의 차원: 2
```

`ndim`은 number of dimesions의 약자로 다차원 배열의 차원수를 리턴해주는 인스턴스이다.



**출처:\- 사이토 고키, **『**밑바닥부터 시작하는 딥러닝3**』, 개앞맵시, 한빛미디어(2020)

