# DAY 04

## -- Python --

### ▷ 파이썬 함수

- 함수 

  - 특정 입력 값을 주었을 때, 이를 사용하여 어떠한 일을 수행하고 난 다음의 결과를 반환하는 역할을 수행하는 것
  - 선언 방식

  ~~~
  def 함수명(매개변수):
  	<수행할 문장1>
  	<수행할 문장2>
  	...
  	return OOO
  ~~~

  - main 함수
    - 프로그램 시작 시 가장 먼저 호출되는 함수

  ~~~
  # -*- coding:utf-8 -*-
  # 파이썬 인코딩 설정 방식
  
  if __name__ == "__main__":
  	<수행할 문장1>
  	<수행할 문장2>
  ~~~

  - 일반적인 함수

  ~~~
  def add(a, b):
  	...
  	return a + b
  
  print(add(1, 5))
  print(add(a=3, b=6))
  print(add(b=7, a=3))
  ~~~

  - 입력값이 없는 함수

  ~~~
  def sayHi( ):
  	...
  	return ‘Hi’
  
  print( sayHi() )
  ~~~

  - 결과값이 없는 함수

  ~~~
  def add(a, b):
  	print(“합 : %d" % (a+b))
  
  add(10, 15)
  add( a = 10, b = 15 )
  add( b= 15, a = 10 )
  ~~~

  - 입력값도 결과값도 없는 함수

  ~~~
  def sayHi( ):
  	print(‘Hi’)
  
  sayHi()
  ~~~

  - 매개변수가 불확실한 함수

  ~~~
  def 함수이름(*매개변수):
  	for i in 매개변수명 :
  		  <수행할 내용>
  	return
  
  함수이름(1, 2, 3, 4, 5)
  함수이름(1, 2, 3)
  ~~~

  - 결과값이 2개인 함수

  ~~~
  def add_result(a, b):
  	return a, a + b
  
  add_result(1, 2) # 결과는 튜플의 형태로 나온다
  ~~~

  - 람다
    - 함수를 생성할 때 사용하는 예약어로 def와 동일한 역할로, def를 사용할 정도로 복잡하지 않거나, def를 사용할 수 없는 곳에서 쓰임

  ~~~
  # lambda 매개변수1, 매개변수2, ... : 매개변수를 이용한 표현식
  
  add = lambda a, b: a+b
  result = add(3, 4)
  print(result) 			# 결과는 7이 나온다.
  ~~~



### ▷ 파이썬 모듈

- 모듈

  - 함수나 변수 또는 클래스를 모아 놓은 파일 (자바의 import와 동일)
  - mod01.py

  ~~~
  def add(a, b):
  	return a+b
  
  def minus(a, b) :
  	return a-b
  ~~~

  - mod02.py

  ~~~
  import mod01  
  
  print( mod01.add( a + b ) )
  print( mod01.minus( a + b ) )
  ~~~

  

- 사용법

  - import 모듈이름 [ as 별칭 ] 
    - import는 현재 디렉터리에 있는 파일이나 파이썬이 설치된 곳의 라이브러리가 저장된 디렉터리에 있는 모듈만 불러올 수 있다.
  - from 모듈이름 import 함수명 ( 모듈 이름 생략 가능 )

  ~~~
  import mod01
  
  print( mod01.add( a, b ) )
  
  -------------------------
  
  from mod01 import add
  
  print( add( a, b ) )
  ~~~



- 파이썬 대표적인 기본 모듈	
  - 참조 - https://docs.python.org/ko/3/library/index.html 
  - re - 정규 표현식 관련 모듈
  - datetime - 기본 날짜와 시간을 표현하는 모듈
  - math - 수학적 계산과 관련된 모듈
  - random - 임의의 난수를 생성하는 모듈
  - json -  JSON 처리를 돕는 모듈
  - pickle - 파이썬 객체를 직렬화처리하는 모듈
  - sys - 인터프리터 설정과 관련된 모듈
  
  

### ▷ 파이썬 데이터 시각화

- 한눈에 볼 수 없는 많은 양의 데이터를 한 번에 볼 수 있도록 함
- 데이터의 변화, 현황 등을 요약해 보다 쉽게 파악하여 데이터의 분석 결과를 확인할 수 있도록 돕는 것



- 데이터 시각화와 관련된 외부 모듈
  - numpy - 고성능의 수치계산을 지원하는 모듈
  - matplotlib - 주어진 데이터를 시각화하는 가장 기본적인 모듈
  - seaborn matplotlib - 기반으로 보다 다양한 라이브러리를 지원
  - plotnine - R의 ggplot2 모듈에 기반한 그래프를 표현하는 모듈
  - folium - 지도 데이터를 시각화하는 모듈
- numpy 모듈
  - 현실 세계의 다차원 배열을 효과적으로 처리할 수 있도록 해주는 고성능 과학 계산용 패키지 모듈
- 특징
  - 일반 List에 비해 계산이 빠르고, 메모리를 효율적으로 사용한다.
  - 반복문 없이 데이터 배열에 대한 처리를 지원하여 빠르고 편리하다.
  - 선형대수와 관련된 다양한 기능을 제공한다.
  - C, C++, 등의 언어와 통합이 가능하다.

~~~
import numpy as np

np_array = np.array([1.5, True, 5, '8'], dtype=np.float)
print(np_array) 	# dtype : 지정한 타입으로 바꿔줌

np_array2 = np.arange(15).reshape(3, 5)
print(np_array2) 	# dtype : 5 * 3 배열 형태로 객체 생성
~~~

- numpy 주요 함수

  - sum() - 배열의 모든 요소의 합 
  - min() - 모든 요소 중 최소값
  - max() - 모든 요소 중 최대값 
  - argmax() - 모든 요소 중 최대값의 위치
  - ravel() - 해당 배열을 1차원의 배열로 변환 
  - T() - 해당 배열을 전치시킴

- matplotlib 모듈

  - 가장 대표적인 데이터 시각화 모듈로, 배열 형태의 데이터로 기본적인 그래프를 그릴 수 있는 함수들을 제공함

  ~~~
  import matplotlib.pyplot as plt
  
  plt.plot([1, 2, 3, 4])
  
  plt.ylabel(‘y-Label')
  
  plt.show()
  ~~~

  
