Java 정규표현식
===

### Java에서 정규표현식 사용

Java에서 정규표현식을 사용할 때 java.util.regex 패키지 안에 있는 Pattern 클래스와 Matcher 클래스를 주로 사용.

<br>

### Pattern 클래스

정규표현식을 사용하기 위해 Pattern 클래스의 인스턴스로 컴파일 되거나, Pattern 클래스의 matches() 메서드를 사용하면 <br>
대상 문자열이 정규표현식에 맞는지 확인할 수 있음.

주요 메서드
- static Pattern compile(String regex) <br>
  주어진 정규표현식으로부터 패턴을 만들어낸다.

- static Matcher matcher(CharSequence input) <br>
  원하는 패턴을 찾는 Matcher 객체를 만든다.

- static boolean matches(String regex, CharSequence input) <br>
  주어진 정규표현식에 입력이 부합되는지 확인한다.

- String pattern() <br>
  컴파일된 정규표현식을 String으로 반환한다.

- ..

<br>

### Matcher 클래스

특정 문자열이 주어진 패턴과 일치하는지 판별할 때 사용.

주요 메서드
- boolean find() <br>
  주어진 문자열에서 특정 패턴을 찾아낸다.

- boolean matches() <br>
  주어진 문자열 전체가 특정 패턴과 일치하는지 판단한다.

- boolean lookingAt() <br>
  주어진 문자열이 특정 패턴으로 시작하는지 판단한다.

- int start() <br>
  일치한 문자열의 시작 index를 반환한다.

- int end() <br>
  일치한 문자열의 마지막 index를 반환한다.

- ..

<br>

### 사용 예제
~~~java
// Pattern 클래스의 matches 사용 예
public boolean patternMatches(String regex, String target) {
	return Pattern.matches(regex, target);
}

// Pattern 클래스의 compile 사용 + Matcher 의 find 사용 예
public boolean patternCompile(String regex, String target) {
	Pattern pattern = Pattern.compile(regex);
	Matcher matcher = pattern.matcher(target);

	return matcher.find();
}
~~~

<br>


Reference
- https://coding-factory.tistory.com/529
- https://ktko.tistory.com/entry/JAVA-%EC%9E%90%EB%B0%94%EC%9D%98-%EC%A0%95%EA%B7%9C%ED%91%9C%ED%98%84%EC%8B%9D-Pattern-Matcher
- https://mparchive.tistory.com/45
- ..