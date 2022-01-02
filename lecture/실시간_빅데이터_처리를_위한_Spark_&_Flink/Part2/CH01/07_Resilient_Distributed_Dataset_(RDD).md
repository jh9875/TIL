Resilient Distributed Dataset (RDD)
===

### RDD 란
Resilient Distributed Dataset => 탄력적인 분산 데이터셋

<br>

### RDD 생성
SparkContext <br>
ex)

```Python
sc = SparkContext

..

lines = sc.textFile()
```

여기서 로딩된 파일이 담긴 lines객체가 RDD

RDD는 텍스트 파일이나 <br>
JDBC, Cassandra, Elasticsearch, JSON, CSV 등 다양하게 불러올 수 있다.

<br>

### RDD의 특징

1. 데이터 추상화
	데이터 클러스터에 흩어져 있지만 하나의 파일인 것처럼 사용이 가능하다. <br>
	ex) 위 코드에서 데이터가 여러 노드에 담겨있을때 하나의 객체에 담아서 사용할 수 있다.
2. Resilient & Immutable (탄력적 & 불변)
   여러 데이터 노드 중 하나가 망가진다면? 네트워크 장애, 하드웨어 / 메모리 문제 등 여러 가지 문제가 발생할 수 있다.

   데이터가 Immutable하면 복원이 가능해진다. <br>
   이유 : 예를 들어 RDD1에서 RDD2로 변환할 때 Immutable하면 RDD1이 RDD2로 바뀌는게 아니라 새로운 RDD2가 만들어진다. => 변환을 거칠때마다 연산의 기록이 남는다. (RDD의 변환 과정은 하나의 비순환 그래프로 그릴 수 있게 된다.)
3. Type-sage
   컴파일시 Type을 판별할 수 있어 문제를 일찍 발견할 수 있다. (개발자 친화적)
4. Unstructured / Structured Data를 동시에 다룬다.
   - Unstructured : 텍스트 데이터 (로그, 자연어 ..)
   - Structured : 테이블 데이터 (RDB, DataFrame)
5. Lazy
   게으르다 -> 결과가 필요할때까지 연산을 하지 않는다. <br>
   연산은 변환과 액션 두 가지 종류가 있다. <br>
   액션을 할때까지 벼노한은 실행되지 않는다. => Lazy Evaluation

   Spark Operation = Transform + Action

<br>

### 왜 RDD를 쓸까
- 유연하다
- 짧은 코드로 할 수 있는게 많다.
- 개발할때 무엇보다는 어떻게에 대해 더 생각하게 한다 (how-to)
  - 게으른 연산 덕분에 데이터가 어떻게 변환될지 생각하게 된다.
  - 데이터가 지나갈 길을 닦는 느낌