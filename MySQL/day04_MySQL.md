# DAY 04

## -- MySQL --

### ▷  JOIN

- OUTER JOIN (외부조인)
  * left outer join 
  * right outer join

### ▷ ALTER

- alter table 테이블명
  		
- drop column 열이름
    	add 열이름 데이터타입  [not null  : null]
  	  modify column 열이름 데이터타입   / change에러 뜰때 modify로
    	change column 열이름 변경할이름 데이터타입 [not null  : null]
  	  drop primary key;  -- 기본키 삭제

### ▷ SUB QUERY

- 스칼라 부속질의 : select절
- 인라인 뷰 : from 절
- 하위질의 (서브쿼리,중첩질의) : where 절

### ▷ 스토어드 프로시저 (Stored Procedure)

- 쿼리문의 집합
- 일괄처리하기 위한 용도로 사용
- 하나의 요청으로 여러 SQL문을 실행 가능 네트워크 소요 시간을 줄일 수 있음 ,보수성이 뛰어남
- 개발 업무를 구분하여 개발할 수 있다. 

~~~
형식)
    delimiter $$  -- //, \\ 끝을 새롭게 정의 / 어떤걸 써도 상관없음 -- sql에서 문장의 끝은 ;
    create procedure 스토어드프로시저명 (in or out 파라미터)
    begin 
    
		sql 프로그래밍 코딩
    
    end $$
    delimiter;
    
    call 스토어드프로시저명(); -- sql문을 사용할 수 있도록 끝의 정의를 ;으로 바꿔줌
~~~



### ▷ 스토어드 함수 (Stored Function)

- 사용자가 직접만들어 사용하는 함수 
- return 값을 가짐
  - 단 하나의 값만 리턴
-  프로시저 처럼 in, out을 사용할 수 없음 
- select 문장 안에서 호출 
- 주로 테이블을 조회시 사용
-  스토어드함수 쓰기전에 함수 생성할 수 있는 권한을 부여해야함
  - set global log_bin_trust_function_creators = 1;

### ▷ 트리거 (Trigger)

- dml(insert, update, delete) 이벤트가 발생했을 때 자동으로 처리되게 하는 개체

- view테이블에는 트리거 부착 안됨

- 직접 실행할 수 없음

- 테이블에서 insert,update,delete가 발생할 때 자동으로 실행

-   for each row   -- 모든 행 처리 

- old.기존컬럼명 / old 테이블 - update 또는 delete가 수행되기 전의 데이터가 잠깐 저장되어 있는 임시테이블

   