# DAY 04

## -- HTML --

### ▷ 입력 양식 태그

- 입력 양식은 사용자에게 정보를 입력받는 요소

- get방식 - 주소에 데이터를 입력해서 전달
- post방식 - 비밀스럽게 데이터 전달

~~~
<form action="전송위치, 입력양식을 처리할 파일명" method="전송방식" name="이름"></form>
ex)<form action="" method="post" name="member" id="member">

~~~

- label : 글자를 클릭해도 입력에 포커스 가게 하기

  - 단, for와 id의 값이 같아야지만 가능

- input type

  - text : 글자 입력

  - button : 버튼 생성

  - checkbox : 체크박스 생성

  - hidden : 보이지 않음

  - password : 비밀번호입력

  - radio : 라디오 버튼 생성

  - reset : 초기화 버튼 생성

  - submit : 제출 버튼 생성

- textarea 
  -  cols/rows : 여러행의 글자 입력 양식 생성, cols - 너비, row-높이
- select : 선택 양식 생성
- option : 옵션생성