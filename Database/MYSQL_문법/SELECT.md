SELECT
===

### 기본 문법

~~~SQL
SELECT 필드이름
FROM 테이블 이름
[WHERE 조건]
[ORDER BY 조건]
[GROUP BY 조건]
[HAVING 조건]
[LIMIT]
~~~

- SELECT : 원하는 열을 선택
- FROM : 원하는 테이블을 선택
- WHERE : 원하는 조건을 선택
- LIMIT : 데이터 조회 시 개수를 지정할 수 있음. <br>
  LIMIT n    => 상위 n개 행을 조회. <br>
  LIMIT n, m => n+1행부터 m개 행을 조회. <br>

- ETC <br>
  - ..
  - DISTINCT : 중복된 결과를 제거.
