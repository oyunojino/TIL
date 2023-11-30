# Optional

## # 참고 자료

### Youtube : [Optional 이론편 [ 자바 (Java) 기초 ]](https://youtu.be/6aVlvJNb_1Y?si=t-uRKVMzh8OClDXO)

## # null이란

- null은 자바에서 제공하는 키워드
- 참조형 타입의 기본 값으로 사용
- null인 경우 할당되는 메모리 없음

## # NullPointerException

최대한 발생하지 않도록 조치해야하는 예외

### 예외가 발생하는 경우

- null 객체의 메소드나 필드를 접근하는 경우
- null을 throw하는 경우

### 예외를 피하는 방법

1. 참조 객체를 사용하기 전에 NPE를 방지하기 위해 null 체크 로직 추가  
   ( 코드량 ⬆️, 가독성⬇️ )
2. 객체 선언시 초기값 설정( 권장 )
3. Optional 사용( 2번째 방법 적용 후에 발생하는 예외도 처리 가능 )

## # Optional<T>

- java.util.Optional<T> -> JAVA 8버전부터 사용 가능
- null이 올 수 있는 참조객체를 감싸는 Wapper Class
- 클래스를 통해서 null을 안전하게 사용할 수 있게 기능 제공  
  EX ) Spring Data JPA에서 제공해주는 JPARepository

### 객체 선언

Optional 클래스로 사용하고자 하는 레퍼런스 타입을 삽입하여 선언  
EX )

```java

Optional<Sample> sample;
Optional<String> test;
```

### 객체 초기화

empty, of, ofNullable과 같은 메소드를 통해 구현할 수 있음

```java
// null 값으로 초기화
Optional<String> aaa = Optional.empty();
```

```java
// null 값이 아닌 경우
Optional<String> bbb = Optional.of("TEXT");
```

```java
// null 또는 객체가 있을 수 있는 경우
Optional<String> aaa = Optional.ofNullable(getText());
```

### 다양한 메서드 활용

| 메서드명        | 설명                                                                                 |
| --------------- | ------------------------------------------------------------------------------------ |
| filter          | predicate를 사용하여 해당값이 참이면 필터를 통과시킴                                 |
| map             | function을 사용하여 입력값을 다른 값으로 변환하는 기능을 제공                        |
| flatmap         |                                                                                      |
| isPresent       | 연산이 끝나고 객체가 존재하는지 확인하는 기능                                        |
| isEmpty         | isPresent와 반대로 객체가 존재하지 않으면 true를 리턴                                |
| ifPresent       | 연산을 끝내고 객체가 존재한다면 그 객체를 입력값으로 주는 기능                       |
| ifPresentOrElse |                                                                                      |
| get             | 최종적으로 나온 객체를 Optional에서 꺼내는 기능을 제공                               |
|                 | 객체가 존재하지 않는다면 예외 발생(isPresent 또는 ifPresent 같은 메서드로 검증 필요) |
| orElse          | 객체가 비어있다면 기본값으로 제공할 객체를 설정하는 기능                             |
| orElseGet       | orElse와 마찬가지로 객체가 비어있따면 기본값으로 제공할 객체를 지정하는 기능을 제공  |
|                 | orElse랑 차이를 보면 orElseGet은 실제 객체가 비어있을 때만 동작함                    |
