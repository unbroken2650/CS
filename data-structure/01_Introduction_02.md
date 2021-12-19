## C++ 프로그램의 구성

### 파일의 종류

-   헤더 파일 : .h 또는 .hpp 확장자 / 선언 저장에 사용
-   소스 파일 : .cpp 확장자 / 소스 코드 저장에 사용

### 프로그램의 실행

컴파일 -> 링크 -> 적재(로드)

### 영역(Scope)

-   파일 영역 : 함수 정의에 속하지 않은 선언, 클래스 정의, 네임스페이스
-   네임스페이스 영역
    ! 네임스페이스 : 논리적으로 연관된 변수나 함수를 한 그룹으로 만드는 기법
-   지역 영역 : 블록 안에서 선언된 이름
-   클래스 영역

### C와 다른 점

-   입출력 : <<, >> 사용
-   연산자 다중화(Operator Overloading) 사용
-   시스템 정의 헤더 파일인 <code>iostream</code>이 필요

```C++
#include <iostream>
```

-   <code>std</code> : 클래스이고, cin, cout 등의 함수를 올바르게 쓰기 위해 필요하다.

```C++
#include <iostream>
using namespace std;
```

-   <code>cin, cout</code> : 입출력을 위해 사용, 여백으로 입출력값을 구분

```C++
#include <iostream>
using namespace std;
int main(){
    int a, b;
    cin >> a >> b;
    cout << a << " " << b << endl;
}
//a와 b 두 숫자를 입력받고 "a b" 형태로 출력하는 코드
```

-   <code>new, delete</code> : 원하는 타입의 객체를 생성하고 포인터를 반환 / 기억 장소를 다시 반환
