# DAY 03

## -- JavaScript --

### ▷ String 객체

- trim() : 문자열 양쪽 끝의 공백 없애기
- split() : 문자열의 특정 기호로 자르기
- length() : 문자열의 길이
- slice(시작, 끝) : 문자열을 추출
-  substring(시작, 끝)
- substr(시작,끝)
- replace("변경하려는 값","바꿀값") : 값1을 값2변경
- charAt(인덱스) : 인덱스위치의 글자 추출

### ▷ JSON

- JavaScript Object Notation, 자바스크립트의 객체처럼 자료를 표현하는 방식
- 값을 표현할 때는 문자열, 숫자, 불 자료형만 사용할 수 있음 (함수 사용 불가능)
-  문자열은 반드시 큰따옴표("")로 만들어야 함
- 키에도 반드시 큰따옴표("")를 붙여야 함 

- JSON의 배열 [{"이름 : "값"},{"이름" : "값"},...]
-  자바스크립트 객체를 JSON 문자열로 변환 : JSON.stringify()
-  JSON.stringfy(데이터,객체에서 어떤 속성만 선택해서 추출하고 싶을 때 사용하나 대부분 null,들여쓰기칸수)
- JSON 문자열을 자바스크립트 객체로 변환(전개) : JSON.parse()



### ▷DOM(Document Object Model)

- 문서객체 모델, 문서 객체 : html태그를 자바스크립트에서 사용하는 객체 만든것 

  - window(document).onload = function(){

  ​            실행할 코드들

  ​       };

  - document.addEventListener('DOMContentLoaded', function(){

  ​             실행할 코드들

  ​       });

- 부모객체.appendChild(자식객체) : 부모 객체 아래에 자식객체를 추가

- 부모객체.removeChild(자식객체) : 자식객체(문서객체)를 제거
  - 문서객체.parentNode.removeChild(자식객체)