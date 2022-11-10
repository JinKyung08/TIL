# DAY 05

## -- JavaScript --

### ▷버그(bug)

- 버그(bug) - 소프트웨어 버그, 프로그램의 오류나 결함
- 디버그(debug) - 프로그램에 발생한 버그의 원인을 파악하여 제거하고 프로그램이 제대로 동작하도록 수정하는 작업
- use strict  - 엄격모드

- 즉시 호출 함수 - 변수 이름 충돌문제를 해결하기 위해 사용



### ▷ 예외 처리

- try{

  ​	예외가 발생할 수 있는 문장

  }catch(예외객체){

  }

- try{

  ​	예외가 발생할 수 있는 문장

  }catch(예외객체){
  }finally{

  }

-  예외 발생시키기 : throw표현식



### ▷ Class

~~~
ex)
class Rectangle { //클래스명
        constructor(width, height) {  //생성자
          this.width = width
          this.height = height
        }


~~~

- 상속
  - class 자식클래스명  extends 부모클래스명{ }