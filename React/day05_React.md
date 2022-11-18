# DAY 05

## -- React --

### ▷ ajax (Asynchronous Javascript And Xml)

- 서버에 GET,POST 요청을 할 대 웹페이지의 새로고침없이 데이터를 주고 받을 수 있도록 도와주는 브라우저 기능

- 자바스크립트 라이브러리

- 페이지 일부만을 위한 데이터를 로드하는 기법으로 자바스크립트를 사용하는 비동기 통신, 서버와 클라이언트 같이 XML 데이터를 주고받는 기술 

- npm install axios

- 서버 - 정보제공

- 클라이언트 - 정보요청

  - <button onClick={()=>{

       axios.get(서버로부터 가져오고자 하는 데이터 / URL).then((결과)=>{

    ​    console.log(결과.data) 

       }).catch(()=>{실패했을 때 처리할 것들})

      }}>자료가져오기</button>

  - axios : 리액트에서 AJAX를 구현하기 위해 사용
    - 리액트에서 AJAX를 구현하기 위해서는 자바스크립트의 내장객체인 XMLRequest를 사용하거나, HTTP Client를 사용 HTTP Client의 라이브러리 중 하나
  - REST API 
    - REST란 어떤 자원에 대해 CRUD(Create, Read, Update, Delete)연산을 수행하기 위해 URI로 요청을 보내는 것으로 Get, Post 방식의 method를 사용하여 요청을 보냄 
    - 요청을 위한 특정한 형태로 표현되며, 이러한 REST 기반의 API를 웹으로 구현한 것이 REST API
  - REST API 대표적인 http 메서드
    - GET : 데이터 조회
    - POST : 데이터 등록 및 전송
    - PUT : 데이터 수정
    - DELETE : 데이터 삭제
  - POST 요청하는 방법
    - axios.post('URL', {name : '홍길동'}).then(()=>{완료시 특정 코드를 실행하고 싶을 때 작성})
    - "{"name " : " 홍길동 "}" => 서버로부터 받아오는 데이터는 문자열, JSON
  
  

- build
  - npm run build
