# DAY 03

## -- JSP --

### ▷ JSP

- HTML에 Java를 결합할 수 있는 도구(문법)
- 컴파일 할 때는 java로 변환되어 실행됨
- 기본적으로 HttpServlet을 상속하고, Servlet의 모든 기능을 상속

- 단, 주로 View를 그리기 위해 활용됨으로 복잡한 로직(=비지니스 로직)은 Servlet(Controller)에서 처리됨
  - MVC2 패턴 구성시 View-JSP, Controller-Servlet, Model-Service, DAO,VO



- 표기법
  - 주석  - <%--   --%>
  - 지시자 - <%@   %>
  - 선언문 - <%!     %>
  - scriptlet - <%    %>
  - 표현식 -  <%=    %>



### ▷ 지시어 (Directive)

- JSP page전체에 영향을 미치는 정보를 기술할 때 쓰임

- page 태그 - 현재 JSP 페이지 컨테이너에 필요한 각종 속성을 기술하는 태그

  - language : JSP 페이지 내부에서 사용할 언어를 지정한다. (초기확장을 위해 만들어지고 안쓴다!)

  - contentType : 웹브라우저에서 해당 페이지의 프로토콜, 표현식, 인코딩 확인하기 위해 사용

  - pageEncoding : jsp에서 사용할 인코딩을 표시함 -> java 컴파일 용도 및 전송용

  - import : 자바의 import와 같이 외부 class를 로드할 때 사용됨 

    ※  Tip, 자동완성 방법 추천 : 기존 단축키 먹히지 않음으로 Class 이름 끝에 자동완성을 쓰면 완성됨

  - errorPage : JSP 페이지에서 예외가 발생한경우 처리할 페이지를 지정할 수 있다.

  - isErrorPage : 자신이 에러페이지라는 것을 알리는 구문

- include 태그 - JSP 페이지 내부에서 다른 JSP나 HTML페이지를 로드할때 사용하는 지시어 헤더,풋터 활용

- taglib 태그 -  JSP 태그 외에 확장할수 있는 태그를 import 할때 사용, ex) 액션태그, EL, JSTL



### ▷JSP 내장 객체

- JSP에서 기본적으로 제공하는 객체들로 request, response, out 등 Scriptlet tag와 Expression tag에서 사용할 수 있게 암시적으로 선언된 객체

- JSP 코드에서 별도로 import나 선언 없이 사용 됨

- 내장 객체

  - request : Client의 요청 내용을 담고 있는 객체 / HttpServletRequest 객체 참조 변수 
  - response : Client에게 응답할 내용을 담을수 있는 객체 / HttpServletResponse
  - session : 브라우저 ID를 통해 사용자의 고유정보를 담을수 있는 객체 / HttpSession
  - out : html을 출력할수 있는 객체, response.getPrinter()와 동일 / JspWriter
  - application : Context의 변수 버전으로 Attribute 저장에 활용됨 (잘 안씀) / ServletContext
  - page : 현재 JSP 페이지 내에서만 사용할수 있는 참조변수 (page = this)
  - pageContext : JSP 페이지에 관련된 변수를 관리하거나 제어권을 다른페이지로 넘길때 활용

- JSP 내장 객체 영역

  - page - 하나의 JSP페이지를 처리할 때 사용되는 영역
  - request - 하나의 요청을 처리할 때
  - session - 하나의 브라우저와 관련된 영역
  - application - 하나의 웹 애플리케이션과 관련된 영역

  - 객체간 유효한 범위(Scope)를 가지며, 속성값(Attribute)를 통해 사용자 데이터를 공유 가능

- 영역객체 종류

  - Page Scope : pageContext를 통해 접근, 페이지가 웹브라우저에 살아 있는 동안 유효 (로컬 객체와 같음)

  - Request Scope : request를 통해 접근, 웹브라우저의 요청을 처리하는 동안 유효(페이지 이동도 가능) 

  - Session Scope : session를 통해 접근, 사용자가 지정한 세션의 생명주기 동안 유효, 브라우저 종료까지 유효

  - Application Scope : application통해 접근, 웹 어플리케이션(WAS, 서버)가 실행되는 동안 유효 = context

    ※ 위에서 아래로 내려갈수록 긴 생명주기를 가짐