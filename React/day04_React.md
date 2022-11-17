# DAY 04

## -- React --

- 이미지 삽입

  - import Img from './images/flower_small1.jpg';

    - <img src={Img}></img>

    - 위 처럼 하면 계속 import해서 삽입 해야함 이미지를 많이 넣어햐 할 경우 아주 불편

  - 그래서 이미지 파일을 public안에 넣어줘야함

  - 이미지 파일을 public 안에 넣고

    - <img src={**process.env.PUBLIC_URL** + "./images/flower_small1.jpg"}/> 처리

### ▷ 리액트 라우터

- 리액트 라우터 사이트 - https://reactrouter.com/en/v6.3.0 

- 라우터

  - **클라이언트 측 라우팅**을 활성화한다.
  - 서버에서 다른 문서를 요청하지 않고도 앱이 링크 클릭에서 URL을 업데이트할 수 있음
    -  대신, 앱은 즉시 새로운 UI를 렌더링하고 fetch새로운 정보로 페이지를 업데이트하기 위해 데이터를 요청할 수 있음
    - 브라우저가 완전히 새로운 문서를 요청하거나 다음 페이지에 대한 CSS 및 JavaScript 자산을 다시 평가할 필요가 없기 때문에 더 빠른 사용자 경험이 가능
    -  애니메이션과 같은 항목으로 보다 동적인 사용자 경험을 가능하게 함
  - 하나의 페이지(SPA)에서 렌더링 해주는 라이브러리 라고 볼 수 있음
    - 사용자가 입력한 주소를 감지하는 역할을 하며, 여러 환경에서 동작할 수 있도록 여러 종유의 라우터 컴포넌트를 제공

- 특징

  - SPA(Single Page Application) 방식
    - 새로운 페이지를 로드하지 않고 하나의 페이지 안에서 필요한 데이터만 가져오는 형태를 가짐
    - React-Router는 신규 페이지를 불러오지 않는 상황에서 각각의 url에 따라 선택된 데이터를 하나의 페이지에서 렌더링 해주는 라이브러리 라고 볼 수 있음

- 설치 

  - npm install react-router-dom@6

  

  - index.js 에서 import {BrowserRouter} from 'react-router-dom';

  - root.render(
      <React.StrictMode>
       	<BrowserRouter>

    ​    		<App />
    ​    		<Myapp /> 
    ​    		<Imgtest/>

    ​    	</BrowserRouter>
      </React.StrictMode>
    );

    - <BrowserRouter>    </BrowserRouter> 안에 파일넣기 

  - import {Routes, Route, Link} from "react-router-dom";

    ~~~
    function RouterTest(){
    
      return(
    <div className="App">
          <h1>리액트 라우터를 이용한 웹페이지 나누기 연습</h1>
          <img src={process.env.PUBLIC_URL + "/images/main_banner.jpg"}/><br/>
          <br></br>
          {/* <a href="">home</a> */}
          {/* <a href="counter.js">카운터</a>  a 태그의 단점 페이지를 불러옴 */}
          <div className="cc">
            <Link to="/" className="bb">home</Link>
            <Link to="/counter" className="bb">counter</Link>
            <Link to="/calculator" className="bb">calculator</Link>
    
          </div>
          <hr/>
          <br/>
          <Routes>
            <Route path="/" element={<div>처음으로 오셨네요...</div>}/>
            <Route path="/counter" element={<Counter/>}/>
            <Route path="/calculator" element={<Calculator/>}></Route>
          </Routes>
        </div>
        )
        }
    ~~~

    