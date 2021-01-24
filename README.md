# vs2013-1-24
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
////数组的创建方式
//type_t   arr_name    [const_n];
////type_t 是指数组的元素类型
////const_n  是一个常量表达式，用来指定数组的大小
////实例：
////代码1：
//int arr1[10];
////代码2：
//int count = 10;
//int arr2[count];//数组时候可以正常创建？
////代码3：
//char arr3[10];
//float arr4[1];
//double arr5[20];
////注意：数组创建，[]中要给一个常量才可以，不能使用变量。

//int main()
//{
//	//创建一个数组-存放整型-10个
//	int arr[10];
//	char arr2[5];
//	int n = 5;
//	char ch[n];
//	return 0；
//}

//int arr1[10] = { 1, 2, 3 };//不完全初始化，剩下的元素默认初始化为0
//int arr2[] = { 1, 2, 3, 4 };
//int arr3[5] = { 1, 2, 3, 4, 5 };
//char arr4[3] = { 'a', 98, 'c' };
//char arr5[] = { 'a', 'b', 'c' };
//char arr6[] = "abcdef";
//
//
//int main()
//{
//	char arr1[] = "abc";
//	char arr2[3] = { 'a', 'b', 'c' };
//	printf("%d\n", sizeof(arr1));//4
//	printf("%d\n", sizeof(arr2));//3
//	printf("%d\n", strlen(arr1));//3
//	printf("%d\n", strlen(arr2));//随机
//	return 0;
//}

//char arr3[5] = { 'a', 'b' };
//char arr4[5] = "ab";//ok

//int main()
//{
//	char arr4[] = "abcdef";
//	printf("%d\n", sizeof(arr4));//7
////sizeof计算arr4所占空间的大小
//	//7个元素-char 7*1=7
//	printf("%d\n", strlen(arr4));//6
//	//strlen 求字符串的长度-‘\0’之前的字符个数
//	//[a b c d e f \0]
//}

//strlen 和sizeof的比较
//1.strlen 和 sizeof 没有什么关联
//2.strlen 是求字符串长度的-只能针对字符串求长度-库函数-使用得引头文件
//3.sizeof 计算变量、数组、类型的大小-单位是字节-操作符

//int main()
//{
//	char arr[] = "abcdef";//[a][b][c][d][e][f][\0]
//	printf("%c\n", arr[3]);
//	return 0;
//}

//int main()
//{
//	char arr[] = "abcdef";
//	int i = 0;
//	for (i = 0; i < 6; i++);
//	{
//		printf("%c", arr[i]);
//	}
//	return 0;
//}
//
//int main()
//{
//	char arr[] = "abcdef";
//	int i = 0;
//	for (i = 0; i < (int)strlen(arr); i++);
//	{
//		printf("%c", arr[i]);
//	}
//	return 0;

//}int main()
//{
//	char arr[] = "abcdef";
//	int i = 0;
//	int len = strlen(arr);
//	for (i = 0; i < len ; i++);
//	{
//		printf("%c", arr[i]);
//	}
//	return 0;
//}

//int main()
//{
//	int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 0 };
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	int i = 0;
//	for (i = 0; i < sz; i++)
//	{
//		printf("%d\n", arr[i]);
//	}
//	return 0;
//}

//int main()
//{
//	int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	int i = 0;
//	for (i = 0; i < sz; i++)
//	{
//		printf("&arr[%d]=%p\n",i,&arr[i]);
//	}
//	return 0;
//}

//int arr[3][4];
//char arr[3][5];
//double arr[2][4];
//int arr[3][4] = { 1, 2, 3, 4 };
//int arr[3][4] = { { 1, 2 }, { 4, 5 } };
//int arr[][4] = { { 2, 3 }, { 4, 5 } };

//int main()
//{
//	int arr[3][4] = { { 1, 2, 3 }, { 4, 5 } };
//	int i = 0;
//	for (i = 0; i < 3; i++)
//	{
//		int j = 0;
//		for (j = 0; j < 4; j++)
//		{
//			printf("%d ", arr[i][j]);
//		}
//		printf("\n");
//	}
//	return 0;
//}
//1 2 3 0
//4 5 0 0
//0 0 0 0 

//int main()
//{
//	int arr[3][4] = { { 1, 2, 3 }, { 4, 5 } };
//	int i = 0;
//	for (i = 0; i < 3; i++)
//	{
//		int j = 0;
//		for (j = 0; j < 4; j++)
//		{
//			printf("&arr[%d][%d]= %p\n", i , j ,&arr[i][j]);
//		}
//
//	}
//	return 0;
//}

//冒泡排序
//void bubble_sort(int arr[],int sz)
//{
//	//确定冒泡排序的趟数
//	int i = 0;
//	//int sz = sizeof(arr) / sizeof(arr[0]);//10
//	for (i = 0; i < sz - 1; i++)
//	{
//		int flag - 1;//假设这一趟要排序的数据已经有序
//		//每一趟冒泡排序
//		int j = 0;
//		for (j = 0; j <sz-1-i ; j++)
//		{
//			if (arr[j]>arr[j + 1])
//			{
//				int tmp = arr[j];
//				arr[j] = arr[j + 1];
//				arr[j + 1] = tmp;
//				flag = 0;//本趟排序的数据其实不完全有序
//			}
//		}
//		if (flag == 1)
//		{
//			break;
//		}
//	}
//	
//}
//int main()
//{
//	int arr[] = { 9, 8, 7, 6, 5, 4, 3, 2, 1, 0 };
//	int i = 0;
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	//对arr进行排序，排成升序
//	//arr是数组，我们对数组arr进行传参，实际上传递过去的是数组aee首元素的地址&arr[0]
//	bubble_sort(arr,sz);//冒泡排序函数
//	for (i = 0; i < sz; i++)
//	{
//		printf("%d ", arr[i]);
//	}
//	
//	return 0;
//}

void bubble_sort(int arr[], int sz)
{
	//确定冒泡排序的趟数
	int i = 0;
	//int sz = sizeof(arr) / sizeof(arr[0]);//10
	for (i = 0; i < sz - 1; i++)
	{
		//每一趟冒泡排序
		int j = 0;
		for (j = 0; j <sz - 1 - i; j++)
		{
			if (arr[j]>arr[j + 1])
			{
				int tmp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = tmp;
			}
		}
	}

}
int main()
{
	int arr[] = { 9, 8, 7, 6, 5, 4, 3, 2, 1, 0 };
	int i = 0;
	int sz = sizeof(arr) / sizeof(arr[0]);
	//对arr进行排序，排成升序
	//arr是数组，我们对数组arr进行传参，实际上传递过去的是数组aee首元素的地址&arr[0]
	bubble_sort(arr, sz);//冒泡排序函数
	for (i = 0; i < sz; i++)
	{
		printf("%d ", arr[i]);
	}

	return 0;
}

//int main()
//{
//	int arr[] = { 1, 2, 3, 4, 5, 6, 7 };
//	printf("%p\n", arr);
//	printf("%p\n", &arr[0]);
//	printf("%p\n", *arr);//1
//	return 0;
//}

//int main()
//{
//	int arr[] = { 1, 2, 3, 4, 5, 6, 7 };
//	printf("%p\n", arr);
//	printf("%p\n", arr+1);
//	printf("%p\n", &arr[0]);
//	printf("%p\n", &arr[0]+1);
//	printf("%p\n", &arr);
//	printf("%p\n", &arr+1);
//	//int sz = sizeof(arr) / sizeof(arr[0]);
//	//1.sizeof （数组名）-数组名表示整个数组，sizeof（数组名）计算的是整个数组的大小，单位是字节
//	//2.&数组名，数组名代表整个数组，&数组名，取出的是整个数组的地址
//}
