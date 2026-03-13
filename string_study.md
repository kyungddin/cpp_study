# CString

## Concept
- C++ MFC의 문자열 Class
- Windows와 MFC는 보통 TCHAR / wchar_t 기반 문자열을 사용
  - wchar_t: C++의 문자 타입으로 wide character (2 byte) 라는 뜻
  - TCHAR은 매크로로 ANSI에선 char, Unicode에선 wchar_t
    - 요즘 Windows에서는 TCHAR = wchar_t
- CString은 자동으로 LPCTSTR로 변환?
    - LPCTSTR = const TCHAR*
    - 따라서 CString과 Windows/MFC는 궁합이 좋다

## _T() 매크로
- 문자열 타입 자동 변환 매크로이다
- ex
'''cpp
CString str = _T("Hello");
'''
      
# std::String

## Concept
- C++의 STL 중 하나
- Char 기반으로 문자열을 생성 및 관리해주는 아주 좋은 클래스~
- 다만 Char 기반이므로 MFC에선 안 먹을 가능성이 높으다
