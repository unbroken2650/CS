## 알고리즘

: 특정 작업을 수행하는 명령어들의 유한 집합

### 특성

-   입력 : 외부에서 제공되는 데이터가 있어야 함
-   출력 : 적어도 한 개의 결과 생성
-   명확성 : 명령이 명확하고 모호하지 않아야 함.
-   유한성 : 알고리즘대로 수행하면 어떤 경우에도 반드시 종료
-   유효성 : 실행가능 해야 함.

## 선택 정렬(Selection Sort)

: 정렬되지 않은 정수들 중에서 가장 작은 값을 찾아서 정렬된 리스트 다음 자리에 놓는다.

```C++
#include <iostream>
using namespace std;
void SelectionSort(int *a, const int n)
//a가 정렬할 수들이 있는 배열, n이 수의 개수
{
  for (int i = 0; i < n; i++){
    int j = i;
    for (int k = i+1; k < n; k++) {
      if (a[k] < a[j]) j = k;
      swap(a[i], a[j]);
    }
}
}
```

## 이원 탐색(Binary Search)

: 이미 정렬된 배열에서 특정 값을 찾는 것
![](https://i.imgur.com/KeSXwa5.png)

1. left = 0, right = n-1, middle = (left+right)/ 2로 설정 (배열의 index)
2. 가운데 값(m)을 찾고자 하는 값(x)과 비교하여
   2-1. m > x일 경우 right = middle - 1 (-1인 이유는 m!=x이기 때문에)
   2-2. m < x일 경우 left = middle + 1
   2-3. m == x일 경우 m의 index인 middle을 반환.

## 순환(Recursion)

: 수행이 완료되기 전에 자기 자신을 다시 호출
ex) BinarySearch

```C++
#include <iostream>
using namespace std;
int BinarySearch(int *a, const int x, const int left, const int right) {
  //a : 정렬된 수의 배열
  if(left <= right){
    int middle = (left + right ) / 2;
    if (x < a[middle]) return BinarySearch(a, x, left, middle - 1); // right = middle - 1
    else if (x > a[middle]) return BinarySearch(a, x, middle + 1, right); // left = middle + 1
    return middle;
  }
  return -1; //발견되지 않음
}
```

ex) 순열 생성기

```C++
#include <iostream>
using namespace std;
void Permutations(char *a, const int k, const int m) {
  //a : 수의 배열
  if (k==m) {//순열을 출력
    for (int i = 0; i <= m; i++) cout << a[i] << " ";
  } else {
    for (i = k; i <= m; i++) {
      swap(a[k], a[i]);
      Permutations(a, k+1, m);
      swap(a[k], a[i]);
    }
  }
}
```

## 표준 라이브러리(Standard Template Library, STL)
