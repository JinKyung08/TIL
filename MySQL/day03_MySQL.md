# DAY 03

## -- MySQL --

### ▷ view 

- 가상 테이블, 물리적으로 저장된 테이블이 아니라 논리적으로 만들어진 가상의 테이블



### ▷ 하위쿼리( sub query)

- 부속질의 
- 쿼리문안에 또 쿼리문이 들어 있는 것
  - 스칼라 부속질의 : select 절에 오면
  - 인라인 뷰 부속질의 : from 절에 사용
  - 하위절( sub query) : where문에 사용
    - =, <=, >, <, <> -> 한개 값만 처리 할수 있음
    - 값들이 많을때 and조건, or조건 사용
    - or 조건 : any 
    - and 조건 : all
    - =any(서브쿼리) = in(서브 쿼리)



\* 집계함수 

  - where에 사용할 수 없음 ,where 절에서 쓰려면 서브쿼리 이용
    - sum(열이름) : 합계
      avg(열이름) : 평균
      max(열이름) : 최댓값
      min(열이름) : 최솟값
      count(*) : null을 포함한 개수
      count(열이름) : null을 제외한 개수
      count(distinct) : 중복을 제거한 개수

- select 열이름 ,...
  from 테이블명
  where 조건
  group by 열이름
  having group by의 조건
  order by 열이름 [ desc | asc]
  - having : group by의 조건을 해결하기 위해 사용



### ▷ JOIN

- 두 개 이상의 테이블을 서로 묶어서 하나의 결과 집합으로 만들어 내는 것

- inner join(내부조인)

  - 양쪽 테이블에 모드 내용이 있는 것만 조인되는 방

    - select 열이름,...

      from 첫번째 테이블명 별명
      		inner join 두번째 테이블명 별명  //inner 생략가능
              on 조인조건 
       where 검색조건;

    \* 열이름이 한쪽 테이블에만 있으면 열이름만 사용가능

    단,  여러 테이블을 사용할 때는 반드시 테이블명(별명).컬럼명

  - 3개 테이블 조인 (다대다)

    - select 열이름,...

      from 첫번째 테이블명 별명
      		inner join 두번째 테이블명 별명 
                  on 조인 조건 

      ​        inner join 세번째 테이블명 별명

      ​			on 조인 조건

       where 검색조건;

- outer join(외부조인)
- cross join(상호조인)