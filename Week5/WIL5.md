5주차 내용 정리

구조적 프로그래밍 언어에서 가장 중요한 것 = 함수 -> D&C (Divide&Conquer) - 중복 제거, 논리의 분할을 위해

사람이라는 분류(Class) 안에 객체(Object)는 속성(property)와 행위(method)를 가지고 있음

- 클래스 vs 객체 -> 붕어빵을은 붕어빵을 만드는 팩터리. => 클래스는 분류에 대한 개념(실체X), 객체는 실체 (ex. 사람 - 클래스, 유재석 - 객체)

객체 = 세상에 존재하는 유일무이한 사물 = 클래스의 인스턴스(클래스를 통해서 object를 만들었다는 것을 강조할 때)
클래스 = 분류. 집합. 같은 속성과 기능을 가진 여러 객체를 총칭하는 개념

-객체 지향의 4대 특성 = 캡(캡슐화)! 상(상속) 추(추상화)다(다형성)! - 클래스와 객체를 통해서 구현됨

캡슐화 = 정보은닉
상속 = 재사용
추상화 = 모델링
다형성 = 사용편의

1. 추상화 = 모델링 = 구체적인 것을 분해해서 관찰자가 관심 있는 특성만 가지고 재조합하는 것 = 구체적인 것을 분해해서 관심영역(애플리케이션 경계)에 있는 특성만 가지고 재조합 하는 것 = 자바의 class 키워드 -> 결과 : 모델 -> 자바에서는 클래스 (상속을 통한 구체화, 추상화. 인터페이스를 통한 추상화. 다형성을 통한 추상화도 넓게 보면 포함 가능)

모델 = 추상화를 통해 실제 사물을 단순하게 묘사

클래스와 객체의 관계 표현(새로운 객체 하나 생성해 그 객체의 주소값(포인터)를 객체 참조 변수에 할당) : 클래스(객체 참조 변수의 자료형) 객체*참조*변수(생성된 객체를 참조할 수 있는 변수) =(할당문) new 클래스(); (클래스의 인스턴스 = 객체를 색성하기 위해 객체 생성자 호출)

클래스 모델 표현하는 국제 표준 표기법 = UML 클래스 다이어그램 -> 모델링 -> 논리적 설계(개발환경에 영향을 받지 않는 설계) -> 물리적 설계(개발 환경에 맞춰진 설계)

객체가 생성되어야만 속성의 값을 저장하기 위한 메모리 공간이 힙영역에 할당(스태틱X. 클래스의 인스턴스), 밑줄의 유무 -> 클래스의 멤버 메서드(유) vs 객체의 멤버 메서드(무)

자바에서 포인터는 객체 참조 변수에 할당됨

객체참조변수.객체속성 -> 객체의 속성에 접근 가능('.'은 참조 연산자)

스태틱 - 스태틱 영역에 올라간 정보는 main() 메서드 시작 전에 올라가서 main() 메서드 종료된 이후에 내려옴 -> 단단히 고정되어있어서 스태틱 영역

클래스 멤버 vs 객체 멤버 = static 멤버 vs 인스턴스 멤버

객체 = 유일무이하게 존재하는 실체 -> 속성에 값 있음
클래스 = 개념, 분류체계 -> 속성에 값 X

클래서 멤버 속성 : 클래스 안의 모든 객체들에 공통된 속성 -> 클래스에 가지고 있어도 됨 -> static 키워드를 속성 앞에 -> T메모리의 스태틱 영역에 단 하나의 저장공간을 갖게 됨(클래스명.속성 , 객체참조변수.속성 둘 다 접근 O)

static x -> 객체 멤버 속성.
메서드도 static의 유무에 따라 클래스 멤버 메서드( ex. main() 메서드) vs 객체 멤버 메서드

클래스 멤버 - static 키워드와 함께 사용 + T메모리의 static 영역에 상주 -> static(정적) 멤버라고도 함 - 속성, 메서드
객체 멤버 - 객체가 클래스의 인스턴스 -> 인스턴스 멤버라고도 함 - 속성, 메서드

정적 메서드 - 객체들의 존재 여부에 관계없이 쓸 수 있음 (클래스에 속함, 클래스는 JVM 구동 시 T메모리의 스캐틱 영역에 바로 배치되기 때문) -> main() 메서드, getter(정적 변수에 대한 접근자 메서드), setter(설정자 메서드), 유틸리티성 메서드(인스턴스 만들지 않고 사용) -> UML 표기법에서는 밑줄을 사용해 표시

정적 속성 - 클래스 내부에 메모리 공간이 확보됨
객체 속성 - 속성명만 있고, 실제 메모리 공간 확보 X, 힙 영역에 객체 생성 시 각 객체 안에 멤버 속성을 위한 메모리 공간 할당.

필드 = 속성 = 프로퍼티
함수 = 히메서드
변수 공간 = 메모리 공간

스택 영역에 생기는 변수 = 지역 변수 -> 별도 초기화 하지 않으면 쓰레기 값이 있음
클래스 속성(전역 변수, 프로그램 어디서든 접근 O), 객체 속성(하나의 객체 안에서 다수의 객체 메서드가 공유하는 변수) - 별도 초기화 안해도 0, 0.0, false, null(객체)로 초기화됨
-> 지역변수는 한 지역에서만 사용하지만 멤버 변수는 공유 변수의 성격을 갖고 있기 때문에

객체 멤버 - 생성자를 통해, 정적멤버 - 정적 실행 영역을 통해 초기화. but 규정 X

2. 상속 : 재사용 + 확장 = 상위 클래스의 특성을 하위 클래스에서 상속(특성 상속)하고 거기에 필요한 특성울 추가 및 확장하여 사용 O
   -> 확장, 세분화, 슈퍼클래스 ㅡ 서브클래스의 개념(상위 클래스 ㅡ 하위 클래스. 상위 클래스 쪽으로 갈 수록 추상화, 일반화. 하위 클래스 쪽으로 갈 수록 구체화, 특수화.) -> 자바에서는 extends

"하위 클래스 IS A 상위 클래스" -> LSP(리스코프 치환 원칙)을 나타냄 => is a kind of

상위 클래스에서만 구현한 메서드를 모든 하위 클래스의 객체에서 사용이 가능, 최상위 클래스인 Object의 특성도 물려받음(toString() 메서드 사용 가능)

상속 = 상위 클래스의 특성 재사용 + 상위 클래스의 특성 확장 + is a kind of 관계 만족 (JAVA는 다중 상속 관계를 포기하고 인터페이스를 도입해 득을 취함)

인터페이스 = 구현 클래스 is able to 인터페이스(Java API - Serializable, Cloneable, Comparable, Runnable)

=> 상위 클래스는 특성이 풍부할수록(LSP-리스코프 치환 법칙), 인터페이스는 구현을 강제할 메서드의 개수가 적을 수록(ISP-인터페이스 분할 원칙) 좋음.

UML 표기법 - 하위 클래스 ㅡ> 상위 클래스, 클래스 ---> 인터페이스(점선 또는 막대사탕)

T메모리 구조 : 하위 클래스의 인스턴스 + 상위 클래스의 인스턴스 모두 함께 힙 영역에 생김 (+모든 클래스의 최상위 클래스인 object 클래스의 인스턴스도 함께 생성)

상위 클래스의 인스턴스로 객체 참조 변수를 생성시 하위 클래스의 메서드와 속성을 사용할 수 X
(형변환 연산, 암묵적 형변환)

3. 다형성 = 오버라이딩, 오버로딩 for 사용 편의성

오버 라이딩 = 같은 메서드 이름, 같은 인자 목록으로 상위 클래스의 메서드를 재정의(재정의하면 기존의 메서드는 가려짐, 상위 클래스 타입의 객체 참조 변수를 사용하더라도 하위 클래스에서 오버라이딩(재정의)한 메서드가 호출됨), 상위 클래스 타입의 객체 참조 변수에서 하위 클래스가 재정의한 메서드를 알아서 호출 -> 형변환, instanceof 연산자를 써서 하위 클래스가 무엇인지 신경 쓸 필요 X + 깔끔한 코드 유지

오버 로딩 = 같은 메서드 이름, 다른 인자 목록으로 다수의 메서드를 중복 정의

4. 캡슐화 = 정보 은닉
   UML에서 - : private, ~ : [default], # : protected, + : public, \_ : 정적 멤버(속성, 메서드)

접근 제어자

- 객체멤버(인스턴스 멤버)와 쓰일때
  public - 모두 접근 가능
  protected - 자신과 상속 관계에 있는 서브 클래스 접근 가능 + 같은 패키지면 접근 가능(한집)
  [default] - 같은 패키지 내의 클래스에서 접근 O
  private - 본인만 접근 가능

- 정적 멤버(클래스 멤버)와 쓰일 때
  클래스명.정적멤버 형식 접근 : 같은클래스, 같은 패지키, 다른 패키지, 상속 여부 상관 없이 전부 가능
  정적멤버 형식 접근 : 같은 클래스, 같은 패키지, 다른 패키지에서 상속 받았다면 사용 가능
  this.정적멤버 형식 접근 : 같은 클래스, 같은 패키지, 다른 패키지에서 상속 받았다면 사용 가능
  => 클래스명.정적멤버 형식으로 접근해야 일관적으로 접근이 가능(객체 생성한 경우 객체참조변수명.정적변수 형태로도 접근 가능)

-참조 변수의 복사
call by value = 값에 의한 호출, 값이 복사되며 두개의 변수는 서로 영향을 주지 않음 = 기본 자료형 변수 -> 저장하고 있는 값을 그 값 자체로 해석
call by reference (call by address) = 참조에 의한 호출, 객체가 저장하고 있는 객체 참조 변수를 복사 = 객체 참조 변수 -> 저장하고 있는 값 = 주소

둘 다 변수가 가진 값이 그대로 복사되지만, 그 값을 값 자체로 해석(기본 자료형 변수)하느냐 주소값(포인터)으로 해석(참조 자료형 변수)하느냐의 차이

Q. 객체지향 패러다임과 객체란?
패러다임 = 한 시대의 사람들의 견해나 사고를 근본적으로 규정하고 있는 인식의 체계. 또는, 사물에 대한 이론적인 틀이나 체계. 순화어는 `틀'
-> 객체지향 패러다임 = 객체지향적인 사고의 틀 -> 프로그램의 각 기능과 데이터를 객체로 바라보는 사고

객체 = 상태를 저장할 수 있는 자율적으로 행동하는 주체 -> 기본이 되는 단위 : class(ADT(추상 자료형) + 상속 + 다형성)
