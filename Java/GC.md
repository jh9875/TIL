GC
===

<img src="../images/gc.png"></img> <br>

### Garbage Collection이란?

애플리케이션 실행 중 더 이상 사용하지 않는 동적으로 할당된 메모리에 대해 사용 가능한 자원으로 회수하는 것을 말한다. <br>
자바 애플리케이션을 실행할 때 JVM에서 Garbage Collection 작업을 수행한다. <br>
C나 C++과 달리 JVM에서 직접 메모리 관리를 해주므로 개발자가 직접 메모리를 관리할 필요가 없다.

GC가 발생하는 동안 JVM 애플리케이션이 멈춘다. 이것을 stop-the-world라고 부른다. <br>
stop-the-world가 발생하는 동안 GC를 수행하는 Thread를 제외하고 모든 Thread가 멈춘다. <br>
GC가 완료된 후 중단되었던 작업이 다시 시작된다. <br>
(애플리케이션의 성능을 높이기 위해서 stop-the-world 시간을 줄이기 위해 GC 튜닝을 한다고 한다..)


<br>

### GC 대상 메모리 영역

GC는 2가지 전제조건이 있다. <br>
- 대부분의 객체는 금방 접근 불가능 상태가 된다.
- 오래된 객체에서 젊은 객체로의 참조는 아주 적게 존재한다.

이러한 전제조건 하에 HotSpot VM에서는 Heap 영역을 크게 2가지로 나눈다. (HotSpot VM이란 JVM의 종류 중 하나로 가장 대표적인 JVM이다.)

- Young 영역 <br>
  새로 생성된 객체가 위치한 영역이다. 이 영역에서 객체가 사라질 때 Minor GC가 발생한다고 한다. <br>
  대부분의 객체는 금방 접근 불가능한 상태가 되기 때문에 Young 영역에 있다 사라진다.

- Old 영역 <br>
  Young 영역에서 살아남은 객체가 Old 영역으로 복사된다. 이 영역에서 객체가 사라질 때 Major GC가 발생한다고 한다.

<br>

### Young 영역의 구성과 동작 과정

Young 영역은 3개의 영역으로 나뉜다. <br>
- Eden 영역
- Survivor 영역 2개

Eden 영역은 새로 생성된 객체가 위치하는 영역이고, Survivor 영역 중 1개는 GC가 한번 실행된 후 살아남은 객체들이 위치한다. <br>
Survivor 영역이 가득 차면 다른 Survivor 영역으로 이동한다. <br>
이 과정을 반복하면서 살아남은 객체는 Old 영역으로 이동된다.

<br>

### 동작 과정 (Old 영역)

Old 영역은 데이터가 가득 차면 GC를 실행한다.

GC 방식은 JDK7 기준으로 다음과 같은 방식들이 있다. (설명은 생략..)

- Serial GC
- Parallel GC
- Parallel Old GC(Parallel Compacting GC)
- Concurrent Mark & Sweep GC (CMS)
- G1(Garbage First) GC


<br>

Reference
- https://d2.naver.com/helloworld/1329
- ..