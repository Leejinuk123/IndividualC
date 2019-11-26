> ## 1. 퀵 쇼팅(Quick Sorting)  

퀵 정렬(Quick)  
```c
#include <stdio.h>      /* printf */
#include <stdlib.h>     /* qsort */
int compare(const void* a, const void* b) { //void는 형태가 없다. const는 상수화 시켜준다.
	return (*(int*)a - *(int*)b); //타입캐스팅
}
int main() {
	int v[] = {3,1,2,5,4}; 
	int n; 
	qsort(v, 5, sizeof(int), compare); //매개변수 (배열,갯수,사이즈,함수)
	for (n = 0; n < 5; n++)  printf("%d ", v[n]); 
	return 0;
}
```  
* * *  

> ## 2. 퀵 쇼팅(소수점)  
```c
#include <stdio.h>      /* printf */
#include <stdlib.h>     /* qsort */
int compare(const void* a, const void* b) { //void는 형태가 없다. const는 상수화 시켜준다.
	return (*(double*)a - *(double*)b); //타입캐스팅
}
int main() {
	double v[] = {3,1,2,5,4}; 
	int n; 
	qsort(v, 5, sizeof(double), compare); //매개변수 (배열,갯수,사이즈,함수)
	for (n = 0; n < 5; n++)  printf("%f ", v[n]); 
	return 0;
}
```

> ## 3. 스택 Stack :
배열에 마지막에 넣은게 처음으로 나온다.  
```c
#include<stdio.h>
int sp = -1; //스택포인터
int v[1000]; //스택
void push(int a) {
	++sp;
	v[sp] = a;
}
int pop() {
	return(v[sp--]);
}
int main() {
	push(5); 
	push(3);
	printf("%d\n", pop()); 
	printf("%d\n", pop());
}
```
