# Day 03

## -- Spring --

### ▷ Spring AOP

- 관점 지향 프로그래밍(Aspect Oriented Programming)의 약자

- 일반적으로 사용하는 클래스(Service, DAO 등)에서 중복되는 공통 코드 부분(commit, rollback, log 처리)을 별도의 영역으로 분리

- 소스 코드 중복을 줄이고 필요할 때마다 가져다 쓸 수 있게 객체화하는 기술

- 용어

  - Aspect
    - 부가 기능을 정의한 코드인 어드바이스(Advice)와 어드바이스를 어디에 적용할지 결정하는 포인트컷(PointCut)을 합친 개념
  - JoinPoint
    - 객체(인스턴스) 생성시점, 메소드호출시점, 예외발생지점등특정작업이시작되는시점
  - Advice
    - JoinPoint에 삽입되어 동작될 코드, 메소드
    - Before Advice - JoinPoint 앞에서 실행
    - Around Advice - JoinPoint 앞뒤
    - After Advice -JoinPoint - 호출이 리턴되기 직전
    - After Returning Advice -JoinPoint 메소드 호출이 정상적으로 종료된 후
    - After Throwing Advice -예외가 발생했을 때 실행

- 구조 정리

  - 기본구조 
    - 핵심기능 - 로그인, 회원가입
    - 부가기능 - 로그, 보안검사

- 특징

  - Spring은 Proxy기반 AOP를 지원
  - Proxy는 대상 객체의 호출을 가로챈다 (Intercept)
  - Spring AOP는 메소드 조인(패키지) 포인트만 지원
  - XML기반의 AOP 네임 스페이스를 통한 AOP 구현
  - @Aspect 어노테이션 기반 AOP 구현

- 구현방식 - XML

  - Advice를 정의하는 태그
    - \<aop:before>
    - \<aop:around>
    - \<aop:after>
    - \<aop:after-returning>
    - \<aop:after-throwing>
  - Advice를 정의하는 어노테이션
    - @Before("pointcut")
    - @Around("pointcut")
    - @After("pointcut")
    - @AfterReturning(Pointcut="",Returning="")
    - @AfterThrowing(Pointcut="",Returning="")

- JoinPoint

  - JoinPoint는 Spring AOP 혹은 AspectJ에서 AOP의 부가 기능을 지닌 코드가 적용되는 지점을 뜻
  - JoinPoint Interface 메소드
    - getArgs() - 메소드의 매개변수 반환
    - getThis() -현재 사용 중인 프록시 객체 반환
    - getTarget() -대상 객체 반환 
    - getSignature() -대상 객체 메소드 설명(메소드 명, 리턴 타입 등) 반환
    - toString() -대상 객체 메소드의 정보 출력

- Advice 작성

  ~~~
  import org.aspectj.lang.ProceedingJoinPoint;
  import org.springframework.util.StopWatch;
  
  public class AroundLog {
  	public Object aroundLog(ProceedingJoinPoint pp) throws Throwable{
  		String methodName = pp.getSignature().getName();
  		
  		StopWatch stopWatch = new StopWatch();
  		stopWatch.start();
  		
  		Object obj = pp.proceed();
  		stopWatch.stop();
  		
  		System.out.println(methodName + "() 메소드 수행에 걸린 시간 : " +
  		stopWatch.getTotalTimeMillis() + "(ms)초");
  
  		return obj;
  	}
  }
  ~~~

  