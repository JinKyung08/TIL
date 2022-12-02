# DAY 08

## -- JSP --

### ▷ JSP Action Tag

- 기존의 JSP문법을 확장하는 매커니즘을 제공하는 태그

- 표준 액션 태그

  - JSP페이지에서 바로 사용
  - JSP에서 기본으로 제공하는 태그

  - <jsp:   />
  - jsp:include - 특정 페이지를 포함할 때 사용
    - jsp파일이 java파일로 바뀌고 컴파일이 완료되어 런타임 시 삽입
  - jsp:forward - (request.forward()와 동일) , 페이지 이동
  - jsp:param
  - jsp:useBean
  - jsp:setProperty
  - jsp:getProperty

- 커스텀 액션 태그

  - 별도의 라이브러리 설치 필요

  - <c:      />



### ▷ EL

- Expression Language의 약자로 JSP 2.0버전에서 추가 됨
- ${ value }  == <%=  %>

**1. EL 내장객체**

- pageScope
- requestScope

- sessionScope
- applicationScope

- param
- paramValues
- header
- headerValues

- cookie

- initParam
- pageContext



### ▷ JSTL

- Standard Tag Library
- 공통으로 사용하는 코드의 집합을 사용하기 쉽게 태그화 하여 표준으로 제공한 것

**1. 태그 종류**

- Core Tags - 변수와 url, 조건문, 반복문 등의 로직과 관련된 JSTL문법 제공
- Formatting Tags - 메시지 형식이나 숫자, **날짜** 형식과 관련된 포맷 방식 제공
- Function - trim, substring과 같은 여러 문자열 처리 함수 제공

**2. Core Tags**

- \<c:set>

  - 초기 값은 반드시 기술
  - \<c:set>으로 선언한 변수는 EL 식 안에서 사용 가능

  - JSP <% %>같은 스크립틀릿 요소에서는 사용 불가능

- \<c:set> scope 속성

  - scope속성을 이용하면 page영역 뿐만 아니라 request, session, application 영역에 속성 저장 가능 (미 설정 시 기본 값은 page)

- \<c:out>

- \<c:if>

  - if문과 비슷한 역할을 하는 태그 (else X 없음)

    - ex) <c:if test=“${num1 > num2}”>
      		num1이 더 큽니다.

      ​		\</c:if>

- \<c:choose>
  - switch문과 비슷 
  - \<c:when>, \<c:otherwise>태그와 함께 사용

- \<c:forEach>
  - 자바의 for, for-in문에 해당하는 기능 제공
  - var - 현재 반복 횟수에 해당하는 변수 이름
  - begin - 반복이 시작할 요소 번호
  - end - 반복이 끝나는 요소 번호
  - items - 반복할 객체 명(Collection 객체)
  -  step -  증감할 값
- \<c:forEach>의 varStatus
  - 상태 값 명.current -  현재 반복 회수
  - 상태 값 명.index - 반복 라운드의 제로기반 인덱스
  - 상태 값 명.count - 반복 라운드의 1 기반 인덱스
  - 상태 값 명.first - 현재 라운드가 반복을 통한 첫번째임을 의미
  - 상태 값 명.last - 현재 라운드가 반복을 통한 마지막 번째임을 의미

**3. JSTL Formatting Tags**

- \<fmt:formatNumber>
  - 표현하고자 하는 숫자의 포맷을 통화 기호, ‘,’ 표시, % 표시 등 원하는 쓰임에 맞게 지정 가능
  - maxIntegerDigits 및 minIntegerDigits의 속성으로 표시하고자 하는 수의 단위 표현 가능
  - maxFractionalDigits 및 minFractionalDigits의 속성은 소수 자릿수를 지정할 수 있음

- \<fmt:formatDate>
  - 날짜나 시간의 포맷 방식을 지정하여 화면에 보여줄 때 사용 
  - java.util.Date()객체를 사용해야 함
- \<fmt:setLocale>
  - 지역 설정을 통해 통화 기호나 시간 대역을 다르게 설정 가능

**4. JSTL Function**

- 문자열 처리에 관한 메소드들을 EL형식에서 사용할 수 있게 하는 라이브러리

- ${fn:메소드 명(문자열)}

