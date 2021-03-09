RESTful API란?
===


### REST란?

**REST**는 월드 와이드 웹과 같은 분산 하이퍼미디어 시스템을 위한 *소프트웨어 아키텍처*의 한 형식이다.

REST는 웹에 존재하는 자원에 대해 주소를 지정하여 활용하는 방법을 일컫는다.

여기서 말하는 자원은 DB에 있는 데이터, 이미지 등을 의미한다. 주소는 URI를 의미한다.

HTTP 메서드를 통해 자원에 접근(CRUD 연산) 할 수 있다.

HTTP 메서드는 다음과 같이 있다.

- Create : 생성 (POST)
- Read : 조회 (GET)
- Update : 수정 (PUT)
- Delete : 삭제 (DELETE)

<br>

### REST의 구성

- 자원 : URI
- 행위 : HTTP Method
- 표현 : 자원에 대한 행위는 HTTP Method로 표현

<br>

### REST 아키텍처 제약 조건

- Client–server architecture : <br>
  자원을 가진 쪽이 서버, 자원을 요청하는 쪽이 클라이언트이다. <br>
  서버와 클라이언트를 구분함으로써 각 역할이 명확해지고, 의존성이 줄어든다.

- Statelessness : <br>
  서버는 클라이언트의 각 요청에 대해 상태를 저장하면 안 된다.

- Cacheability : <br>
  클라이언트는 응답을 캐싱 할 수 있다.

- Layered system : <br>
  서버는 다중 계층으로 구성될 수 있다. <br>
  서버와 클라이언트 사이에 proxy 또는 load balancer 등 중간 서버를 두어도 영향을 주지 않는다.

- Uniform interface : <br>
  일관성 있는 인터페이스로 분리되어야 한다.

- Code on demand (optional) : <br>
  서버는 실행 가능한 코드를 전송하여 클라이언트의 기능을 일시적으로 확장하거나 사용자 정의할 수 있다.

<br>

### RESTful API는?

RESTful은 REST라는 명사에 ~ful 이란 접미사를 붙여 만든 단어이다.

~ful은 명사 뒤에 붙여서 그것이 가진 성질, 특성을 가진 형용사를 만든다.

즉 RESTful API는 REST의 성질, 특성을 가진 API이다. 다르게 말하면 REST 아키텍처의 원칙을 지키며 설계된 API인 것이다.

<br>

### 잘 설계된 RESTful API란?



<br>

### RESTful API의 장단점



<br>


