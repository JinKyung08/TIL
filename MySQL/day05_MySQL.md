# DAY 05

## -- MySQL --

### ▷ JDBC (Java Database Connectivity)

- 자바에서 데이터베이스에 접속할 수 있도록 하는 자바 API

- java.sql 패키지

  

1. DriverManager

- jdbc driver를 관리
- db와 연결해서 Connection 구현 객체 생성

2. Connection

- Statement, PreparedStatement, CallableStatement 구현 객체를 생성
- 트랜잭션 처리및 db연결을 끊을 때 사용

3. Statement

- SQL의 ddl 과 dml을 실행할 때 사용
- 주로 변경되지 않는 정적 sql문을 실행할 떄 사용

4. PreparedStatement

- SQL의 ddl 과 dml을 실행할 때 사용
- 매개변수화된 sql문을 사용할 수 있기 때문에 편리성과 보안성이 좋음 

5. CallableStatement

- 스토어드 프로시저와 스토어드 함수

6. ResultSet

- DB 에서 가져온 데이터를 읽을 때 사용 

==================================================

- 접속

  - 자바코드 -> JDBC interface -> JDBC Driver -> 

    DBMS가 설치된 컴퓨터의 IP주소

    DBMS가 허용하는 포드(port)번호 : 3306, DBMS로 연결하기 위해

    사용자(DB계정) 및 비밀번호 : 셀제로 사용할 DB이름

    사용하고자 하는 DB이름 : 인증하기 위해

     

- DB연결

  - JDBC Driver를 메모리로 읽어오기(로딩)

  - class.forName("com.mysql.cj.jdbc.Driver");

    없으면 예외발생 : ClassNotFoundException

  - db 연결 : getConnection(url, user, password)

  ~~~
  ex)
  package boardtest;
  
  import java.sql.Connection;
  import java.sql.DriverManager;
  
  public class ConnectionExam {
  	public static void main(String[] args) {
  		Connection conn = null;
  		String url = "jdbc:mysql://localhost:3306/jdbctest?characterEncoding=UTF-8&serverTimezone=UTC";
  		//jdbc:mysql:  => jdbc 사요하는 dbms가 mysql이다.
  		//localhost : ip주소(== 127.0.0.1), 내컴퓨터, 원력으로 연결할 때 : ip주소 쓰기
  		//3386 => 포트번호, 들어오는 입구
  		//jdbctest : 데이터베이스명
  		
  		String user = "test";  //사용자(계정), root, ...
  		String password = "1234";  //암호
  		
  		try {
  			//JDBC driver 등록,메모리에 로딩, Build path에서 찾고 메모리로 로딩(읽어들이기)
  			Class.forName("com.mysql.cj.jdbc.Driver");
  //			Class.forName("com.mysql.jdbc.Driver");
  			
  			//db 연결하기
  //			conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/jdbctest","test","1234");
  			conn = DriverManager.getConnection(url,user,password);
  			
  			System.out.println("연결 성공");
  			}
  ~~~

  

- executeUpdate() : insert, update, delete
- executeQuery() : select	
- execute() : 저장프로시저(스토어드 프로시저), 저장함수(스토어드 function)