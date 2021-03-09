MSA
===

<img src ="https://www.redhat.com/cms/managed-files/monolithic-vs-microservices.png"></img> <br>
출처 : redhat

<br>

### MSA란?

**MSA**(Microservice Architecture)는 애플리케이션 구축을 위한 아키텍처 기반 접근 방식이다.

**하나의 큰 애플리케이션을 여러 개의 작은 서비스(핵심 기능)를 조합하여 구현하는 방식이다.**

각각의 서비스는 독립적으로 작동하며 각 서비스는 느슨하게 연결되어 있다.

MSA는 애플리케이션 규모가 커짐에 따라 모놀리틱 아키텍처의 한계점이 있어서 많이 사용되고 있는 방식이다.

<br>

### 모놀리식 아키텍처

MSA는 흔히 모놀리식 아키텍처(Monolithic Architecture)와 많이 비교된다.

모놀리식 아키텍처란 일반적으로 애플리케이션을 구현할 때 많이 사용되던 방식으로, 
애플리케이션의 모든 구성요소를 통합된 형태로 구축하는 방식이다.

<br>

### MSA의 장단점

장점
- 출시 기간 단축 => 각 서비스가 독릭접으로 배포되기 때문에, 전체 애플리케이션을 배포하지 않고 부분적으로 업데이트 가능. <br>
- 높은 확장성 => 특정 요구사항에 대해 확장이 용이함. <br>
- 결함 격리 => 각 서비스들이 독립적이기 때문에 하나의 서비스에 문제 있을 때 다른 서비스에 영향을 주지 않음. <br>
- 손쉬운 배포 => 서비스의 규모가 작아졌기 때문에 배포에 따르는 우려가 없어짐.
- 향상된 개방성 => 서비스 별로 다른 기술 스택 사용 가능. => 이로인해 각 서비스에 적합한 기술을 사용 가능. <br>

단점
- 성능 => 서비스가 커짐에따라 서비스 간 통신 시간이 증가할 수 있음. <br>
- 구축 => 서비스 간 종속성을 파악하는데 시간을 투입해야함. <br>
- 복잡성 => 모놀리식 애플리케이션보다 각 서비스는 단순하지만 전체적으로 복잡함. <br>
- 테스트 => 통합 테스트뿐만 아니라 엔드-투-엔드 테스트 수행하기 어려움. <br>
- 버전 관리 => 업데이트로 인해 종속된 서비스가 손상되지 않도록 고려해야함. <br>
- 관리 => 마이크로 서비스에 성공하려면 성숙한 DevOps 문화가 필요함. <br>

<br>

### MSA의 동작 과정

(진행중..)

<br>

Reference
- https://www.redhat.com/ko/topics/microservices/what-are-microservices
- https://docs.microsoft.com/ko-kr/azure/architecture/guide/architecture-styles/microservices
- https://velog.io/@tedigom/MSA-%EC%A0%9C%EB%8C%80%EB%A1%9C-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-1-MSA%EC%9D%98-%EA%B8%B0%EB%B3%B8-%EA%B0%9C%EB%85%90-3sk28yrv0e
- ..