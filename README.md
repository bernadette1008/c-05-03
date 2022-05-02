# c-05-03-Calculator

c언어로 만든 계산기

```c
#include <stdio.h>

int main() {
	int input, num;

	printf("계산기\n");

	printf("숫자를 입력하시오.");
	scanf_s("%d", &num);
	printf("현재 숫자는 %d\n\n", num);

	while (1) {
		printf("연산자를 선택하시오. (0. 숫자초기화  1. +   2. -   3. *   4. /   9. exit) : ");
		scanf_s("%d", &input);

		if (input == 9)
			break;

		else if (input == 0) {
			num = 0;
			printf("처음 숫자를 입력하시오.");
			scanf_s("%d", &num);
			printf("현재 숫자는 %d\n\n", num);
		}

		//	+ 더하기
		else if (input == 1) {
			printf("%d + ____\b\b\b\b", num);
			scanf_s("%d", &input);
			num += input;
			printf("현재 숫자는 %d\n\n", num);
		}

		//	- 빼기
		else if (input == 2) {
			printf("%d - ____\b\b\b\b", num);
			scanf_s("%d", &input);
			num -= input;
			printf("현재 숫자는 %d\n\n", num);
		}

		//	* 곱하기
		else if (input == 3) {
			printf("%d * ____\b\b\b\b", num);
			scanf_s("%d", &input);
			num *= input;
			printf("현재 숫자는 %d\n\n", num);
		}

		// / 나누기(몫)
		else if (input == 4) {
			printf("%d / ____\b\b\b\b", num);
			scanf_s("%d", &input);
			num /= input;
			printf("현재 숫자는 %d\n\n", num);
		}
	}
	return 0;
}
```
