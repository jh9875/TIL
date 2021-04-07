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

단일 책임 원칙이란 하나의 **소프트웨어 설계 부품 (클래스, 함수 등)은 하나의 책임**만을 가져야 하는 원칙이다. 여기서 말하는 책임은 기능, 역할 정도로 해석하면 된다.

SRP 원칙을 잘 지키면 클래스마다 기능이 잘 분배되어 있고, 하나의 클래스에 변화가 생길 때 다른 클래스에 영향을 최소화할 수 있다.

즉 응집도를 높게, 결합도를 낮게 설계할 수 있다.

만약 하나의 클래스에 책임이 많아진다면 다른 클래스들과 강하게 결합될 가능성이 있다.

<br>

### Open - Closed Principle (개방 - 폐쇄 원칙)

소프트웨어 구성 요소는 **확장에 열려**있으나, **변경에는 닫혀**있어야 한다는 원칙이다. 즉, 기존의 코드는 변경하기 않고(Closed) 기능을 수정 및 추가(Opne) 할 수 있도록 해야 한다는 원칙이다.

이 원칙을 지키기 위해서 **추상화**를 이용하는 방법이 있다.

**변경되지 않는 핵심 개념**은 interface로 만들고 자주 변경될 수 있는 개념은 interface를 상속받아서 구현하면 된다.

ex)
~~~java
interface playAlgorithm {
	public void play();
}
class Wav implements playAlgorithm {
	@Override
	publci void play() {
		System.out.println("Play Wav");
	}
}
class Mp3 implements playAlgorithm {
	@Override
	public void play() {
		System.out.println("Play Mp3");
	}
}

class SoundPlayer {
	private playAlgorithm file;

	public void setFile(playAlgorithm file) {
		this.file = file;
	}
	public void play() {
		file.play();
	}
}

public class Client {
	public static void main(String[] args) {
		SoundPlayer sp = new SoundPlayer();
		sp.setFile(new Wav());
		sp.setFile(new Mp3());
		sp.play();
	}
}
~~~
코드 출처 : https://dev-momo.tistory.com/entry/SOLID-%EC%9B%90%EC%B9%99

<br>

### Liskov Substitution Principle (리스코프 치환 원칙)

자식 클래스는 부모 클래스에서 가능한 행위를 수행할 수 있어야 한다는 원칙이다.

자식 클래스가 부모 클래스를 대체하기 위해서는 부모의 기능에 대해 override 하지 않도록 해야 된다. <br>
즉, 자식 클래스는 부모 클래스의 기능을 재정의 하지 않고 확장만 수행하도록 해야 된다.

<br>

### Interface Segregation Principle (인터페이스 분리 원칙)

사용하지 않는 인터페이스는 구현하면 안 된다.

하나의 일반적인 인터페이스보다, 여러 개의 구체적인 인터페이스가 낫다. <br>
즉 ISP 원칙은 **인터페이스의 단일 책임**을 강조한다.

<br>

### Dependency Inversion Principle (의존관계 역전 원칙)

의존관계를 맺을 때, 구체화에 의존하면 안 된고 추상화에 의존해야 한다.

<img src ="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=http%3A%2F%2Fcfile2.uf.tistory.com%2Fimage%2F9993CF4D5BF7A8290F9519">

이미지 출처 : https://victorydntmd.tistory.com/291

 <br>

위 이미지처럼 Client가 Cat, Dog, Bird보다 추상적인 Animal과 관계를 맺어야 한다.

<br>


Reference
- https://ko.wikipedia.org/wiki/SOLID_(%EA%B0%9D%EC%B2%B4_%EC%A7%80%ED%96%A5_%EC%84%A4%EA%B3%84)
- https://victorydntmd.tistory.com/291
- https://dev-momo.tistory.com/entry/SOLID-%EC%9B%90%EC%B9%99
- https://velog.io/@lsb156/%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5-%EA%B0%9C%EB%B0%9C-5%EB%8C%80-%EC%9B%90%EC%B9%99-SOLID

