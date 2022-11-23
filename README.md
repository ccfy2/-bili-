# -bili-
//在有序的数组中查找某个数字并算出它的下标
#include<stdio.h>
int main()
{ 
  int arr[] ={1,2,3,4,5,6,7,8,9,10,11};
  int k = 7;
  int sz =sizeof(arr)/sizeof(arr[0]);
  int left = 0;
  int right = sz - 1;
  while(left<=right)
  {
    int mid = (left+right)/2;
    if(arr[mid]>k)
    {
     right = mid -1;
     }
     else if(arr[mid]<k)
     {
       left = mid +1;
     }
     else
     {
       printf("找到了，下标是:%d\n", mid);
       break;
     }
 }
 if(left>right)
 {
   printf("找不到\n");
 }

return 0;
}


//演示多个字符从两端移动，向中间汇集
#include<stdio.h>
#include<string.h>
#include<windows.h>
int main()
{
  char arr1[] = "welcome to bit!!!!!!";
  char arr2[] = "####################";
  int left = 0;
  int right = strlen(arr1)-1;
  //int right = sizeof(arr1)/sizeof(arr1[0])-2;
  while(left<=right)
{
  arr2[left] = arr1[left];
  arr2[right] = arr1[right];
  printf("%s\n",arr2);
  Sleep(1000);
  //休息一秒
  system("cls");
  //执行系统命令的一个函数-cls-清空屏幕
  left++;
  right--;
}
printf("%s\n", arr2);

  return 0;
}  


//登录用户密码 三次机会 第四次退出程序
#include<stdio.h>
#include<string.h>
int main()
{
	int i = 0;
	char password[20]= {0};
	for(i=0; i<3; i++)
	{
		printf("请输入密码:>");
		scanf("%s", password);
		if(strcmp(password, "123456")==0)
		{
			printf("登录成功\n");
			break;
		}
		else
		{
			printf("密码错误\n");
		}
	}
	if(i==3)
		printf("三次密码均错误，退出程序\n");
	return 0;
}


//传址--利用取地址来改变函数外部的实际参数的值
void swap(int* pa, int* pb)
{
	int tmp = 0;
	tmp = *pa;
	*pa = *pb;
    *pb = tmp;
}

#include<stdio.h>
int main()
{
	int a =10;
	int b =20;
	printf("a=%d b=%d\n", a, b);
	swap(&a,&b);
	printf("a=%d b=%d\n", a, b);

	return 0;
}


//打印100-200之间的素数
int is_prime(int n)
{
	int j;
	for(j=2; j<n; j++)
	{
		if(n%j==0)
			return 0;
	}
	return 1;
}

#include<stdio.h>
int main()
{
	int i = 0;
	for(i=100; i<=200; i++)
	{
		if(is_prime(i) == 1)
			printf("%d ", i);
	}

	return 0;
}


//打印1000—2000的闰年
#include<stdio.h>
int is_leap_year(int y)
{
	if((y%4==0&&y%100!=0)|| (y%400==0))
		return 1;
	else
		return 0;
}
int main()
{
	int year = 0;
	for(year=1000; year<=2000; year++)
	{
		if(1==is_leap_year(year))
		{
			printf("%d ", year);
		}
	}
	return 0;
}
























































