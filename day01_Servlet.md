# DAY 01

## -- Servlet --

### ▷ Server

- client (요청)  ----->  Server

- client <----- (응답) Server

- 종류 

  - Web Server - 웹 브라우저와 HTTP 프로토콜을 사용하여 사용자의 요구에

    따른 특정 서비스를 제공하는 서버

  - Mail Server - 인터넷을 통해 사용자 간의 전자 우편을 주고 받는 서비스

    제공

  - FTP Server - 서버 내에 파일을 업로드, 다운로드 할 수 있도록 파일 관리

    기능 제공

  - Telnet Server - Terminal, 텍스트로만 이루어진 창에서 특정 명령어를 통해

    원격지 서버를 접속, 관리

  - Database Server - Data를 저장하고, 원격지에서 접속할 경우 권한에 따라 해당
    데이터를 열람, 추가, 수정, 삭제 기능 처리



### ▷ Web

- 통신구조
  - client(서비스 사용자) ↔ Web  Server (HTML) ↔ WAS (JSP/Servlet) ↔ Database (데이터 관리 서버)

- Web Server
  - 사용자에게 HTML페이지나 jpg, png같은 이미지를 HTTP프로토콜을 통해
    웹 브라우저에 제공하는 서버로 내부의 내용이 이미 만들어져 있는
    정적인 요소들을 화면에 보여주는 역할
- Web Server의 종류
  - **Apache** - Apache Software Foundation에서 만든 서버로 HTTP통신에 대한 여러 라이브러리 제공
  - Window IIS - Window OS에서 제공하는 웹 서버 /  높은 수준의 보안성과 성능 제공
  - NGINX - 무료 오픈 소스 서버로 사용자 요청을 스레드가 아닌 확장성이 있는 이벤트 기반 설계로 리소스만 할당해 사용



### ▷ WAS 

- Web Application Server

- 사용자가 요청한 서비스의 결과를 스크립트 언어 등으로 가공하여 생성한 동적인 페이지를 사용자에게 보여주는 역할

- WAS의 종류

  - **tomcat** - Apache Software Foundation에서 Servlet과 JSP를 통한 동적인 웹 문서를 처리하기 위해 만든 웹 애플리케이션 서버
  - wildfly - 톰캣이 제공하는 Servlet Container 뿐만 아니라 EJB Container를 별도로 제공 / 폭 넓은 서비스 구현 
  - jeus - 국산 / 대용량 데이터 트랜잭션을 고성능으로 처리하며 개발 및 운영에 관한 기술 지원이 뛰어남

  

- 서블릿 컨테이너 (Servlet - Container)

  - 서블릿의 생명 주기 관리 (생성, 초기화, 소멸)
  - HttpServletRequest / HttpServletResponse객체 생성
  - 요청에 따라 멀티 스레딩 구성
  - 전송 방식에 따라 동적으로 페이지 구성하는 작업 진행
  - 정적 로딩 처리

- JSP 컨테이너 (JSP - Container)

  - JSP파일을 다시 java코드로 변경해주고 class파일로 전환하여 메모리 공간에 로드한 뒤 실행 가능하게 만드는 작업 진행(Servlet화)
  - 처리 결과를 HTML파일로 만들어주는 작업 진행
  - 동적 로딩 처리

- Web Server 와 WAS 의 장단점
  - WebServer 장점 
    - 빠른 처리 속도
    - 구현이 쉬움
  - 단점
    - 한정적 서비스
    - 글의 추가, 수정, 삭제가 어려움
  - WAS 장점
    - 서비스의 다양성
    - 글의 추가, 수정, 삭제가 쉬움
  - 단접
    - 느림
    - 구현 어려움

### ▷ Servlet

- 외부에서 특정 페이지(url)의 요청(Request)에 따라 응답(Response) 내용을 사용자가 정의한 Class
- 서블릿은 요청과 응답 사이에 사용자가 정의한 기능에 대한 비지니스 로직(알고리즘, 코드)을 구현한 구조로 구성됨
- 사용법 : HttpServlet을 상속하고, doGet, doPost를 재정의(오버라이딩 @Override)하여 사용함

- 사용자 데이터 전송 방식
  - get 방식
    - URL창에 “?” 뒤에 데이터를 입력하는 방법(쿼리스트링)
    - 데이터가 여러 개일 경우 &로 묶어서 보냄
    - 조회,검색에 많이 사용 
    - 데이터 크기에 한계가 있으며 보안 취약
  - post 방식
    - BODY에 내용을 보내는 방식으로 데이터 크기에 제한이 없고 보안이 뛰어남
    - 쓰기 
    - 히스토리 안남음
- 메소드
  - doGet
    - client에서 데이터 전송 방식을 get방식으로 전송하면 호출되는 메소드
  - doPost
    - client에서 데이터 전송 방식을 post방식으로 전송하면 호출되는 메소드
- 매개변수 객체
  - HttpServletRequest - HTTP Serlvet을 위한 요청 정보(request information) 제공
  - HttpServletResponse - 요청에 대한 처리 결과를 작성하기 위해 사용하는 객체