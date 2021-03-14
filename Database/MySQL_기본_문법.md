MySQL 기본 문법
===

<img src="../images/mysql.png"></img> <br>

### 데이터 정의어 (DDL)

- CREATE : 데이터베이스 또는 테이블을 생성할 때 사용. <br>
  - 기본 형태 <br>
    - 데이터베이스 생성할 때 <br>
	  ~~~SQL
	  CREATE DATABASE 테이터베이스이름;
	  ~~~
    - 테이블 생성할 때 <br>
	  ~~~SQL
	  CREATE TABLE 테이블이름
	  (
		  필드이름1 필드타입1,
		  필드이름2 필드타입2,
		  ...
	  )
	  ~~~
  - 예제 <br>
	..

- ALTER <br>
- DROP <br>
- RENAME <br>

<br>

### 데이터 조작어 (DML)
데이터베이스 사용자가 응용 프로그램이

- SELECT : 테이블의 레코드를 선택할 때 사용. <br>
  - 기본 형태 <br>
	~~~SQL
	SELECT 필드이름1, 필드이름2, ..
	FROM 테이블이름
	[WHERE 조건]
	~~~
  - 옵션 <br>
    - 필드 정렬
  
- INSERT <br>
- UPDATE <br>
- DELETE <br>

<br>

### 데이터 제어어 (DCL)

- GRANT <br>
- REVOKE <br>

<br>

### 트랜잭션 제어어 (TCL)

- COMMIT <br>
- ROLLBACK <br>
- SAVEPOINT <br>

<br>

### 집계 함수

...

<br>

Reference
- http://www.tcpschool.com/mysql/intro