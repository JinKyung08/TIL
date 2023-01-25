# Day 01

## -- Spring Boot --

### ▷ Spring Boot

- 독립형 spring 애플리케이션 생성
- Tomcat, Jetty 또는 Undertow 직접 포함(WAR 배포 필요X)
- 독자적인 'starter'종속성을 제공 -> 빌드 구성을 단순화 
- 가능할 때마다 자동으로 Spring 및 타사 library 구성
- 메트릭, 상태 확인 및 외부화된 구성과 같은 프로덕션 준비 기능 제공
- 코드 생성 및 XML 구성에 대한 요구 사항이 전혀  없음



---

Spring Boot(자식) 독립 프로젝트가 아닌 Spring Framework(부모)의 상속 버전

Framework -> Boot 쉬움, Boot -> Spring Framework 어려움



- **Spring Framework** vs **SpringBoot**

|          구분          |                       Spring Framework                       |                          SpringBoot                          |
| :--------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|          개념          |      Enterprise(SI)계열에 최적화된 Web 개발 프레임워크       |  Restful / MSA 설계에 최적화된 Spring Framework의 확장 버전  |
|        설계방법        | Monolithic Architecture가 일반적(기존 MVC 프로젝트 기반의 대형 서비스) | 기존 + Micro Service Architecture도 지원(REST API / 다양한 UI/플랫폼 에서 활용) |
|       주요 특징        |              XML 기반의 DI를 활용한 다양한 기능              | Auto Configuration 지원<br/>(XML과 DI는 사용자에게 노출되지 않음) |
|          서버          |                외부 서버가 반드시 존재해야 함                |            Tomcat이 내장되어 있어 독립 실행 가능             |
|       설정 방법        |     .xml 기반의 DI를 통해 다양한 객체를직접 관리 해야 함     | application.properties로 관리<br/>(별도 사용자 설정은 Java에서 Configuration 객체를 생<br/>성하여 설정 필요, 사실 더 복잡 할 때도 있음) |
| 프로젝트<br/>생성/관리 | 공식 Spring Project 샘플 (MVC)<br/>기반으로 의존성 관리 DI(XML) 설정 추가 | Spring Stater를 통해 의존성 관리 수행<br/>(만일 Stater에 원하는 툴이 없다면 추가하기 까다로움 ) |
| 표준적인<br/>도구 Set  | Template : JSP<br/>Persistence : MyBatis<br/>Log / Test : log4j, Junit4 | Template : Thymeleaf / JS(Vue,리액트)<br/>Persistence : Hibernate, JPA(CRUDRepo)<br/>Log / Test : logback, Jupiter |



- Spring Starter
  - 스프링 부트 전용 도구
  - 프로젝트에 필요한 기본 설정과 의존성 관리를 자동으로 관리
- 주요한 Depedencies

| 분류 | 도구 이름                | 설 명                                                        |
| ---- | ------------------------ | ------------------------------------------------------------ |
| 개발 | Spring Boot<br/>DevTools | Provides fast application restarts, LiveReload, and configurations for enhanced<br/>development experience<br/>빠른 재시작 및 로드 지원, 개발 개발자용 도구로 필수적 |
| 개발 | Lombok                   | Java annotation library which helps to reduce boilerplate code.<br/><br/>어노테이션을 통해 생성자 get/setter 생성 |
| Web  | Spring Web               | Build web, including RESTful, applications using Spring MVC. Uses Apache<br/>Tomcat as the default embedded container.<br/>Spring MVC 기반 어플 생성, REST 사용 가능 톰캣 내장하여 관리 |
| Web  | Thymeleaf                | A modern server-side Java template engine for both web and standalone<br/>environments. Allows HTML to be correctly displayed in browsers and as static<br/>prototypes. 템플릿 엔진으로 JSP 대체하여 사용 |
| DB   | JDBC API                 | Database Connectivity API that defines how a client may connect and query a<br/><br/>database. DB 접근을 위한 기능 활용 |
| DB   | Spring Data JDBC         | Persist data in SQL stores with plain JDBC using Spring Data.<br/><br/>JDBC Data 활용 (JPA 사용시 필수) |
| DB   | Spring Data JPA          | Persist data in SQL stores with Java Persistence API using Spring Data and<br/>Hibernate.<br/>Hibernate 및 JPA, CRUDRepo 사용시 필수적인 의존성 |
| DB   | MySQL Driver             | MySQL JDBC drive                                             |
| IO   | Validation               | Bean Validation with Hibernate validator.<br/><br/>VO(Bean)에서 특정 값에 대한 검증을 대신 해주는 기능(DB 제약과 동일기능) |

- 알아 두면 좋은 dependencies

| 분류                                       | 도구 이름                         |
| ------------------------------------------ | --------------------------------- |
| 보안                                       | Spring Security                   |
| 보안                                       | OAuth2 Client                     |
| DB                                         | MyBatis Framework                 |
| DB                                         | XXX Driver                        |
| 배치 처리<br> (대용량 + 반복된 작업 처리)  | Spring Batch                      |
| 배치 처리<br/> (대용량 + 반복된 작업 처리) | Quartz Scheduler                  |
| 메세징 처리                                | Spring for Apache Kafka           |
| 메세징 처리                                | Spring for RabbitMQ               |
| NoSQL or Session                           | Spring Data Redis (Access+Driver) |
| NoSQL or Session                           | Spring Data MongoDB               |
| NoSQL or Session                           | Spring Session                    |
| REST 관련                                  | Spring HATEOAS                    |
| REST 관련                                  | Rest Repositories                 |
| REST 관련                                  | Rest Repositories HAL Explorer    |
| 웹소켓                                     | WebSocket                         |

