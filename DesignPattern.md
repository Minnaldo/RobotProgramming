# 디자인패턴(DesignPattern)
## 디자인패턴이란?
  :객체 지향 프로그래밍 설계를 할 때 자주 발생하는 문제들을 피하기 위해 사용되는 패턴. <br>
  :소프트웨어를 설계할 때 특정 맥락에서 자주 발생하는 고질적인 문제들이 또 발생했을 때 재사용 할 수 있는 훌륭한 해결책 <br>
  :과거의 소프트웨어 개발 과정에서 발견된 설계의 노하우를 축적하여 그 방법에 이름을 붙여서 이후에 재사용하기 좋은 형태로 특정 규약을 만들어서 정리한 것 <br>
  :소프트웨어 설계에 있어 공통적인 문제들에 대한 표준적인 해법과 작명법을 제안하며, 알고리즘과 같이 프로그램 코드로 바로 변환될 수 있는 형태는 아니지만, 특정한 상황에서 구조적인 문제를 해결하는 방식
   즉, "효율적인 코드를 만들기 위한 방법론"이라고 생각하시면 됩니다. <br>
   
## 디자인 패턴 구조
- 콘텍스트(context) <br>
  :문제가 발생하는 여러 상황을 기술한다.  즉, 패턴이 적용될 수 있는 상황을 나타낸다. <br>
  :경우에 따라서는 패턴이 유용하지 못한 상황을 나타내기도 한다. <br>
- 문제(problem) <br>
  :패턴이 적용되어 해결 될 필요가 있는 여러 디자인 이슈들을 기술한다.  <br>
  :이때 여러 제약 사항과 영향력도 문제 해결을 위해 고려해야 한다.  <br>
- 해결(solution)  <br>
  :문제를 해결하도록 설계를 구성하는 요소들과 그 요소들 사이의 관계, 책임, 협력 관계를 기술한다. <br>
  :해결은 반드시 구체적인 구현 방법이나 언어에 의존적이지 않으며 다양한 상황에 적용할 수 있는 일종의 템플릿이다. <br>

## 디자인 패턴의 분류
<img src="./img/DesignPattern_Kind.PNG" width = 60%><br>**디자인 패턴의 종류**</img>
1. 생성(Creational) 패턴 <br>
  - 객체 생성에 관련된 패턴 <br>
  - 객체의 생성과 조합을 캡슐화해 특정 객체가 생성되거나 변경되어도 프로그램 구조에 영향을 크게 받지 않도록 유연성을 제공한다.
2. 구조(Structural) 패턴 <br>
  - 클래스나 객체를 조합해 더 큰 구조를 만드는 패턴 <br>
  - 예를 들어 서로 다른 인터페이스를 지닌 2개의 객체를 묶어 단일 인터페이스를 제공하거나 객체들을 서로 묶어 새로운 기능을 제공하는 패턴 <br>
3. 행위(Behavioral) 패턴 <br>
  - 객체나 클래스 사이의 알고리즘이나 책임 분배에 관련된 패턴 <br>
  - 한 객체가 혼자 수행할 수 없는 작업을 여러 개의 객체로 어떻게 분배하는지, 또 그렇게 하면서도 객체 사이의 결합도를 최소화하는 것에 중점을 둔다. <br>

## 디자인 패턴의 종류
i. 생성(Creational) 패턴 <br>
  - 추상 팩토리(Abstract Factory) <br>
    : 구체적인 클래스에 의존하지 않고 서로 연관되거나 의존적인 객체들의 조합을 만드는 인터페이스를 제공하는 패턴 <br>
  - 팩토리 메서드(Factory Method) <br>
    : 객체 생성 처리를 서브 클래스로 분리해 처리하도록 캡슐화하는 패턴 <br>
  - 싱글턴(Singleton) <br>
    : 전역 변수를 사용하지 않고 객체를 하나만 생성하도록 하며, 생성된 객체를 어디에서든지 참조할 수 있도록 하는 패턴 <br>
    -> ex) 다크모드를 사용할 때, 페이지가 넘어가도 다크모드가 유지되도록 전역 변수가 아닌, 객체를 하나만 생성하여 생성된 객체를 어디서든 참조하여 사용한다.
    
<br>
ii. 구조(Structural) 패턴  <br>
  - 컴퍼지트(Composite) <br>
    : 여러 개의 객체들로 구성된 복합 객체와 단일 객체를 클라이언트에서 구별 없이 다루게 해주는 패턴 <br>
  - 데커레이터(Decorator) <br>
    : 객체의 결합을 통해 기능을 동적으로 유연하게 확장할 수 있게 해주는 패턴 <br>
 
 iii. 행위(Behavioral) 패턴
   - 옵저버(Observer) <br>
     : 한 객체의 상태 변화에 따라 다른 객체의 상태도 연동되도록 일대다 객체 의존 관계를 구성하는 패턴 <br>
   - 스테이트(State)  <br>
     : 객체의 상태에 따라 객체의 행위 내용을 변경해주는 패턴
   - 스트래티지(Strategy)
     : 행위를 클래스로 캡슐화해 동적으로 행위를 자유롭게 바꿀수 있게 해주는 패턴
     -> ex) 검색할 때, [전체, 이미지, 뉴스, 지도] 중 하나를 눌러 모드를 선택하여 검색의 방식이 결정되도록 할 때.
         즉, 프로그램 실행 중 모드가 바뀔 때마다, 검색이 이뤄지는 방식,,  즉. 전략이 수정된다는 것!
        => 각각 버튼 들바다 onClick 으로 다른 메소드를 실행한다고 가정할 때,
   - 템플릿 메서드(Template Method)
     : 어떤 작업을 처리하는 일부분을 서브 클래스로 캡슐화해 전체 일을 수행하는 구조는 바꾸지 않으면서 특정 단계에서 수행하는 내역을 바꾸는 패턴
   - 커맨드(Command)
     : 실행될 기능을 캡슐화함으로써 주어진 여러 기능을 실행할 수 있는 재사용성이 높은 클래스를 설계하는 패턴
