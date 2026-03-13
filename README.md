# C-Study
C++ 공부 기록용 Repository


## enum
- enum은 정수 열거형 자료형이고.. switch하고 쓸 때 궁합이 좋다 (왜냐하면 코드 가독성을 키우니까)
- 특히, C/C++에서는 매크로를 써서.. 상수를 정의할 수 있지만.. 이 경우에는 컴파일 과정에서 추적이 힘드므로, 이때 const나 enum을 쓰기를 권장한다
  - 이 얘기의 여담으로 매크로 함수를 쓸 때도, 인라인 함수를 생각해주는 것이 좋다
- enum과 switch를 쓰기에 앞서서.. FSM을 설계하고 이를 시각적으로 그려두면 도움이 되겠지..?
- 또한.. enum의 경우 자칫 남발하면 중복으로 인한 충돌이 발생할 수 있으므로 클래스 enum이 C++에서는 권장되고 있음

'''
// ex
enum class Color
{
    Red,
    Blue
};
Color c = Color::Red;
'''


## noexcept
- 함수의 예외사항을 고려하지 않음을 명시하는 것
- 만약 예외상황 발생시 std::terminate()으로 프로그램 exit(1)!


## RAII (Resource Acquisition Is Initialization)
- 자원의 생성과 해제를 객체의 생명주기에 맡긴다
- 즉, 자원의 할당은 생성자가, 해제는 소멸자에게 맡기는 것..


## extern 키워드
- 만약 하나의 변수나 객체를 다른 소스들에서도 사용하고 싶은 상황에서 사용한다
- 이 경우.. 헤더에서 선언을 해준다
- 정의를 제공하지 않는 전역 선언에만 extern을 사용하는 것이 C++의 권장


## 소스 extern vs 헤더 extern
- 소스 extern: 그저 다른 파일의 변수를 참조할 때 사용
- 헤더 extern: 공유 전역 변수 선언 시에 사용 (general purpose)
##
