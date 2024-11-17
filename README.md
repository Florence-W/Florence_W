# Florence_W
//制作一个简单的计算器
#include<stdio.h>
int main()
{
	//输入数字及运算符

	double num1, num2;
	char operator;
	printf("Please Output the first number: ");
	scanf_s("%lf",&num1);
	printf("Please Output operator: ");
	scanf_s(" %c", &operator); // 注意这里的空格，用于处理输入缓冲区的换行符
	printf("Please Output the second number: ");
	scanf_s("%lf",&num2);

	//进行计算

	double result;
	if (operator=='+')
	{
		result = num1 + num2;
	}
	else if (operator=='-')
	{
		result = num1 - num2;
	}
	else if (operator='*')
	{
		result = num1 * num2;
	}
	else if (operator='/')
	{
		if (num2 == 0)
		{
			printf("除数不能为0！");
			return 1;
		}
		else
		{
			result = num1 / num2;
		}
	}
	else
	{
		printf("运算符无效\n");
	}

	//打印结果

	printf("%.2lf",result);

	return 0;
	}
