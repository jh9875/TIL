CI/CD
===

<img src ="https://www.redhat.com/cms/managed-files/ci-cd-flow-desktop_1.png"></img> <br>
출처 : redhat


<br>

### CI란?

CI란 Continuous Intergration의 약자로 **지속적인 통합**을 말한다.

여기서 말하는 지속적인 통합이란 여러 개발자들이 동일한 애플리케이션의

각기 다른 기능을 개발한 새로운 코드 변경 사항을 정기적으로 빌드 및 테스트하고 공유 repository로 통합하는 것을 말한다.

<br>

CI를 성공적으로 구현할 경우 애플리케이션 통합 과정에서 버그를 신속하게 찾아 해결하고 여러 코드가 충돌할 수 있는 문제를 해결할 수 있다.

<br>

### CD란?

CD란 Continuous Delivery 또는 Continuous Deployment의 약자로 **지속적인 서비스 제공** 또는 **지속적인 배포**를 말한다.

여기서 말하는 지속적인 서비스 제공이란 공유 repository에 자동으로 Release 하는 것을 말한다.

지속적인 서비스 제공을 구축하기 위해선 CI가 먼저 구축되어 있어야 한다.

<br>

여기서 말하는 지속적인 배포란 애플리케이션을 production으로 Release 하는 작업을 자동화하는 것을 말한다.

지속적인 배포를 성공적으로 구현할 경우 애플리케이션에 변경사항을 적용한 후 몇 분 이내에 애플리케이션을 자동으로 실행할 수 있는 것을 의미한다.

<br>

### CI/CD의 목적 (+ 결론)

CI/CD의 목적은 개발 단계를 자동화함으로써 애플리케이션을 보다 짧은 주기로 고객에게 제공하기 위해서이다.

<br>
<br>


참고 자료 :
- https://www.redhat.com/ko/topics/devops/what-is-ci-cd
- https://artist-developer.tistory.com/24
- https://itholic.github.io/qa-cicd/