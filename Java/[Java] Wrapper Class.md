## Wrapper Class



기본 자료형을 객체 타입의 자료형으로 변환이 필요할 때 주로 사용한다. 



- 사용 용도
  - 객체로 저장해야 할 경우.
  - 매개변수로 객체가 요구될 경우(ex. 제네릭, Collection의 타입)
  - 객체 간의 비교가 필요할 경우
  - 제네릭이나 컬렉션에서 사용할 경우, 기본형을 쓸 수 없기 때문에 이를 Wrapping한 형태를 사용해야 한다. 

- 특징
  - 산술 연산을 위한 클래스가 아니기 때문에 `Immutable`하다.(불변)
  - 불변 객체이기 때문에 값에 대한 변경은 불가능하고 새로운 값(객체)의 할당이나 참조만 가능하다.
  - Boxing : 기본 자료형 -> Wrapper Class
  - UnBoxing : Wrapper Class -> 기본 자료형
  - JDK 1.5부터 오토 박싱, 오토 언박싱을 지원한다.
  - 언박싱 시 사용되는 메소드는 다음과 같은 형태를 갖는다.
    - intValue : 객체 -> int 값으로 변환. 



문자를 숫자로 바꾸거나, 숫자를 문자를 바꿀 때 두 가지 방식의 차이점이 존재한다.

[Code]

```java
// 문자열 -> 기본형
int number1 = Integer.parseInt("100");

// 문자열 -> wrapper class
Integer number2 = Integer.valueOf("100");
```



위에서 언급했듯이, JDK 1.5부터 오토 박싱과 오토 언박싱이 지원되기 때문에 반환값이 기본형이든, wrapper class이든 차이가 없어졌다. 그래서 굳이 구별하지 않고 `valueOf()`를 사용해도 된다. 



단, 성능을 비교하면 valueOf()가 조금 더 느리다고 한다. 

