# DAY 02

## -- Servlet --

### ▷ Page 이동

- forward 방식
  - Response - RequestDispatcher에서 forward 함수를 활용하여 이동하는 방식
  - 페이지 이동이 되면서 가지고 있던 파라메터 및 Attribute를 모두 넘겨줌.
  - 예시) 로그인 Controller(Servlet) -> 로그인 결과 View (JSP) 
  - [MVC패턴2] 에서 활용됨
  - 메커니즘 : 서버에서 서버로 내부 이동하는 방식 



- SendRedirect 방식
  - Request - SendRedirect 함수를 호출하는 방식
  - 페이지가 이동되면서 기존에 가진 파라메터 및 Attribute를 초기화 함
  - 예시) 로그인 실패 -> 메인페이지로 이동 시킬때, 기존 data를 소거하고 get 방식
  - 주로 단순 페이지 이동에도 활용됨.
  - 메커니즘 : 사용자 브라우저에서 페이지가 이동되는 원리
  - SendRedirect
    - 단순 페이지 이동으로 사용자 파라메터와 Attribute가 저장되지 않음.
    - 다음 페이지 호출은 get방식으로 호출됨!



### ▷ Session , Cookie

- Session
  - HTTP 프로토콜 중 하나로, 서버에서 Session ID를 통해 사용자 정보를 저장하는 용도로 활용
  - 저장 기간 : 클라이언트 (브라우저)가 종료되었을때 세션 해지, 서버가 지정한 시간의 time out 시 
  - 저장 위치 : 서버의 메모리 공간 / 디스크 공간 (임시적으로 생성됨)
  - 특징 : 쿠키 보단 보안적으로 안전하다.
  - 단점 : 인터넷 연결이 불완전하거나 브라우저가 종료되는 경우 세션이 유지 않음

​     			 -> 최근 스마트폰 환경에서 단점을 보완하기 위해 cookie와 혼용되어 활용됨

```
// Session 생성(HttpServletRequest에 있음)
HttpSession 세션명=HttpServletRequest.getSession();

//생성된 Session값 설정  (객체도 넣을수 있다.)
세션명.setAttribute(“이름”,”값(Obj)”); 
//세션데이터 설정  (옵션, default : 30분)
세션명.setMaxInactiveInterval(숫자); //세션유지시간설정

//생성된 Session 호출
HttpSession 세션명=HttpServletRequest.getSession();
세션명.getAttribute(“이름”); // 데이터불러오기
```



		getSession(true) : session 있으면 세션을 가져오고 없으면 생성해서 넣어줌 (default)
		getSession(false) : session 있으면 세션을 가져오고, 없으면 null로 반환



- Cookie

   *  HTTP의 기록서의 일종으로 사용자가 웹사이트를 방문하면 사이트에서 사용하는 정보를 저장할수 있는 기능
   *  쿠키 표준 : 최대 4kb, 저장갯수 3000개 
   *  기록 장소 : 웹브라우저가 지정한 고유 path에 저장됨 (Client)
      *  특징 : 보안에 취약하다고 알려짐 -> 개발자가 안전하게 사용할수 있도록 기술적 보완을 하거나 중요하지 않은 기능만 저장

  ~~~
  //Cookie클래스 생성(패키지 import)
  Cookie 쿠키명 = new Cookie("key",”value”);
  //생성된 쿠키설정
  setMaxAge(int expiry) : 유효시간설정
  setPath(String uri) : 경로설정
  ** 서버의 모든 요청 X / 특정 경로를 통한 요청시 쿠키를 사용하는 경우
  setDomain(String domain) : 쿠키도메인 설정, 쿠키생성
  ** 도메인 외의 도메인 설정시 사용
  //생성된 쿠키 전송
  response.addCookie(Cookie cookie) : 생성된 쿠키전송
  ~~~

  

