# DAY 02

## -- Python --

### ▷ 파이썬 연산자

- 산술 연산자 
  - 사칙 연산자: +, -, *, /, %
  - 제곱 연산자 : **
  - 소수점 이하를 버리는 연산자 : //
- 비교 연산자 (= 관계 연산자)
  - 같음(==), 같지 않음(!=), 부등호(<, >, <=, >=)
- 논리 연산자
  - 양쪽 모두 참(and), 둘 중 한쪽만 참(or), 반대 논리 연산자(not)
- Identity 연산자
  - 동일한 객체인지 비교하는 연산자 ( is / is not )

- 범위 연산자

  - 특정 범위를 자르는 연산자
  - [start:end] : start ~ end – 1
    [start: end:step] : start ~ end - 1 까지 step만큼씩 증가

  ~~~
  ex)
  str='Hello World!'
  
  print(str[0:5]) # 0 ~ 4 번째 문자 모두 추출
  print(str[3:10:3]) # 3, 6, 9 번째 문자 각각 추출
  ~~~

    - 범위 연산자(reverse)
      - -1, 즉 음수로 하면 역순으로 실행함
  
  ~~~
  ex)
  #[start:end] : start ~ end – 1
  print(str[-1])
  print(str[-1:])
  print(str[:-1])
  print(str[::-1])
  ~~~

- 멤버 연산자

  - 좌측 항의 객체가 우측의 객체에 들어 있는 지 확인 (in / not in )

  ~~~
  list=[0,1,2,3,4,5]
  print(3 in list)
  print(5 not in list)
  print(6 not in list)
  ~~~

- 문자열 관련 함수

  - split

  ~~~
  str1 = 'Hello, world!\nHello, python!'
  arr1 = str1.split(' ')
  print(arr1)
  ~~~

  - join

  ~~~
  arr2 = ['1', '2', '3', '4']
  print('+'.join(arr2))
  ~~~

- 정규표현식(Regular Expression)

  - 주어진 문자열에서 찾고자 하는 특정 문자열을 탐색하는 형식언어
  - 자바스크립트의 정규표현식과 유사함

  ~~~
  import re
  str = ‘700905-1059119'
  match = re.search(r'[\w.-]+@[\w.-]+', str)
  print(match.group())
  ~~~

  
