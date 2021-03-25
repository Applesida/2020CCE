# 2020CCE

## 第一週

### 進階題:分式化簡
```C
#include <stdio.h>
int main()
{
	int n,m;
	scanf("%d%d",&n,&m);
	for (int i=10000;i>=1;i--){
		if (n%i==0 && m%i==0) {printf("%d %d\n",n/i,m/i);
			break;}
}
```
## 進階題：讀入整數反序列印
```C
#include <stdio.h>
int main()
{
	int n,a[10]={0};
	for (int i=0;i<10;i++){
	   scanf("%d",&a[i]);
	}
	for (int i=9;i>=0;i--){
		if (a[i]!=0) printf("%d ",a[i]);
	}
		printf("\n");
	
}
```

## 進階題：A的B次方函數
```C
#include <stdio.h>
int MYPOWER(int n,int m)
{
	int ans=1;
	for (int i=1;i<=m;i++){
		ans*=n;
	}
	return ans;
}
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}
```
## 進階題：漸增數列相加 
```C
#include <stdio.h>
int main()
{
	int n;
	int ans=0;
	scanf("%d",&n);
	for (int i=1;i<n;i++){
		ans+=i*(i+1);
	}
	printf("%d\n",ans);
}
```
## 基礎題：找零錢 
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	printf("%d=50*%d+5*%d+1*%d\n",n,n/50,(n%50)/5,n%50%5);
}
```
## 基礎題：因數個數 
```C
#include <stdio.h>
int main()
{
	int n,m=0;
	scanf("%d",&n);
	for (int i=1;i<=n;i++){
		if (n%i==0) {m++;} 
	}
	printf("%d\n",m);
}
```
## 基礎題：找倍數 
```C
#include <stdio.h>
int main()
{
	int n,a[10];
	int b=0;
	for (int i=0;i<10;i++){
		scanf("%d",&n);
		if (n<=1000 && n>=1) a[i]=n;
	}
	for (int i=0;i<10;i++){
		if (a[i]%3==0) {b++;}
	}
	printf("%d\n",b);
}
```
## 基礎題：整數轉換為等級
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	if (n>=90) printf("A\n");
	else if (n>=80) printf("B\n");
	else if (n>=60 && n<80) printf("C\n");
	else printf("F\n");
}
```
# 第二週

## 現在改用陣列 int n[3]={10, 20, 30}, 再用指標, 去改裡面的值
```C
#include <stdio.h>
int main()
{
    int n[3]={10,20,30};
    printf("n[0]:%d n[1]:%d n[2]:%d\n",n[0],n[1],n[2]);

    int *p= &n[0];
    *p=200;
    printf("n[0]:%d n[1]:%d n[2]:%d\n",n[0],n[1],n[2]);

    int *p2= &n[2];
    *p2=300;
    printf("n[0]:%d n[1]:%d n[2]:%d\n",n[0],n[1],n[2]);

    p2=p;
    *p2=400;
    printf("n[0]:%d n[1]:%d n[2]:%d\n",n[0],n[1],n[2]);
}

```
## 進階題：大小寫轉換
```C
#include <stdio.h>
int main()
{
	char a[10];
	scanf("%s",&a);
	for (int i=0;a[i]!=0;i++){
		if (a[i]>='0' && a[i]<='9'){
			printf("%c",a[i]);
		}
		else if(a[i]>='A' && a[i]<='Z'){
			a[i]+=32;
			printf("%c",a[i]);
		}
		else if(a[i]>='a' && a[i]<='z'){
			a[i]-=32;
			printf("%c",a[i]);
		}
	}
		printf("\n");
}
```
## 進階題：漸增數列相加
```C
#include <stdio.h>
int main()
{
	int n,ans=0;
	scanf("%d",&n);
	for(int i=1;i<n;i++){
		ans+=i*(i+1);
	}
	printf("%d\n",ans);
}
```
## 進階題：計算陣列的平方值
```C
#include <stdio.h>
int main()
{
	int n,a;
	scanf("%d",&n);
	for(int i=0;i<n;i++){
		scanf("%d",&a);
		printf("%d,",a*a);
	}
	printf("\n");
}
```
## 進階題：2進位轉10進位 
```C
#include <stdio.h>
int main()
{
	int n,ans=0,m=1;
	scanf("%d",&n);
	for(int i=0;i<4;i++){
		ans+=n%10*m;
		n/=10;
		m*=2;
	}
	printf("%d\n",ans);
}
```
## 基礎題：計算幾週與幾天
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	printf("%d %d\n",a/7,a%7);
}
```
## 基礎題：計程車資計算
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	if (a<=2000) printf("100\n");
	else  if ((a-2000)%500==0){printf("%d\n",(a-2000)/500*5+100);}
	else printf("%d\n",(a-2000)/500*5+105);
}
```
## 基礎題：兩數間可被5整除的整數
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	if(a>b)
	{
		int t=a;a=b;b=t;
	}
	for (int i=a;i<=b;i++){
		if (i%5==0){printf("%d\n",i);} 
	}
}
```
## 基礎題：整數間最大距離 
```C
#include <stdio.h>
int main()
{
	int a[3],ans;
	for(int i=0;i<3;i++){
		scanf("%d",&a[i]);}
	for(int i=0;i<3;i++){
		for(int i=0;i<2;i++){	
			if(a[i]>a[i+1])
			{
				int t=a[i];
				a[i]=a[i+1];
				a[i+1]=t;
			}
		}
		}
	for(int i=0;i<3;i++){
		ans=a[2]-a[0];
	}
	printf("%d\n",ans);
	
}
```
## 第三週
### 指標練習1

```C
#include <stdio.h>
int a[5]={0,10,20,30,40};
int main()
{
	int *p=a[2];
	*p=222;
	
	p=p+2;
	*p=666;
}
```
### 指標練習2

```C
#include <stdio.h>
int a[5]={0,10,20,30,40};
void p1()
{
	for (int i=0;i<5;i++){
		printf("%d",a[i]);
	}
	printf("\n");
}
int main()
{
	int *p= &a[2];
	*p=222;
	p1();
	
	p=p+2;
	*p=666;
	p1();

	p--;

	*p=555;
	p1();
}
```
### 指標練習3
```C
#include <stdio.h>
int a[10]={0,10,20,30,40,50,60,70,80,90};
void p1()
{
	for (int i=0;i<10;i++){
		printf("%d",a[i]);
	}
	printf("\n");
}
int main()
{
	int *p= &a[2];
	*p=222;
	p1();
	
	p=p+4;
	*p=666;
	p1();

	p--;

	*p=555;
	p1();
}
```
### 指標練習4
```C
#include <stdio.h>
#include <stdlib.h>
int a[10];
int main()
{
	int b[10];

	int *p = (int*) malloc(sizeof(int)*10);
	return 0;
}
```
## 第四週
### struct 結構練習1
```C
#incldue <stdio.h>
struct DATA{
	float x,y,z;
}
int main()
{

}
```
### struct 結構練習2
```C
#incldue <stdio.h>
struct DATA{
	float x,y,z;
} point1 ;
int main()
{
	point1.x=3;
	point1.y=4;
	point1.z=6;
	printf("%f %f %ｆ",point1.x,point1.y,point1.z);
}
```
### struct 結構練習3
```C
#incldue <stdio.h>
struct DATA{
	float x,y,z;
} point1 ;
struct DATA points[5];
int main()
{
	for (int i=0;i<5;i++){
		point1.x=3;
		point1.y=4;
		point1.z=6;
		printf("%f %f %ｆ",point[i].x,point[i].y,point[i].z);
	}
}
```
### struct 結構練習4
```C
#incldue <stdio.h>
struct DATA{
	float x,y,z;
} a,b,c;
struct DATA points[5];
int main()
{
	struct DATA d,e,f;
	for(int i=0;i<5;i++){
		point1.x=3;
		point1.y=4;
		point1.z=6;
		printf("%f %f %ｆ",points[i].x,point1s[i].y,points[i].z);
	}
}
```
### struct 結構練習5
```C
#incldue <stdio.h>
struct DATA{
	float x,y,z;
} a,b;
struct DATA c,d;
int main()
{
	struct DATA e;
	struct DATA f={1,2,3};
	printf("%f %f %f\n",a.x,a.y,a.z);
	printf("%f %f %f\n",b.x,b.y,b.z);
	printf("%f %f %f\n",c.x,c.y,c.z);
	printf("%f %f %f\n",d.x,d.y,d.z);
	printf("%f %f %f\n",e.x,e.y,e.z);
	printf("%f %f %f\n",f.x,f.y,f.z);
}
```
## 第五周

### 字元練習1
```c
#include <stdio.h>
char line[20]="233233233233233233";
int main()
{
    char *p=line;
    for (int i=0;line[i]!=0;i++){
            p=&line[i];
            char c=line[i];
            if (c!='2') printf("%c",c);

    }
    printf("\n");

}
```
### 字元練習2
```c
#include <stdio.h>
int main()
{
    char line[10]="decline";
    char line2[10]={'p','r','o','p','e','r','\0'};
    printf("%s\n",line);
    printf("%s\n",line2);
}

```
### 字元練習3 //錯誤的版本
```c
#include <stdio.h>
int main()
{
    char line[10]="decline";
    char line2[10]={'p','r','o','p','e','r','\0',};

    printf("%s\n",line);
    printf("%s\n",line2);

    char line3[]="majority這是好的，沒問題，要多長有多長";
    char line4[]={'m','a','j','o','r','i','t','y'};
    printf("你相信嗎？這是line4==%s==",line4);
}

```
### 字元練習4
```c

```
### 字元練習5
```c

```
