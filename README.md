# 2020CCE

##第一周作業

##第一題 : 進階題:分式化簡
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
##第二題 : 進階題：讀入整數反序列印
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

##第三題 : 進階題：A的B次方函數
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
##第四題 : 進階題：漸增數列相加 
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
##第五題 : 基礎題：找零錢 
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	printf("%d=50*%d+5*%d+1*%d\n",n,n/50,(n%50)/5,n%50%5);
}
```
##第六題 : 基礎題：因數個數 
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
##第七題 : 基礎題：找倍數 
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
##第八題 : 基礎題：整數轉換為等級
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
##第二周

##現在改用陣列 int n[3]={10, 20, 30}, 再用指標, 去改裡面的值
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
