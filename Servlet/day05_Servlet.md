# DAY 06

## -- Servlet --

### ▷ Filter

- javax.servlet.Filter인터페이스를 상속받아 구현하는 클래스
- HTTP요청과 응답 사이에서 전달되는 데이터를 가로채 서비스에 맞게 수정하는 필터링 작업을 수행할 수 있는 클래스
- ‘경유지’역할
- Request는 보안 관련 사항, 요청 헤더와 바디 형식 지정, 요청에 대한 log 기록 유지 등을 처리
- Response는 응답 스트림 압축, 응답 스트림 내용 추가 및 수정, 새로운 응답 작성 등 처리



- Filter Interface
  - init(FilterConfig config)
  - doFilter(ServletRequest req, ServletResponse res, FilterChain chain)
  - destroy()



### ▷ Wrapper

- 필터 클래스로부터 전달받은 데이터를 가공하여 다시 필터에게 반환하는 클래스

- HttpServletRequestWrapper - 요청한 정보를 변경하는 Wrapper클래스
- HttpServletResponseWrapper - 응답할 정보를 변경하는 Wrapper클래스