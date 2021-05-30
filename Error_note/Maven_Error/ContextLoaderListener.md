ContextLoaderListener
===

Maven을 사용하다보면 springframework.web.context.contextloaderlistener 에러가 뜰때가 있다.

이런 문제는 Maven - Update Project를 하면 가끔씩 Maven Dependencies 설정이 날아갈 수 있다고 한다.

해결 방법은..

1. 프로젝트 우클릭
2. properties
3. Deployment Assembly
4. Add를 클릭
5. Java Build Path Entires
6. Maven Dependencies 선택 후 Apply

<br>


Reference
- https://jaeu0608.tistory.com/155
- ..