JVM
===

<img src="../images/JVM.png"></img> <br>

### JVM이란?

JVM(Java Virtual Machine)은 자바 가상 머신의 약자로 운영체제로부터 메모리를 할당받아 자바 기반 애플리케이션을 실행하는 역할을 한다.

JVM이 운영체제 위에서 동작하기 때문에 자바 기반 애플리케이션은 운영체제에 독립적이라는 장점이 있다.

<br>

### JVM 구성

- Class Loader <br>
  JVM으로 .class파일을 로드하고 ..

- Execution Engine <br>
- Garbage Collector <br>
- Runtime Data Area <br>

<br>

### JVM 메모리 구조

<br>

### JVM 실행 과정

1. 프로그램이 실행되면 JVM은 운영체제로 부터 필요한 메모리를 할당받는다. <br> 할당받은 영역은 용도에 따라 나누어 관리된다.
2. 자바 컴파일러(javac)가 자바 코드(.java)를 읽어 자바 바이트코드(.class)로 변환시킨다.
3. Class Loader를 통해 class파일들을 JVM으로 로딩한다.
4. 로딩된 class 파일들은 Execution engine을 통해 해석된다.
5. 해석된 바이트코드는 Runtime Data Areas에 배치되어 수행이 이루어진다.

<br>

Reference
- ..

