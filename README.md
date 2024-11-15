# 2주차 Study [ 2024-11-11 ~ 2024-11-15 ]

**[ 목표 ]**
- 이번주 목표 : c/c++ 기본 개념 잡기
-----

**[ 진행 사항 ]**

2주차 진행하면서 c/c++ 기본 개념이 제대로 안잡혀 있다는것을 느꼈으며, 그리하여 이번주에는 기본 개념을 잡는 시간을 가질려고 배웠던것도 다시 배우는 복습 형식과 새로운것을 배우는 방식으로 개념 잡아볼려고 합니다.

- 이번주내내 감기로 인하여 공부시간이 길지 않았었습니다.

[ C ]


[ C++ ]

* 프로그램의 텍스트 기본적으로 소스파일과 헤더 파일로 구성된다
- [ 소스 파일 ] : .c .cpp .cxx .cc 등등
- [ 확장자 ] : h. .hh . hpp .hxx .hh 등등

주석 처리
/* 을 시작해서 */ 으로 끝을 내면 그 안에 있는 내용은 프로그램과 상관 없는것으로 컴파일러는 간주
한라인 주석 처리 : //

프로그램의 텍스트와는 별도로 컴파일이 진행되기 전 소스 파일에 필요한 사항들을 먼저 처리하는 전처리(Preprocessing) 작업이 실행 된다. #include 사용

ex)<br>
// main.pp<br>
// 전처리 지시문 : 코드에 사용되는 파일을 포함시킴<br>
#include <iostream><br>

int var = 0; //변수 선언 및 초기화<br>

int main()<br>
{<br>
  var = 100; //**정수 리터럴**을 연산자 =을 사용해 변수에 대입<br>
  std::cout<<"Hello !";<br>
  return 0; //return **키워드 사용**<br>
}

[ 정수 자료형 ]
signed : **부호를 갖는**(0을 포함한 양수/음수 구분) 변수 선언, 일반적으로 unsigned 없이 변수를 선언하면 signed 자료형이다.

unsigned : 음수를 사용하지 않겠다.

둘의 가장 큰 차이는 음수를 표현할 수 있는가 없는가 이다. 

[ 텍스트 구분 ]
식별자(Identifiers) : 일련의 문자(**영어 문자셋**)와 숫자로 이루어져 변수나 함수의 이름을 나타냄.
키워드(Keywords) : 미리 정해져 있는 식별자(**if, for, return** 등등)
연산자(Operators) : 숫자 연산(**+,-,*,/** 등등)에 사용됨, 연산자는 우선순위를 가짐.
리터럴(Literals) : 정수, 소수 또는 문자 같은 일정 상수값을 나타내는 것.

[ 변수 ]
**객체(Object)** : 메모리와 격체와 연결시켜서 객체의 의미를 일정의 메모리를 차지하는 것으로 정의한다.
**타입(Type)** : 객체의 일정의 메모리를 확정되기 위해 크기가 정해져야할때 이것을 타입을 통해 결정되고 타입은 객체의 주요 특징이 된다.
**수명(storage duration)** : 메모리 점유를 프로그램이 끝날 때까지 유지할지 아니면 해당 객체가 사용이 완료되면 메모리를 해제할지와 관련도니 메모리의 수명도 객체의 특징이 된다.
**선언(declaration)** : 객체 사용을 위해서는 타입과 함께 식별자 이름으로 선언을 해야한다
**변수(variable)** : 객체를 지정하는 것을 변수 라고 한다 객체는 변순의 선언을 통해서 생성되고 또한 동적으로 메모리 할당하는 new 연산자를 통해서도 가능하고 임시 객체의 방식으로도 객체가 생성된다.

[ 기본 타입 ]
기본 타입으로는 **char, int, bool, float, double** 등이 있고 타입별로 크기가 다르다.

* 문자(character) 타입
한 문자를 저장하는 char 타입은 부호의 결정에 따라 signed char, unsigned char 그리고 char 형태로 쓰이며 모두 문자 1바이트(byte)를 저장한다. char타입으로 사용할 때 일반적으로 signed char 타입을 가지는데 시스템에 따라서 unsigned char 타입을 가질 수 있다.

범용 문자 세트를 저장하는 wchar_t char8_t char16_t 그리고 char32_t 타입이 있고 이것은 부호를 결정하는 타입이 아니기 때문에 singed, unsigned을 같이 사용할 수 없다.

* 정수(integer) 타입
정수 타입의 대표적인 **int** 타입으로 부호 있는 정수 타입 지정자(type-specifiers) 인 signed 에 따라 short int, int, long int, long long int 형태를 가진다 signed를 명시하지 않아도 동일하게 처리된다. 또한 signed char 타입을 사용해서 정수 타입을 나타낼 수 있다. 여기서 short, long은 int 타입에서 특수 목적으로 사용되는 타입 지정자로서 int 타입의 기본 크기를 변경시킨다. 단독으로 short나 long 타입으로 사용되면 각각 short int, long int타입으로 처리된다.

[ 네임 스페이스 ]
변수나 함수를 선언할 때 다른 소스 파일에 같은 이름으로 선언될 수 있는 경우에 하나의 영역으로 정계를 두어 서로 영향을 주지 않고 독립적으로 잰재하도록 선언하는 것을 **네임스페이스(namespace)**라고 한다.

네임스페이스의 정의는 **전역 범위** 또는 **네임스페이스 내에서만** 허용 된다. 함수처럼 일정 블록 내에서 선언을 하면 에러가 발생한다.

//네임스페이스 선언
namespace A{<br>
  int i;<br>
  double d;<br>
}

int var = A::i; //네임스페이스에서 선언된 데이터에 접근. 범위 지정자 사용

// 네임스페이스 다시 선언, A 네임스페이스 안에는 위에 선언된 변수와 함수가 들어가게 됨<br>
namespace A{<br>
  void f();<br>
}

