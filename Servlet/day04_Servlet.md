# DAY 04

## -- Servlet --

### ▷MVC
 
- Model View Controller
- 웹 어플리케이션 개발 시 MVC 패턴을 적용하여 각각의 역할 별 작업이 가능하도록 분담하는 설계 패턴
- Model 
  - DB와 관련된 비지니스 로직을 수행할 서비스를 담당
  -  Service
    - 여러 DAO호출 -> 데이터 접근/갱신 ->읽은 데이터에 대한 비지니스 로직을 수행하여 controller에 결과 전송하는 클래스
  - DAO
    - Data Access Object
    - DB에 직접 접근하여 요청 받은 결과를 반환하는 클래스
  - VO
    - Value Object
    - 계층 간 데이터 교환을 위한 객체 클래스
- View
  - 사용자가 요청하거나 요청한 정보를 응답 받아 볼 수 있는 화면을 담당하며
    JSP, HTML 등을 통해 표현
- Controller
  - 사용자의 요청을 전달 받아 응답처리를 위한 Service를 호출하고 결과를
    View에 전송하는 클래스로 Servlet으로 작성
  - 사용자 요청을 분석한 후, 서비스에 전달할 VO 객체를 생성하여 Service에 전달하고 Service로부터 결과를 관련된 View 화면에 담아 사용자에게 응답

- RequestDispatcher
  - 사용자의 요청을 다른 서블릿이나 JSP 페이지에 전달할 때 사용하는 클래스로
    request 객체를 사용해 생성할 수 있다.
