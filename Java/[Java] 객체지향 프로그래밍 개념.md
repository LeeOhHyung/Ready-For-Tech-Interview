## 객체지향 프로그래밍

객체 지향 프로그래밍은 OOP(Object Oriented Programming)이라고도 한다.

프로그래밍에서 필요한 데이터를 추상화시켜 상태와 행위를 가진 객체를 만들고 그 객체들 간의 유기적인 상호작용을 통해 로직을 구성하는 프로그래밍 방법이다.



**[장점]**

- 코드의 재사용성이 높다.
  - 누군가가 만든 클래스를 가져와 사용할 수 있고 상속을 통해 확장할 수도 있다.
- 유지보수가 쉽다.
  - 수정해야 할 부분이 클래스 내부에 멤버 변수 혹은 메소드로 존재하기 때문에 해당 부분만 수정하면 된다.
- 대형 프로젝트에 적합하다.
  - 클래스 단위로 모듈화시켜서 개발할 수 있으므로 업무 분담하기가 쉽다.



**[단점]**

- 처리 속도가 상대적으로 느리다.
- 객체가 많으면 용량이 커질 수 있다.
- 설계 시 많은 노력과 시간이 필요하다.



## 객체 지향 프로그래밍의 특징

- 추상화

불필요한 정보는 숨기고 필요한 정보만을 표현함으로써 공통의 속성이나 기능을 묶어 이름을 붙이는 것이다.



- 캡슐화

속성과 기능을 정의하는 멤버 변수와 메소드를 클래스라는 캡슐에 넣는 것이다. 즉, 관련된 기능(메소드)과 속성(변수)을 한 곳에 모으고 분류하기 때문에 재활용이 원활하다.

목적 : 코드를 수정 없이 재활용하는 것

또한, 캡슐화를 통해 정보 은닉이 가능하다.



- 상속

부모 클래스의 속성과 기능을 그대로 이어 받아 사용할 수 있게 하고 기능의 일부분을 변경해야 할 경우, 상속 받은 자식 클래스에서 해당 기능만 다시 수정(정의)하여 사용할 수 있게 하는 것이다.

상속을 통해서 클래스를 작성하면 보다 적은 양의코드로 새로운 클래스를 작성할 수 있다. 

또한, 코드를 공통적으로 관리하여 코드 추가 및 변경이 용이하다.



- 다형성

하나의 변수명, 함수명 등이 상황에 따라서 다른 의미로 해석될 수 있는 것이다.

즉, 오버라이딩, 오버로딩이 가능하다.



## 객체 지향 설계 원칙

이와 관련된 내용은 심도 깊으나, 여기서는 간단하게 무엇을 의미하는지만 정리한다. 추후 추가 예정.

1. SRP(Single Responsibility Principle) : 단일 책임 원칙

클래스는 단 하나의 책임을 가져야 하며, 클래스를 변경하는 이유는 단 하나의 이유이어야 한다.

2. OCP(Open Closed Principle) : 개방 폐쇄 원칙

확장에는 열려있고, 변경에는 닫혀있어야 한다.

3. LSP(Liskov Substitution Principle) : 리스코프 치환 원칙

상위 타입의 객체를 하위 타입의 객체로 치환해도 상위 타입을 사용하는 프로그램을 정상적으로 동작해야 한다. 

4. ISP(Interface Segregation Principle) : 인터페이스 분리 원칙

인테퍼이스는 그 인터페이스를 사용하는 클라이언트를 기준으로 분리해야 한다.

5. DIP(Dependency Inversion Principle) : 의존 역전 원칙

고수준 모듈은 저수준 모듈의 구현에 의존해서는 안된다.



