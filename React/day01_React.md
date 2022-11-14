# DAY 01

## -- React --

### ▷ 리액트

- 사용자 인터페이스를 만들기 위한 자바스크립트 라이브러리

- SPA - Single Page Application

- 장점

  - 빠른 업데이트와 렌더링 속도
  - Virtual DOM
  - 컴포넌트 기반 구조 
  - 재사용성 
  - 모바일 앱개발 가능

- 단점

  - 방대한 학습량
  - 높은 상태 관리 복잡도

- 리액트 가져오기

  - <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>        
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>

- create-react-app
  - npx create-react-app 폴더명 또는 .
  - node.modules - 라이브러리 코드 모음
  - public - static 파일 (html,css)
    - **index.html (화면에 보여짐)**
  - src - 실제 코드 짜는 곳
    - **App.js - 메인 (변경가능)**
    - **index.js - App파일을 index.html 파일에 넘기는 역할을 함**
    - package.json - 프로젝트 정보가 들어있음
  - cd 폴더명
  - npm start

### ▷ JSX 

- 자바스크립트와 HTML을 한 번에 합쳐 놓은 것 같은 문법

- JSX(JavaScript XML)로 작성한 코드는 브라우저에서 실행되지 전에 바벨을 통해 번들링되는 과정에서 일반 JS코드로 변환

- 코드1) 자바스크립트로 구현

  - Function App(){Return React.createElemnet("div",null,"Hello",React.createElement("b",null,"react:));}

- 코드2) JSX문번으로 구현

  - function App(){

    ​			return (\<div>Hello\<b>React\</b>코드\</div>)};

    - 코드1과 코드2는 같은 문법

- 주의사항

  - 컴포넌트에 여러 요소가 있다면 반드시 부모 요소 하나로 감싸야 함

    - why?) Virtual DOM에서 컴포넌트 변화를 감지할 때, 효율적으로 비교할 수 있도록 컴포넌트는 내부에 하나의 DOM 트리 구조로 이루어져야 한다는 규칙 때문

    - ex) return(\<h1>Hello React\</h1>\<h2>잘 실행될까?\<h2>);  //오류

      - 요소가 너무 많음, 하나의 부모 요소로 묶어야함

    - 해결) return(

      ​				\<div>

      ​				\<h1>Hello React\</h1>\<h2>잘 실행될까?\<h2>

      ​				\</div>

      ​			;)
    
  - 자바스크립트 표현
  
    - JSX안에서 코드를 { }로 감싸면 자바스크립트 표현식을 사용할 수 있음
  
    - function App(){
  
      ​			const name="홍길동";
  
      ​			return(\<h1>{name}님 안녕!\</h1>);
  
      }
  
  - if문 대신 조건부 연산자(삼항 연산자) 사용 : JSX 내부에서는 if문 사용 할 수 없음
  
    - return(\<div>{name==="홍길동" ? (\<h1>홍길동입니다.\<\h1>) : (\<h1>홍길동 아님 \</h1>)}\</div>)
  
  - AND 연산자를 사용한 조건부 렌더링
  
    - 개발하다 보면 특정조건을 만족할 때 내용을 보여주고, 만족하지 않을 경우 아예 렌더링하지 않아야 하는 경우
    -  function App() { Const name = ‘리액트’; Return \<div>{name === ‘리액트’ && \<h1> 리액트입니다.\</h1>}\</div>; }
      - 위와 같이 코드를 작성하면 name이 ‘리액트’일 떄는 '리액트입니다'가 렌더링되고 아닐 경우 아무것도 나타나지 않음.
  
  - 인라인 스타일링
  
    - DOM 요소에 스타일을 적용할 때는 문자열 형태로 넣는 것이 아니라 객체 형태로 넣어주어야 함
    - render() { const tempStyle={ display:"inline-block", width:"100px", height:"100px", boder:"1px solid black", background:"orange", } 
                  return ( \<Fragment> \<div style={tempStyle}>\</div> \</Fragment> ); } }
      - background-color와 같이 - 문자가 포함될 경우 카멜 표기법인 backgroundColor로 작성해야 함
  
  - class 대신 className 사용
  
    - Why className ?   html에서는 ‘.’을 이용하여 class에 대한 css를 적용하지만, 리액트에서는 class가 예약어라 사용이 불가능하다.  그래서 className을 이용해서 css를 적용한다.
  
    - \<div className = “react" >{name} \</div>
  
      

​      

- 컴포넌트 - 부품화가능
- 첫글자는 반드시 대문자로 처리
- props : 함수를 호출하는 쪽에서 매개변수를 주면 매개변수를 받아오는 객체

  ​			부모로부터 자식 컴포넌트한테 값을 부여하고자 할 때 

  ​			props 객체를 사용 

- useState : state Hook 

  - state : 자신의 상태값을 저장하고 있음, 변수들 

    ​			 클래스기반 컴포넌트 클래스내부에 공통변수를 만들 수 있음

