> ## 1. C++에서 출력하기
```c++
#include<iostream>
int main() {
	std::cout << "hello";
  //printf("hello")랑 똑같은 의미
}
```
* * *  
```c++
#include<iostream>
using namespace std;
int main() {
	cout << "hello";
	int a, b, c;
	cin >> a >> b;
	c = a + b;
	cout << c;
}
```  
* * *  
> ## 2. 구조체 Struct ★★★★★
```c++
#include<stdio.h>
struct Math {
	int a, b; //구조체 멤버 변수
	int add();
};
int Math::add() { //:: = 스코프연산자 구조체 Math안의 변수를 사용한다.
	return a + b;
}
int main() {
	Math me;
	me.a = 2; me.b = 3;
	printf("%d\n", me.add());
}
```
* * *
> ## 3. C++ 클래스
```c++
#include<stdio.h>
class Math {
	int a, b;
public:
	Math(int x, int y) { //생성자
		a = x;
		b = y;
	}
	int add() {
		return a + b;
	}
};
int main() {
	Math me(2, 3); //생성자
	printf("%d\n", me.add());
}
```
