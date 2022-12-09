# Day 01

## -- Spring --

### ▷ Apache Maven

- Project Object Model(POM) XML문서를 통해 해당 프로젝트의 버전 정보(내부) 및 라이브러리 정보(외부)들을 통합하여 관리하는 프레임워크

- 라이브러리 종속성

  - Maven을 사용하면 pom.xml문서에 사용하고싶은 라이브러리를 등록하여 자동으로 프로젝트에 추가 -> 라이브러리 관리의 편리성 제공

- POM

  - POM(Project Object Model)
  - 하나의 프로젝트에서 사용하는 자바 버전, 라이브러리, 플러그인 구성을 통합하여 관리할 수 있게 각 설정 정보를 XML로 문서화한 것

  

### ▷Spring

- 자바 플랫폼을 위한 오픈 소스 애플리케이션 프레임워크

- 동적인 웹 사이트를 개발하기 위한 여러 가지 서비스를 제공

- 특징  (servlet과 다른 점)

  - DI(Dependency Injection) 의존성 주입
    - 개발자가 직접 의존하는 객체를 생성할 필요 없음 (new 안씀)
  - Spring AOP (Aspect Oriented Programming) 관점 지향 프로그래밍
    - 트랜잭션, 로깅, 보안 등 여러 모듈, 여러 계층에서 공통으로 필요로 하는 기능의 경우 해당 기능들을 분리하여 관리
  - POJO (Plain Old Java Object)
    - 일반적인 J2EE 프레임워크에 비해 특정 라이브러리를 사용할 필요가 없어 개발이 쉬우며 기존 라이브러리의 지원 용이
  - IoC (Inversion of Control) 제어 반전
    - 컨트롤의 제어권 프레임워크에 있다는 뜻
    - 객체의 생성부터 모든 생명주기의 관리까지 프레임워크가 주도
    - 만들어둔 자원을 호출하여 사용
  - Spring JDBC
    - MyBatis나 Hibernate 등의 데이터베이스를 처리하는 영속성 프레임워크와 연결할 수 있는 인터페이스 제공
  - **Spring MVC**
    - MVC 디자인 패턴을 통해 웹 애플리케이션의 Model, View,Controller 사이의 의존 관계를 DI 컨테이너에서 개발자가 아닌 서버가 객체들을 관리하는 웹 애플리케이션 구축

- Spring의 구성 모듈

  - Data 접근 계층
    - JDBC나 데이터베이스에 연결하는 모듈로 Data 트랜잭션에 해당하는 기능을 담당하여 영속성 프레임워크의 연결 담당

  - MVC 계층(MVC / Remoting)
    - Spring Framework에서 Servlet, Struts 등 웹 구현 기술과의 연결점을 Spring MVC 구성으로 지원하기 위해 제공되는 모듈 계층
  - AOP 계층
    - 각 흐름 간 공통된 코드를 한 쪽으로 빼내어 필요한 시점에 해당 코드를 첨부하게 하기 위해 지원하는 계층
  - Core Container
    - Spring의 핵심, 모든 스프링 관련 모듈 Core Container 기반으로 구축
    - Spring의 근간이 되는 IoC(또는 DI) 기능을 지원하는 영역 담당
    - BeanFactory를 기반으로 Bean클래스들을 제어할 수 있는 기능 지원

- 모듈 

  - spring-beans - 객체를 생성하는 기본 기능 제공
  - spring-context - 객체 생성, 라이프 사이클 처리, 스키마 확장 등의 기능 제공
  - spring-aop - AOP 기능 제공
  - spring-web - REST클라이언트 데이터 변환 처리, 서블릿 필터, 파일 업로드 지원 등 웹 개발에 필요한 기반 기능 제공
  - spring-websocket - 스프링 MVC에서 웹 소켓 연동을 처리할 수 있도록 제공 (과도한 트래픽 유발 -> 잘 안씀)
  - spring-oxm - XML과 자바 객체 간의 매핑을 처리하기 위한 API 제공
  - spring-tx - 트랜잭션 처리를 위한 추상 레이어 제공
  - spring-jdbc - JDBC프로그래밍을 보다 쉽게 할 수 있는 템플릿 제공
  - spring-orm - Hibernate, JPA, MyBatis 등과의 연동 지원
  - spring-jms - JMS서버와 메시지를 쉽게 주고 받을 수 있도록 하기 위한 템플릿
  - spring-context-support - 스케줄링, 메일발송, 캐시연동, 벨로시티 등 부가기능제공

  

- Spring의 동작 구조

  - Spring컨테이너 구동 시 한 개의 spring환경 설정된 xml파일을 불러오는데 이 파일에 bean, aop, transaction 등 여러 사항을 다 작성하여 구동
  - @Annotation
    - xml파일에는 구동 시킬 필수 요소만 작성하고 소스 코드에 Annotation으로 표시하여 구동

- Spring MVC

  - Spring Framework에서는 클라이언트의 화면을 표현하기 위한 View와 서비스를 수행하기 위한 개발 로직 부분을 나누는 MVC2 패턴 지원
  - Model, View, Controller 사이의 의존 관계를 DI 컨테이너에서 관리하여 유연한 웹 애플리케이션을 쉽게 구현 및 개발 가능