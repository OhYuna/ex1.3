#include <stdio.h>

int main(void)
{
	float a;
	float b = 1.0;
	float temp;
	float sum = 0;
	int m = 2;

	for (a = 2.0; a <= 100.0; a++)
	{
		if (m % 2 == 0 && a != 100) {
			temp = a;
			printf("%.0lf/%.0lf - ", b, a);
		}

		else if (m % 2 != 0) {
			temp = -1 * a;
			printf("%.0lf/%.0lf + ", b, a);
		}
		else {
			temp = a;
			printf("%.0lf/%.0lf ", b, a);
		}

		if (m % 10 == 0)
			printf("\n");

		sum += b / temp;
		b++;
		m++;
	}
		printf(" = %lf \n", sum);
		return 0;
	
}
