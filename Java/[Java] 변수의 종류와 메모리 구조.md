## 전역, 지역, 클래스 변수를 자바의 메모리 구조와 관련해서 생각해보기


<img src="https://user-images.githubusercontent.com/33534771/74100794-00363c80-4b76-11ea-9616-2a819e6dcb4b.png" width="35%"/>


1. 메소드 영역

- 클래스에 대한 정보와 함께 클래스 변수(static variable)가 저장되는 영역. 
- JVM은 자바 프로그램에서 특정 클래스가 사용되면 해당 클래스의 클래스 파일(*.class)을 읽어들여, 클래스에 대한 정보를 메소드 영역에 저장한다. 

2. 힙 영역

- 모든 인스턴스 변수(멤버 변수)가 저장되는 영역.
- new 키워드를 사용해 인스턴스가 생성되면, 해당 인스턴스의 정보를 힙 영역에 저장한다. 
- 힙 영역은 메모리의 낮은 주소 -> 높은 주소의 방향으로 할당된다.

3. 스택 영역

- 메소드가 호출될 때, 메소드의 스택 프레임이 저장되는 영역.
- 메소드 호출 시, 메소드 호출과 관계되는 매개변수와 지역 변수를 스택 영역에 저장한다. 
- 스택 영역은 메소드의 호출과 함께 할당되며, 메소드의 호출이 완료되면 소멸한다.
- 스택 영역에 저장되는 메소드의 호출 정보를 **스택 프레임**이라고 부른다.
- 후입 선출의 구조를 갖고 있으며, 메모리의 높은 주소에서 낮은 주소의 방향으로 할당된다.



### [선언 위치에 따른 변수의 종류]

- 클래스, 지역, 인스턴스 변수가 있으며 선언된 위치에 따라 종류가 결정된다.

```java
public class Test{
  int iv; // 인스턴스 변수.
  static int cv; // 클래스 변수.
  
  void print(){
    int lv; // 지역 변수. 
  }
}
```

- iv, cv는 클래스 내부에 선언되어 있으므로 멤버 변수.
- cv는 static으로 선언되었으니 클래스 변수이고, iv는 인스턴스 변수.
- lv는 메소드 내에 선언되었으므로 지역 변수. 



1. 인스턴스 변수

- 인스턴스가 생성될 때, 생성된다. 따라서 인스턴스 변수를 사용하기 전에 먼제 객체를 생성해야 한다.
- 인스턴스 변수는 **독립적인 저장공간**을 가지므로 인스턴스 별로 다른 값을 가질 수 있다.
- 따라서 각 인스턴스마다 고유의 값을 가져야 할 때는 인스턴스 변수로 선언한다.
- `힙 영역`에 올라간다.

2. 클래스 변수

- `static` 키워드가 붙은 변수이다. 
- 클래스 변수는 **해당 클래스의 모든 인스턴스가 공통된 값을 공유**하게 된다.
- 따라서 한 클래스의 모든 인스턴스가 공통적인 값을 가져야할 때, 클래스 변수로 선언한다. 
- 클래스가 로딩될 때, 생성되어(그러므로 메모리에 딱 한번만 올라간다.) 종료될 때까지 유지되는 클래스 변수는 public을 붙이면 같은 프로그램 내에서 어디서든 접근 가능한 전역 변수가 된다.
- 인스턴스 생성 없이 접근할 수 있으므로 **클래스이름.클래스변수** 를 통해 접근할 수 있다. 
- `메소드 영역`에 올라가며, 주로 **공유의 목적**으로 사용한다.

3. 지역 변수

- 메소드 내에 선언되며 메소드 내에서만 사용할 수 있는 변수이다.
- 메소드가 실행될 때, 메모리를 할당받으며 메소드가 끝나면 소멸되어 사용할 수 없게 된다.
- `스택 영역`에 올라간다.
