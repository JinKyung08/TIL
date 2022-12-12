# Day 02

## -- Spring --

### ▷ Spring IoC

- IoC(Inversion of Controller)는 프로그램을 구동하는데 필요한 객체에 대한 생성, 변경 등의 관리를 프로그램을 구동하는 컨테이너에서 직접 관리하는 것을 말함
- 객체의 생성부터 생명주기까지 해당 객체에 대한 관리를 직접 수행



1. Spring IoC 컨테이너

- 스프링에서 관리하는 객체 - Bean(빈) (xml, 어노테이션)
- Bean Factory - 빈들을 관리한다는 의미
- IoC 컨테이너 역할
  - 객체의 생명주기와 의존성 관리
  - VO(DTO / POJO) 객체의 생성, 초기화, 소멸 등의 처리
  - 객체 생성을 컨테이너에 맡김으로써 소스 코드 구현 시간 단축
- IoC 컨테이너와 Bean 객체
  - **Bean(빈)** - 스프링이 IoC방식으로 관리하는 Class, 스프링이 직접 생성과 제어를 담당하는 객체
  - **Bean Factory (빈 팩토리)** - 핵심 컨테이너 , Bean 등록, 생성, 조회, 반환하는 기능 담당
  - ApplicationContext (애플리케이션 컨텍스트) - BeanFactory를 확장한 IoC 컨테이너, 등록하고 관리하는 기능은 BeanFactory와 동일하지만 스프링이 제공하는 각종 부가 서비스를 추가로 제공
  - GenericXmlApplicationContext - ApplicationContext를 구현한 Class, 일반적인 XML형태의 문서를 읽어 컨테이너 역할
  - Configuration metadata (설정 메타 정보) - ApplicationContext 또는 BeanFactory가 IoC를 적용하기 위해 사용하는 설정 정보, IoC 컨테이너에 의해 관리되는 Bean 객체를 생성하고 구성할 때 사용



### ▷ Spring DI

- DI(Dependency Injection)는 IoC 구현의 핵심 기술
- 컨테이너가 빈의 설정 정보를 읽어와 자동으로 해당 객체에 연결하는 것 의미
- 의존성을 주입 받게 되면 이후 해당 객체를 수정해야 할 상황이 생겼을 때 소스 코드의 수정을 최소화 할 수 있음
- DI 장점
  - 코드 단순
  - 각 객체 간의 종속 관계 (결합도) 해소 가능
- 단점
  - XML 써야함
- Spring DI 종류
  - Setter메소드를 통한 의존성 주입
    - Setter메소드를 통해 의존 관계가 있는 Bean을 주입하기 위해서는 \<property>태그 사용
  - 생성자를 통한 의존성 주입
    - Constructor를 통해 의존 관계가 있는 Bean을 주입하기 위해서는 \<constructor-arg>태그 사용
  - 메소드를 통한 의존성 주입