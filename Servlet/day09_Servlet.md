# DAY 09

## -- Servlet --

###  ▷ AJAX(Asynchronous JavaScript and XML)

* JavaScript를 이용하여 **비동기식**으로 클라이언트와 서버가 데이터(XML)를 주고받는(통신) 방식

- 비동기식데이터
  - 클라이언트가 서버로 데이터 요청 후 응답을 기다리지 않고 다른 작업 수행 가능, 추후 응답이 오면 응답에 관련된 작업 진행
- 동기식 데이터 통신
  - 클라이언트가 서버로 데이터를 요청하면 응답이 올 때까지 다른 작업은 대기
- Ajax 특징
  - 일부분만 업데이트가 가능
  - 사용자에게 즉각적인 반응과 풍부한 UI경험 제공 가능
  - ActiveX나 플러그인 프로그램 설치 없이 이용 가능
  - Javascript방식, jQuery방식 (권장)으로 구현 가능
- 단점
  - 페이지 내 복잡도가 증가하여 에러 발생 시 디버깅이 어려움



- jQuery 방식

  ~~~
  $.ajax({
  		url : “요청이 전송되는 url이 포함된 문자열(필수 구현 속성)“
  		[, settings]
  });
  ~~~

  - 장점 - 구현 간단



### ▷ JSON (JavaScript Object Notation)

- 괄호 {} 내에 key:value 쌍으로 구성 → {“key”:value}

- Ajax통신에서 Object타입의 데이터 전송 시 XML대비 용량이 작고 속도가 빠름
- 핸들링 할 수 있는 라이브러리를 제공해 시스템 간 객체 교환에 용이



- GSON ( Google JSON)
  - Google에서 만든 오픈 라이브러리
  - JSON파일을 쉽게 읽고 만들 수 있는 메소드 제공
  - *toJson(Object, Appendable)