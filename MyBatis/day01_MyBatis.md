# Day 01

## -- My Batis --

### ▷ Framework 

- 클래스 묶음이나 뼈대, 틀을 제공하는 라이브러리를 구현해놓은 것
- 장점
  - 개발시간 ↓
  - 일정 수준 이상의 품질
  - 유지보수 쉬움
- 단점
  - 개발자들의 능력 ↓ 스스로 개발 어려워짐
  - 습득 시간 오래 걸림
- 종류
  - 영속성 Framework - MyBatis ,ORM ,Hibernate
    - 데이터의 저장, 조회, 변경, 삭제를 다루는 클래스 및 설정 파일을 라이브러리화하여 구현
  - 자바 Framework  - Spring Framework, 전자정부표준 Spring, Struts
    - Java EE를 통한 웹 애플리케이션 개발에 초점을 맞춰 필요한 요소들을 모듈화해 제공
  - 화면구현 Framework  - Bootstrap, Foundation, MDL
    - Front-End를 보다 쉽게 구현할 수 있게 틀 제공
  - 기능지원 Framework - Log4j, JUnit 5, ANT
    - 특정 기능이나 업무 수행에 도움을 줄 수 있는
      기능 제공



### ▷ MyBatis

- 데이터의 입력, 조회, 수정, 삭제(CRUD)를 보다 편하게 하기 위해 xml로 구조화한 Mapper설정파일을 통해 JDBC를 구현한 영속성 프레임 워크
- MyBatis API Site : http://www.mybatis.org/mybatis-3/ko
- mybatis-config.xml
  - \<configuration> : 최상위 태그를 작성하고 내부에 필요한 설정 작성
  - \<properties>태그 : 외부 properties파일의 내용을 불러 올 때 사용
  - \<settings>태그 : MyBatis구동 시 선언할 설정 작성
  - \<typeAliases> 태그 : MyBatis에서 사용할 자료형의 별칭 선언
  - \<environments>태그 : MyBatis에서 연동할 DataBase 정보 등록
  - \<mappers>태그 : 사용하고자 하는 쿼리문이 정의된 mapper파일 등록

- POOLED 와 UNPOOLED 차이점
  - POOLED
    - 최초 Connection객체를 생성할 때 정보를 pool영역에 저장해두고 Connection객체를 생성할 때 이를 재 사용함
    - 장점 : DB연결 시간 단축
    - 단점 : 단순한 로직을 수행하는 객체를 만들기에는 설정해야 할 정보가 많음
  - UNPOOLED 
    - Connection객체를 별도로 저장하지 않고 객체 호출 시 매번 생성하여 사용
    - 장점 : Connection연결이 많지 않은 코드를 작성할 때 간단하게 구현 가능
    - 단점: 속도 느림 (그래서 잘 안씀)

- mapper

  - \<resultMap>태그 : 조회한 결과를 객체와 Row간의 1:1 매칭이 아닌 원하는 객체의 필드에 담아 반환하고자 할 때 사용

  - \<select>태그 : SQL의 조회구문을 작성 할 때 사용되는 태그, 해당 쿼리를
    외부에서 접근하고자 할 때 namespace.id명을 적어 접근가능

  - id : 구문을 찾기 위해 사용될 수 있는 네임스페이스 내 유일한 구분자

  - parameterType : 구문에 전달될 파라미터의 클래스 명(패키지 경로 포함)이나 별칭

  - resultType : 리턴되는 타입의 패키지 경로를 포함한 전체 클래스 명이나 별칭,

    collection인 경우 list, arraylist로 설정 가능

  - resultMap : 리턴되는 타입의 필드 명이 다를 때 사용하며 직접 이름을 지정하여 매칭

  - \<insert>, \<update>, \<delete> 태그 - 해당 태그들은 설정 동일



- SqlSession을 통한 쿼리 실행
  - selectOne(String mapper,Object param) - 하나의 객체만을 받고자 할 때 사용
  - selectList(String mapper,Object param) - 결과에 대한 값을 List로 받고자 할 때 사용
  - selectMap(String mapper,Object param, String mapKey) - 결과에 대한 값을 Map으로 받고자 할 때 사용
  - insert(String mapper, Object param), update, delete -  DB에 데이터를 입력하고자 할 때 사용



### ▷ MyBatis 동적 SQL

- 지원 구문 종류
  - if
  - choose(when, otherwise)
  - trim(where,set)
  - foreach
  - bind 구문