# DAY 01

## -- Python --

### ▷ Python | 파이썬

- 구현 코드가 간단하여 배우기 쉬운 동시에 표준 라이브러리를 풍부하게 지원하여 다양한 확장성이 제공되는 언어

- 인터프리터의 특징

  - 프로그램 문장을 하나씩 번역하고 실행
  - 기계어로 번역하는 시간이 빠르나 컴파일 언어에 비해 실행 속도가 느리고 메모리 사용이 비효율적

  - python, javascript, prolog

 **JAVA 는 컴파일러를 통해 바이트 코드로 번역한 후,인터프리터로 한 줄씩 읽는 혼합형 언어**

- 파이썬의 특징
  - 플랫폼 독립적 언어
  - 개발 기간 단축에 초점을 둔 언어
  - 간단하고 쉬운 문법 (Interactive shell : 대화형 언어)
  - 고수준의 내장 객체 자료형 제공



### ▷ Python 기본 문법

- 주석 

  -  # 한줄 주석

  -  ''' 

​					여러줄 주석 ("""도 가능)

​				'''

- 변수 = 값 

  - num1 = 100
  - str1 = 'python is fun'

- 출력

  - print(num1)
  - print('Hello World')

- 자료형

  - 정수형, 실수형, 문자열, 리스트, 튜플, 딕셔너리(자바의  Map)등

  - 자료형 확인 - type()

  - 정수형 

    ~~~
    a =  100
    print(a)
    print(type(a))
    
    #  정수형은 나눗셈 연산(/) 수행 시 실수형으로 바뀜
    ~~~

  - 실수형
  
    ~~~
    b, c = 100.1, 3.14   # 이런 식으로 다중 선언도 가능
    
    print(b)
    print(type(b))
    ~~~

  - 문자열
  
    -  ' , " 차이 없음
  
    ~~~
    a = ‘Hello\nWorld!‘      # \n 은 한 줄 띄어쓰기
    print(a)
    
    b = '''Hello,
    World!''‘
    
    print(b)
    ~~~
  
    

- Print() 함수 상세

  - 계산 결고 출력시 자료형 다르면 출력 X

  - 여러 값 출력시 나열 형태로 출력 가능 (값 사이 공백 자동 추가)

  - end 옵션 -  출력이 끝날 때 끝마침 문자를 바꿀 수 있음(기본값 : 개행(\n))

    ~~~
    print(‘Hello‘, end=‘ ‘)
    print(‘World!!‘) >> Hello World!!
    ~~~

  - sep 옵션 : 출력할 내용을 나열 시 구분자 설정 (기본값 : ‘ ‘)

    ~~~
    print(‘user‘, ‘example.com’, seq=‘@’)
    >> user@example.com
    ~~~

  - % 옵션 : 예전 방식의 형식 지정자로, 자바의 printf와 유사함

    ~~~
    a, b, c = 1, 1, ‘홍길동’
    print( a, ‘학년’, b, ‘반 이름’, c)
    print( ‘%d학년 %d반 이름 %s’%(a, b, c))
    ~~~

  - format 함수 : 예전 방식의 문제점을 해결하여 다양한 출력 형태를 제공

    ~~~
    a, b, c = 1, 1, ‘홍길동’
    print( a, ‘학년’, b, ‘반 이름’, c)
    print( ‘{0}학년 {1}반 이름 {2}’.format(a, b, c)) #0부터 시작
    #순서 미지정 시 format에 명시된 순서대로 들어간다.
    print(‘‘{}학년 {}반 이름 {}’.format(a, b, c))
    ~~~



- 리스트

  - 자바 컬렉션의 List와 유사 (무엇이든 받을 수 있고, 중복 값도 가능)

  - 리스트 선언

    ~~~
    - 생성자를 사용하는 방식
        a = list()
        a.append(10)
        print(a)
    - []를 사용하는 방식
    	b = [ 1, 2, 3 ]
    	print(b)
    ~~~
  
  - 리스트 관련 함수   (a = [1, 3, 2] 라고 가정)
  
    - len( obj ) - 특정 객체의 길이를 구함  ex) print( len(a) )
    - del obj - 특정 객체를 제거 ex) del a[1] / del a[3:]
    - append( obj ) - 리스트에 요소 추가 ex) a.append(4)
    - sort() - 리스트 정렬 ex) a.sort()
    - reverse() - 리스트 순서 뒤집기 ex) a.reverse()
    - index( obj ) - 리스트의 특정 obj의 순번 반환 ex) a.index(3)
    - insert( n, obj ) - 리스트의 n 번째 위치에 obj를 삽입 ex) a.insert( 2, 5 )
    - remove( obj ) - 리스트에서 obj 를 찾아 삭제 ex) a.remove( 3 )
    - pop() - 리스트 마지막 요소를 반환 후 삭제  ex) a.pop()
    - count( obj ) - 리스트 안의 obj 개수 반환  ex) a.count( 1 )
    - extend( list ) - 리스트에 다른 리스트를 추가  ex) a.extend( [5, 6, 7] )



- 튜플

  - list와 유사하나, 선언 방식 및 값의 수정이 안되는 자료형

  - 튜플 선언

    ~~~
    - 생성자를 사용하는 방식
        a = tuple()
        print(a)
    - ( ) 를 사용하는 방식
    	b = ( 1, 2, 3 )
    	print(b)
    ~~~

    

- 리스트 vs 문법

  - 공통점 - 자료형과 상관 없이 모든 객체를 담을 수 있다.

    ​			   두 타입 모두 요소의 순서를 관리한다.

  - 차이점 - 리스트 : 요소 변경 가능 (mutable)

    ​               튜플 : 요소 변경 불가 (immutable)

- 튜플을 사용하는 이유

  - 어떠한 경우에도 변경되어서는 안 되는 불변적 정보를 담을 때 사용한다.
    - 지난 달의 기상 정보, 일주일과 같은 일정한 단위, 예년도 통계 수치
  
- 집합

  - 자바의 Set과 유사한 자료형 ( 요소의 중복 불가, 순서 유지 X )

  ~~~
  - 생성자를 사용하는 방식
  	a = set()
  	print(a)
  - { } 를 사용하는 방식
  	b = { 1, 2, 3 }
  	print(b)
  ~~~

  - 값을 추가 시 연속적인(Iterable) 값을 넣을 경우, 각각을 구분 지어 중복을 제거\
  - 합집합, 교집합, 차집합의 개념이 존재한다.

  ~~~
  eX)
  a = set(‘Hello’)
  print(a)
  결과 : {'l', 'h', 'e', 'o'}	
  ~~~



- 합집합 ( |, union)

  - 두 집합을 합치되 중복되는 값은 한 번만 표현됨

  ~~~
  - | 를 사용하는 방식
  	a = set([1, 2, 4])
      b = set([2, 4, 8])
      print( a | b )
  - union() 을 사용하는 방식
  	a = set([1, 2, 4])
      b = set([2, 4, 8])
      print( a.union(b) )
  
  ~~~

  

- 교집합 ( & , intersection)

  - 두 집합에서 중복되는(공통) 요소만 표현됨

  ~~~
  - & 를 사용하는 방식
  	a = set([1, 2, 4])
      b = set([2, 4, 8])
      print( a & b )
  - intersection() 을 사용하는 방식
      a = set([1, 2, 4])
      b = set([2, 4, 8])
      print( a.intersection(b) )
  ~~~

  

- 차집합 ( - , difference)

  - 앞의 집합에서 뒤의 집합의 공통 요소를 뺀 나머지만 표현됨

  ~~~
  - - 를 사용하는 방식
  	a = set([1, 2, 4])
      b = set([2, 4, 8])
      print( a - b )
  - difference() 을 사용하는 방식
      a = set([1, 2, 4])
      b = set([2, 4, 8])
      print( a.difference(b) )
  ~~~

  

- 집합 관련 함수 
  - add(obj) - 집합에 특정 obj 추가
  - update(obj) -  집합에 여러 obj 추가 
  - remove(obj) - 집합에서 특정obj 제거 

- 딕셔너리

  - 자바의 Map과 유사한 자료형 ( key와 value로 구성된 요소를 저장함 )

  ~~~
  - 생성자를 사용하는 방식
  	a = dict()
      a[‘one’] = ‘Hello’
      print(a)
  - { } 를 사용하는 방식
      b = { 1: ‘월’, 2 : ‘화’ }
      print(b)
  ~~~

- 딕셔너리 각 key의 요소 접근

  - a[ key ] = value / print( a[ key ] )

  ~~~
  keys() :키들만 가져옴
  print(a.keys())
  
  >> dict_keys( [1, 2] )
  
  - values() : 안의 요소들만 가져옴
  print(a.values())
  
  >> dict_values( [‘H’, ‘e’] )
  ~~~

  

- 딕셔너리 관련 함수
  - list( a.keys() ) - a의 키 값들로 리스트 객체 생성
  - items()  - Key와 Value의 쌍을 튜플로 묶어 dict_items 객체로 반환함
  - clear() - 저장된 요소를 모두 삭제함
  - get( key [, default] ) - a[ key ] 와 같으나, 만약 값이 존재하지 않으면 a[ key ] 가 에러를 출력                                       하는 것과 다르게, get() 은 ‘None’을 출력함
  - key in a - 해당 Key가 딕셔너리 안에 있는지 조사



- 불(Bool)

  - 논리 자료형으로 True(참) / False(거짓) 가 있음 ** 첫글자는 대문자!

  ~~~
  - 일반 값으로 쓰일 때
      a = True
      print( a )
  - 함수형태로 쓰일 때
      bool( ‘Python’ )
      >> True
  ~~~



- 자료형 관련 내장함수 (built in)
  - 특정 객체의 자료형을 변환해주는 내장 함수
  - int( obj )  - 정수로 변환
  - int( obj , n )  - 2 | 8 | 16 진수로 변환
  - float( obj ) - 실수로 변환
  - str( obj ) - 문자열(문자열 값의 형태)로 변환
  - repr( obj ) - 문자열(객체 형태)로 반환
