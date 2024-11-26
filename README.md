实验二 顺序结构程序设计
一、实验目的
1、掌握 C 语言中使用最多、最基本的一种语句﹣﹣赋值语句的使用。
2、掌握数据的输入输出方法，能正确使用各种格式转换符。
3、熟悉顺序结构的程序设计方法。
4、进一步掌握 C 语言程序的编辑、编译、连接和运行的过程。
二、实验准备
1、复习 C 语言的赋值运算符，同时区分“=”和“==”的区别。
2、复习 printf 和 scanf 的格式及要求。
3、复习程序代码编写规范。
三、实验内容
1、输入并运行以下程序，调试并运行出结果
#include <stdio.h>
int main()
{
	int a, b;
	float d, e;
	char c1, c2;
	double f, g;
	long m, n;
	unsigned int p, q;
	a = 61; b = 62;
	c1 = 'a'; c2 = 'b';
	d = 3.56; e = -6.87;
	f = 3157.890121; g = 0.123456789;
	m = 50000; n = -60006;
	p = 32768; q = 40006;
	printf("a=%d,b=%d\nc1=%c,c2=%c\nd=%6.2f,e=%6.2f\n",a,b,c1,c2,d,e);
	printf("f=%15.6f,g=%15.2f\nm=%ld,n=%1d\np=%u,q=%u\n'",f,g,m,n,p,q);
	return 0;
}
![1U}_NV7A6Y9J6K@IY)QH 4T](https://github.com/user-attachments/assets/32ae323b-9f47-41bc-90cf-7a0532e81c7a)

2、运行程序并回答问题
#include <stdio.h>
int main()
{
	int n, x, y, z;
	printf("请输入一个不大于 1000 的整数：");
	scanf("%d", &n);
	x = n / 100;
	y = (n - x * 100) / 10;
	z = (n - x * 100 - y * 10);
	printf("\n%d%d%d\n", z, y, x); 
	return 0;
}
问题：此程序的功能是什么？你能用其他方法实现同样的功能吗？请上机调试。
这段代码的功能是将用户输入的一个不大于1000的整数分解成个位、十位和百位上的数字，并按照个位、十位、百位的顺序打印出来。
![B {R9TFUI_V~3 Z@~OBR 3J](https://github.com/user-attachments/assets/4d72456a-9858-4924-b108-2c6f53bd3a60)

除了上面这种方法，还有一种可以实现同样的功能，如下:
#include <stdio.h>
int main() {
    int n;
    printf("请输入一个不大于 1000 的整数：");
    scanf("%d", &n);
    printf("\n%1d%1d%1d\n", n % 10, (n / 10) % 10, n / 100);
    return 0;
}
3、编写输入三角形三边长 a，b，c，求三角形的面积 area 程序
#include <stdio.h> 
#include <math.h> 
int main() {
	double a, b, c, s, area;
	printf("请输入三角形的三边长：\n");
	scanf("%lf %lf %lf", &a, &b, &c);
	if (a + b > c && a + c > b && b + c > a) {
		s = (a + b + c) / 2.0;
		area = sqrt(s * (s - a) * (s - b) * (s - c));
		printf("三角形面积为：%lf\n", area);
	}
	else {
		printf("这不是一个三角形。\n");
	}
	return 0;
}
![CWQW`8EJ1Q))RKWCJ1O59 B](https://github.com/user-attachments/assets/b4e1158a-b7e0-4162-b2e6-7452843dcb6b)
