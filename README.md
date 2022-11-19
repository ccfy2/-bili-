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
















































