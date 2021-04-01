JOIN
===

- INNER JOIN <br>
  두 테이블의 필드가 일치하는 레코드만 가져옴. <br>
  MySQL에서는 JOIN == INNER JOIN == CROSS JOIN을 의미. <br>
  ~~~SQL
  # on 절의 조건을 만족하는 데이터를 가져옴.
  SELECT ..
  FROM A
  INNER JOIN B
  ON A.id = B.id;

  # where 절에 조인 조건을 명시.
  SELECT ..
  FROM A, B
  WHERE A.id = B.id;
  ~~~

- LEFT (OUTER) JOIN <br>
  첫 번째 테이블을 기준으로 두 번째 테이블을 조합. <br>
  ~~~sql
  # A의 id와 B의 id가 일치하는 경우 두 테이블의 모든 필드를 가져옴.
  # 일치하지 않는 경우 B 테이블의 모든 필드를 NULL로.
  SELECT ..
  FROM A
  LEFT JOIN B
  ON A.id = B.id
  WHERE ..;
  ~~~

- RIGHT (OUTER) JOIN <br>
  LEFT JOIN의 반대.
  
- FULL OUTER JOIN <br>
  MySQL엔 FULL OUTER JOIN이 없음. <br>
  LEFT JOIN과 RIGHT JOIN을 이용해 사용할 수 있음.
  ~~~sql
  SELECT ..
  FROM A
  LEFT JOIN B
  ON A.id = B.id
  UNION
  SELECT ..
  FROM A
  RIGHT JOIN B
  ON A.id = B.id;
  ~~~


Reference
- http://www.tcpschool.com/mysql/mysql_multipleTable_join
- https://yoo-hyeok.tistory.com/98