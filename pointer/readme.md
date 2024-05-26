
### 01번 예제

```c
#include<stdio.h>

int main(void) {
	int number = 10;
	int* p;

	p = &number;

	printf("변수 number의 주소 = %p\n", &number);
	printf("포인터의 값 = %p\n", number);
	printf("변수 number의 값 =%d\n");
	printf("포인터가 가리키는 값 = &d\n", *p);

	return 0;
}
```
### 02번 예제
```c
#include<stdio.h>

int main(void) {
	int number = 10;
	int* p;

	p = &number;
	printf("변수 number의 값 &d\n", number);

	*p = 20;
	printf("변수 number의 값 = &d\n", number);

	return 0;
}
```
### 포인터 연산 예제
```c
#include<stdio.h>

int main(void) {
	char* pc;
	int* pi;
	double* pd;

	pc = (char *)10000;
	pi = (int *)10000;
	pd = (double *)10000;
	printf("증가 전 pc =%d, pd =%d\n", pc, pi, pd);

	pc++;
	pi++;
	pd++;
	printf("증가 후 pc =%d, pi = %d, pd =%d \n", pc, pi, pd);
	
	return 0;
}
```
### swap()함수 예정
```c
#include<stdio.h>

int main(void) {
	int a = 100, b = 200;
	
	printf("swap() 호출전 a=%d b=%d\n", a, b);
	swap(&a, &b);
	printf("swap() 호출후 a=%d b=%d\n", a, b);

	return 0;
}

void swap(int* px, int* py) {
	int tmp;

	tmp = *px;
	*px = *py;
	*py = tmp;
}
```
