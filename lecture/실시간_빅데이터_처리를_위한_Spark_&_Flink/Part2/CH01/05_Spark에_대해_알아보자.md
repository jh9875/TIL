Spark에 대해 알아보자
===

### Apache Spark가 무엇일까
Apache Spark는 빅데이터 처리를 위한 오픈소스 고속 분산처리 엔진이다.

<br>

### 하둡 에코시스템
크게 3가지 파트를 가짐.

- HDFS : 파일 시스템
- Map Reduce : 연산 엔진
- Yarn : 리소스 관리

여기서 Apache Spark는 연산엔진을 대체하는 프로젝트

<br>

### 빠른 스파크
스파크 특징 => 빠르다 <br>
메모리 계층간 속도는 L1캐시 ~ RAM, HDD/SDD 중 L1으로 갈수록 빠르다. <br>
높은 메모리 계층에서 처리할 때 빠르게 처리할 수 있는데, 계층이 올라갈수록 메모리 용량이 적어지므로 빅데이터의 경우 무리가 있다. => <br>
해답 : 데이터를 쪼개서 여러 노드의 메모리에서 동시에 처리. (분산 처리) <br>
> 빅데이터의 In-Memory 연산

<br>

### Spark Cluster
스파크는 하나의 클러스터를 이룸.
- Driver Program : Task를 만들고 정의를 하게되는 일을 함. (Script, Python, Java, Scala 등..)
- Cluster Manager : 일거리 분배 (Hadoop => Yarn, AWS => Elastic MapReduce)
- Worker Node : 연산 (1CPU 코어 당 1Node 배치)

<br>

### 그래도 빠른 스파크
1개의 노드에선 Pandas와 Spark를 비교했을 땐 비교적 느릴 수 있다. => Spark는 확장성을 고려해서 설계했기 때문 <br>
Pyspark는 수평적 확장이 가능하다. <br>

Hadoopt MapReduce보다 메모리 상에선 100배, 디스크 상에선 10배 빠르다.

**Lazy Evaluation** : <br>
태스크를 정의할때는 연산을 하지 않다가 결과가 필요할때 연산한다. <br>
=> 기다리면서 연산 과정을 최적화 할 수 있다.

<br>

### 스파크의 핵심 데이터 모델
Resilient Distributed Dataset (RDD)
- 여러 분산 노드에 걸쳐서 저장
- 변경이 불가능
- 여러 개의 파티션으로 분리