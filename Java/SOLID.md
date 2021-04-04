SOLID
===

### SOLID란?

SOLID란 객체지향 설계에서 지켜야 할 5가지원칙을 말한다.
- **S**RP
- **O**CP
- **L**SP
- **I**SP
- **D**IP

시간이 지나도 **유지 보수**와 **확장이 쉬운 시스템**을 만들고자 할 때 이 원칙들을 적용해서 설계한다.

소스 코드를 읽기 쉽고, 확장이 쉽게 리팩터링 할 때 SOLID 원칙을 적용할 수 있다.

<br>

### Single Responsibility Principle (단일 책임 원칙)

단일 책임 원칙이란 하나의 소프트웨어 설계 부품 (클래스, 함수 등)은 하나의 책임만을 가져야 하는 원칙이다. 여기서 말하는 책임은 기능, 역할 정도로 해석하면 된다.

SRP 원칙을 잘 지키면 클래스마다 기능이 잘 분배되어 있고, 하나의 클래스에 변화가 생길 때 다른 클래스에 영향을 최소화할 수 있다.

즉 응집도를 높게, 결합도를 낮게 설계할 수 있다.

만약 하나의 클래스에 책임이 많아진다면 다른 클래스들과 강하게 결합될 가능성이 있다.

<br>

### Open - Closed Principle (개발 - 폐쇄 원칙)

<br>

### Liskov Substitution Principle (리스코프 치환 원칙)

<br>

### Interface Segregation Principle (인터페이스 분히 원칙)

<br>

### Dependency Inversion Principle (의존관계 역전 원칙)



<br>


Reference
- https://ko.wikipedia.org/wiki/SOLID_(%EA%B0%9D%EC%B2%B4_%EC%A7%80%ED%96%A5_%EC%84%A4%EA%B3%84)
- https://victorydntmd.tistory.com/291
- https://velog.io/@lsb156/%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5-%EA%B0%9C%EB%B0%9C-5%EB%8C%80-%EC%9B%90%EC%B9%99-SOLID
- https://velog.io/@kyle/%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5-SOLID-%EC%9B%90%EC%B9%99-%EC%9D%B4%EB%9E%80
- https://dev-momo.tistory.com/entry/SOLID-%EC%9B%90%EC%B9%99
