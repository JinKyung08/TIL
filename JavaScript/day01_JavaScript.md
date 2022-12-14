# DAY 01

## -- JavaScript --

### ▷자바스크립트

- 웹브라우저에서 사용하는 프로그램언어

- // - 한줄주석, /* */ - 여러줄 주석

- alert() - 경고창에 출력

- console.log() - 브라우저의 콘솔창에 출력

- document.write() - 문서(body)안에 출력

- ; - 종결 (생략가능)

- 변수 선언시 자료형 쓰지않음
  - 변수에 담긴 값으로 자료형을 판단

- 기본자료형
  - 숫자(number)
  - 문자열(String) " " ,' '
    - 문자와 문자열 구분 X, 모두 문자열로 철리
  - 불린(boolean)
  
- 변수 선언
  - var - 변수를 중복해서 선언 할 수 없다. / 변수가 속하는 범위가 애매할 수 있다.
  - let  - 한번 선언한 변수명  다시 선언할 수 없다 (중복선언 X) / 범위명확 / 변경할 가능성이 있으면 변수로 선언
  - const - 한번 선언할 때 값을 주면 나중에 변경 되지 않을것 (상수) / 변경할 가능성이 없으면 선언
    - 상수는 한 번만 선언할 수 있으므로 반드시 선언 할떄 값을 지정해줘야 한다
    - 한 번 선언된 상수의 자료는 변경할 수 없다.

- 비교 연산자

  - == (값이 같다) != (값이 같지 않다)

  - === (값과 자료형이 같다)
  - !== (값과 자료형이 같지 않다)
  - \> , \>= ,\< ,\<=

- 자료형검사

  - typeof(  ) - ()생략가능
  - typeof 연산자는 결과로 string, number, boolean, undefined, function, object, Symbol, BigInt 라는 8가지 중에 하나를 출력

- 템플릿 문자열 

  - 백틱(`)기호로 감싸 만들기 
  - 문자열 내부에서 표현식이나 변수를 사용하고 싶으면 ${  } 기호 안네 넣기

- 문자열 입력

  - prompt(메시지 문자열, 기본 입력 문자열) 
  - 기본 입력 문자열은 생략가능

- 문자열을 숫자자료형으로 변환

  - Number(자료)

  -  Number('89') -> 89

  -  단 숫자에 문자가 붙은 자료형은 NaN이란 값 출력

  -  NaN : Not a Number, 숫자이지만 숫자로 나타낼 수 없는 숫자 

  -  Number('$234')  -> NaN  값은 숫자로 나타낼 수 없지만 타입(자료형)은 숫자

-  숫자 연산자를 사용해 자료형 변환하기

  - 숫자형식의 문자열('234')을 숫자 자료형으로 변환 => 연산자 -,*,/를 사용

  - '234' * 1 => 234

  - '234' - 0 => 234

  -  '234' / 1 => 234

- 문자열 자료형으로 변환하기

  - String() 합수 이용 : String(자료)

  - String(234) => '234'

-  \+ 연결연산자 이용

  - 234 + '가' => '234가'

  - 234 + "" => '234'

- Boolean() 자료형 

  - 대부분의 자료는 true로 변환

  - 단, 0, NaN, '', "", null, undefined 5개는 false로 변환 
  
    

- 삼항연산자 : 조건 ? 조건이 참일 때 실행할 것 : 조건이 거짓일 때 실행할 것
-  if(조건){}
  - if(조건 : true/ false를 확인할 수 있는 것){

  					조건이 참일 때 실행할 문장

​							 }


  - if(조건){

  조건의 결과가 참일 때 실행할 문장

 }else{

  조건의 결과가 거짓일 때 실행할 문장

 }

- if(조건){

  조건의 결과가 참일 때 실행할 문장

 }else if(조건){

  조건의 결과가 참일 때 실행할 문장

 }else{

  조건의 결과가 거짓일 때 실행할 문장

 }

- Javascript Date Objects

  - const date = new Date();

  - let date = new Date();
    - new Date()
    - new Date("2022-11-04")
    -  new Date(year, month, day)
    - new Date(2022,11,04)
    - new Date(year, month, day, hours)
    - new Date(year, month, day, hours, minutes)
    - new Date(year, month, day, hours, minutes, seconds)
    - new Date(year, month, day, hours, minutes, seconds, ms)
    - getFullYear() => 4자리 연도, 2022
    - getMonth() => 월 (0~11) , getMonth() + 1 (1~12)
      - getDate - 일
      - getDay - 요일(0~6(0: 일요일~~ 6 : 토요일))

- 자바 스크립트 배열 

  - 다양한 자료형을 저장할 수 있음

  - 여러개의 변수를 한번에 선언해 다룰 수 있는 자료형 
    -  [요소1,요소2,...] => 요소 : 값
    - const(let, var) 배열명(=변수명) = [값1, 값2,...] 
    - const 배열명 = new Array(값1,값2,...)