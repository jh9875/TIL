분산처리와 Latency
===

### 분산처리 문제

- 부분 실패 : 노드 몇 개가 프로그램과 상관 없는 이유로 인해 실패.
- 속도 : 많은 네트워크 통신을 필요로 하는 작업은 속도가 저하된다.

ex

```pyathon
RDD.map(A).filter(B).reduceByKey(C).task(100)
RDD.map(A).reduceByKey(C).filter(B).task(100)
```

위 두 코드 중 첫번째가 더 빠름. => <br>
reduceByKey 때문. <br> 
reduceByKey는 여러 노드에서 데이터를 불러오기 때문에 통신을 필요로 하는데 필터링을 거쳐 데이터 양을 줄인 뒤 reduceByKey를 하면 빨라진다.

