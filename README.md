#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

int main(void)
{
	int d, i, j, summ1 = 0, summ2 = 0, confirmation = 1;

	int a[5][5];
	for (i = 1; i < 6; i++); {
		printf("Enter 5 numbers of row %d\n", i);
		for (j = 1; j < 6; j++) {
			scanf("%d, ", &d);
			a[i][j] = d;
		}
	}
	for (i = 1; i < 6; i++) {
		summ1 = summ1 + a[1][i];
	}
	for (i = 2; i < 6; i++) {
		summ2 = 0;
		for (j = 1; j < 6; j++) {
			summ2 = summ2 + a[i][j];
		}
		if (summ1 != summ2)
			confirmation = 0;
	}
	for (j = 1; j < 6; j++) {
		summ2 = 0;
		for (i = 1; i < 6; i++) {
			summ2 = summ2 + a[i][j];
		}
		if (summ1 != summ2)
			confirmation = 0;
	}
	summ2 = 0;
	for (i = 1; i < 6; i++) {
		j = i;
		summ2 = summ2 + a[i][j];
	}
	if (summ1 != summ2)
		confirmation = 0;
	summ2 = 0;
	for (i = 5; i > 0; i--) {
		j = 6 - i;
		summ2 = summ2 + a[i][j];
	}
	if (summ1 != summ2)
		confirmation = 0;
	if (confirmation = 1)
		printf("Your array is magical!");
	else printf("Your array is not magical...");
	system("pause");
}
