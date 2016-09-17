# Task1

#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>


int main(void)
{
	int number, result=0, ;
	printf("Введите число от 1 до 1000\n");
	scanf("%d", &number);
	if (number > 500)
	{
		result = result + 500;
		number = number - 500;
	}

}
