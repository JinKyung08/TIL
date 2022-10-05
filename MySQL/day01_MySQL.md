# DAY 01

## -- MySQL --

### ▷ DBMS (Database Management System)

**1. 데이터베이스 (Database, DB)**

- 데이터의 집합
- 데이터의 저장 공간 자체
- MySQL에서는 데이터베이스를 자료가 저장되는 디스크 공간(주로 파일로 구성됨)으로 취급

**2. DBMS (Database Management System)**

- 데이터베이스를 관히라고 운영하는 소프트웨어
- 다양한 데이터가 저장되어 있는 DB는 여러 명의 사용자나 응용 프로그램과 공유하고 동시에 접근이 가능해야함
- DBMS의 종류 : MySQL, MariaDB, MsSQL, Oracle,... / MySQL, MariaDB 거의비슷

**3. SQL (Structured Query Language) **

- DBMS에 데이터를 구축, 관리하고 활용하기 위해서 사용되는 언어(명령어)

- 에스큐엘, 시퀄

- 표준 SQL : 국제표준화 기구에서 SQL에 대한 표준을 정해서 발표

  /MySQL(sql), MsSQL(t-sql), Oracle(pl/sql) - > 표준과 함께 조금 변형

**- DB의 주요특징**

- 데이터 무결성
  - 데이터에는 오류가 X
- 데이터의 독립성
  - 데이터베이스의 크기를 변경하거나 데이터 파일의 저장소를 변경하더라도 기존에 작성된 응용 프로그램은 전혀 영향을 받지 않아야 한다.
- 보안
  - 데이터를 소유한 사람이나 데이터에 접근이 허가된 사람만 접근할 수 있어야 한다.
  - 데이터에 접근할 때도 사용자의 계정에 따라서 다른 권한을 가져야 한다.
- 데이터 '중복'의 최소화
  - 동일한 데이터가 여러 개 중복되어 저장되는 것을 방지
- 응용 프로그램 제작 및 수정이 쉬워짐
  - 기존 파일시스템을 사용할 때는 각각 파일의 포맷에 맞춰 개발해야 하는 응용 프로그램을 데이터베이스를 이용함으로써 통일된 방식으로 응용 프로그램 작성이 가능해지고, 유지보수 또한 쉬워진다.
- 데이터의 안전성 향상
  - 데이터의 백업 및 복원 기능을 이용함으로써 데이터가 깨지는 문제 발생시 원상으로 복원 또는 복구 방법이 명확해진다.

**4. DBMS(Relational DBMS) **

- 관계형 DBMS (RDBMS)

- 테이블(realation)이라는 최소단위로 구성

- 테이블은 한 쌍의 행(row)와 열(column)으로 구성

  \* relation - 릴레이션, Entity, 테이블

  relational database - 관계 데티어베이스

  relationship - 관계

**데이터베이스 구축**

**1. 일반 프로그램 단계 **

- 요구사항 -> 요구분석 -> 설계/* -> 구현(코딩) -> 테스트 -> 유지보수
- 폭포수 모델 : 프로젝트 계획 -> 업무 분석 -> 시스템 설계 -> 프로그램 구현 -> 테스트 -> 유지보수

**2. \**데이터베이스\**** / 정보처리기사 단골문제

- 요구사항/분석 -> 개념 모델링(설계)/ERD -> 논리 모델링(설계) /DBMS/정규화 -> 물리 모델링(설계) /반정규화/*-> 데이터베이스 구현

**\**3. 데이터베이스 구축**\**

- //데이터베이스 생성(방, 도서관)(create) -> 테이블 생성(use) //ddl-> // 데이터 입력/수정/삭제 (insert,update,delete-> 데이터 조회/활용(select) // dml

### ▷ *SQL(Structured Query Language, 구조적 질의어)

**1. DDL(Data Define Language, 데이터 정의어)**

- CREATE(생성), ALTER(변경), DROP(삭제)
- 관계 데이터베이스에서 사용될 테이블, 스키마, 도메인, 인덱스, 뷰 등을 정의(생성)하거나 수정, 제거 하기 위해 사용되는 언어

**2. DML(Data Manipulation Language, 데이터 조작어)**

- ELECT(검색), INSERT(삽입), DELETE(삭제), UPDATE(갱신)
- 데이터베이스 내의 자료를 실제 사용자가 이용(조작)하기 위한 언어

**3. DCL(Data Control Language, 데이터 제어어)**

- COMMIT(완료), ROLLBACK(되돌리기), GRANT(권한부여), REVOKE(권한회수)
- 관리자가 데이터의 보안, 무결성 유지, 병행제어, 회복 등을 하기 위해 사용하는 언어

### ▷ MySQL설치

- Mysql

  - localhost : 127.0.0.1 , 자신의 컴퓨터를 의미
  - 포트(방) : 3306 , 오라클(1521)
  - MySQL 인스턴스(instance) : MySQL 서버가 메모리상에서 실행 중인 상태/ mysql 프로그램이 컴퓨터에 활성화되어 백그라운드 서비스를 제공중인 상태
  - MySQL 서버 : 하드디스크에 설치된 프로그램

- cmd(명령프롬프트) 창에서 실행

  - mysql -u root -p

    \- mysql - u [username] - p;

   -또는 : 시작 - mysql - mysql command Line client-unicode

  > > show databases;
  > >
  > > > > create database testdb;
  > > > >
  > > > > > > use testdb;
  > > > > > >
  > > > > > > > > exit; -- 명령 창 종료

- 통합개발환경 GUI 환경에서 MySQL을 사용할 수 있음

- 환경설정([Edit] - [Preferences])

  [SQL Editor] : 오른쪽 맨 아래 의 체크 해제

  체크시 Updatd나 Delete 문의 조건에서 Primary Key가 설정된 열이 포함되어야 함

### ▷데이터베이스 구축

- DB생성 -> 테이블 생성 -> 데이터 입력 -> 데이터 조회/활용
- 주석
  - -- 주석글( 한줄 주석 )
  - /* 주석글(여러줄 주석)*/
- sql은 비절차적 언어
- sql은 대소문자 구분하지 않음

#### 1.DB 생성(방만들기)

- create database 데이터베이스명;

- ; : 문장이 끝났다는 의미, 반드시 넣어 주어야 함

- 실행 : Ctrl + Enter - 한 문장 단위

   Ctrl + Shift + Enter - 여러 문장(블록설정한 후) 단위

- 데이터베이스 사용 : use 데이터베이스명;

   새로 sql 실행할 때 마다 반드시 사용할 데이터베이스를 선택해야 함

\1) 데이터베이스 확인

- show databases;

\2) create 문

- creat 개체 만들개체이름;
- 개체 - 데이터베이스, 테이블, 뷰, 인덱스, 도메인,...

\3) 데이터베이스 제거

- drop 데이터베이스명;
- drop database if exists 지우려는 데이터베이스명;

#### 2. 테이블 생성

- 기본키 - primary key -중복X, null X

  unique - 중복 X ,null O

- 널값 허용하지 않음 not null

- 널값 허용 - null

- 정수

  - int - 4byte
  - smallint - 2byte
  - Integer

- 문자열, 문자

  - char(크기) - 문자열 ,문자 크기 정해짐 ex) 전화번호, 주민번호
  - varchar(크기) - 공간을 크게 확보하지만 쓰는 만큼만 / 쓰지 않는 건 메모리에 돌려줌 ex)주소

<details class="details-reset details-overlay details-overlay-dark" id="jumpto-line-details-dialog" style="box-sizing: border-box; display: block;"><summary data-hotkey="l" aria-label="Jump to line" role="button" style="box-sizing: border-box; display: list-item; cursor: pointer; list-style: none; transition: color 80ms cubic-bezier(0.33, 1, 0.68, 1) 0s, background-color, box-shadow, border-color;"></summary></details>

