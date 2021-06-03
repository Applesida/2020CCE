# 2020CCE

## 第一週

### 進階題:分式化簡
```c
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
```c
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
```c
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
```c
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
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	printf("%d=50*%d+5*%d+1*%d\n",n,n/50,(n%50)/5,n%50%5);
}
```
## 基礎題：因數個數 
```c
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
```c
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
```c
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
```c
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
```c
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
```c
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
```c
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
```c
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
```c
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	printf("%d %d\n",a/7,a%7);
}
```
## 基礎題：計程車資計算
```c
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
```c
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
```c
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

```c
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

```c
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
```c
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
```c
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
```c
#incldue <stdio.h>
struct DATA{
	float x,y,z;
}
int main()
{

}
```
### struct 結構練習2
```c
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
```c
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

```c
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

```c
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
#include <stdio.h>
int main()
{
    char line[5][10]={"decline","proper","majority","bullet","shop"};
    char *p;
    for (int i=0;i<5;i++){
        p =line[i];
        printf("%s\n",line[i]);
    }


}
```
### 字元練習5
```c
#include <stdio.h>
int a[3][3]={ {1,2,3},{4,5,6},{7,8,9}};
int main()
{
    for (int i=0;i<3;i++){
        for (int j=0;j<3;j++){
            printf("%d ",a[i][j]);
        }
        printf("\n");
    }
}

```
### 第六周
### 字串排序1
```C
#include <stdio.h>
#include <string.h>
char a[100][10];
char t[10];
int main()
{
	int n;
	scanf("%d",&n);
	for (int i=0; i<n; i++){
		scanf("%s",a[i]);
	}
	for (int i=0;i<n;i++){
		for (int j=i+1;j<n;j++){
			if (strcmp(a[i],a[j]) >0){
				strcpy(t,a[i]);
				strcpy(a[i],a[j]);
				strcpy(a[j],t);
			}
		}
	}
	for (int i=0;i<n;i++){
		printf("%s\n",a[i]);
	}
}

```

### 字串排序2
```C
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
char a[100][10];
int compare( const void *p1, const void *p2)
{
	char *s1 = (char*)p1;
	char *s2 = (char*)p2;
	return strcmp(s1, s2);
}
int main()
{
	int n;
	scanf("%d",&n);
	
	for (int i=0;i<n;i++){
		scanf("%s",a[i]);
	}
	qsort( a, n, 10, compare);
	for (int i=0;i<n;i++){
		printf("%s\n",a[i]);
	}
}


```
## 第七周
### ctutor試用練習
```c
#include <stdio.h>
int main()
{
	for(int i=0; i<10; i++){
		printf("Hello world");
	}
	return 0;
}
```
### 字串排序 (qsort 版本)

```c
#incldue <stdio.h>
#include <string.h>
#incldue <stdlib.h>
char a[100][10];
int compare ( const void *p1 , const void *p2) 
{
	char *s1= (char *)p1;
	char *s2= (char *)p2;
	return strcmp (s1,s2);
}
int main()
{
	int n;
	scanf("%d",&n);

	for ( int i=0; i<n;i++){
		scanf("%s",a[i]);
	}
	qsort (a, n ,10, compare);
	for (int i=0; i<n ,i++){
		printf("%s\n",a[i]);
	}
}
```
### 使用ctutor 的解說線條及更改

```c
#include <stdio.h>
char *p1, *p2;
char line[4][10]={"jkl","ghi","def","abc"};
char t[10];
int main()
{
	int n=4;
	for (int i=0;i<n;i++){
		for (int j=i+1;j<n;j++){
		p1=line[i];p2=line[j];
		if (strcmp( line[i],line[j])>0){
			strcpy(t,line[i]);
			strcpy(line[i],line[j]);
			strcpy(line[j],t);
			}	
		}
	}
	for(int i=0;i<n;i++){
		printf("%s\n",line[i]);
	}
	return 0;
}
```
## 第八周
### UVA 10226先試讀資料加印出來
```c
#include <stdio.h>
char tree[1000000][32];
int main()
{
	int T;
	scanf("%d\n\n",&T);
	for (int t=0;t<T;t++){
		for(int i=0;i<??;i++){
			gets(tree[i]);
		}
	}
	printf("%s\n",tree[i]);
}
```
### UVA 10226 加入字串排序的部分
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int compare( const void *p1 , const void *p2){
	return strcmp( (char *)p1, (char*) p2);
}
int main()
{
	int n;
	scanf("%d",&n);
	for (int i=0;i<n;i++){
		scanf("%s",line[i]);
	}
	qsort ( line ,n , 10 , compare);
	
	for (int i=0;i<n;i++){
		printf("%s\n",line[i]);
	}
}
```

### UVA 10266 收尾
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
char a[100][10];
int compare (const void *p1 , const void *p2){
	return strcmp( (char*)p1 , (char*)p2);
}
int main()
{
	int n;
	scanf("%d,&n);
	for (int i=0;i<n;i++){
		scanf("%s",a[i]);
	}
	qsort (a , n , 10 , compare );
	for (int i=0 ; i<n; i++){
		printf("%s\n",a[i]);
	}
}
```
## 第十周
### UVA 10008 讀字串加上印出來 ( 小心跳行)
```c
#include <stdio.h>
char line[1000];
int main()
{
	int n;
	scanf("%d\n",&n);
	
	for (int i=0;i<n;i++){
		gets(line);
		printf("%s\n",line);
	}
}
```
### 針對每個字母判斷大,小寫,其他

```c
#include <stdio.h>
char line[1000];
int main()
{
	int n;
	scanf("%d\n",&n);
	
	for (int i=0;i<n;i++){
		gets(line);
	
		for(int k=0;line[k]!=0;k++){
			char c=line[k];
			if (c>='A' && c<='Z') printf("大");
			else if (c>='a' && c<='z') printf("小");
			else printf("他");
		}
		
	}
}
```
### 對應的統計在 ans[ c-'A' ] ++ 和 ans[ c-'a' ] ++
```c
#include <stdio.h>
char line[1000];
int ans[26];
int main()
{
	int n;
	scanf("%d\n",&n);
	
	for (int i=0;i<n;i++){
		gets(line);
	
		for(int k=0;line[k]!=0;k++){
			char c=line[k];
			if (c>='A' && c<='Z') ans[c-'A']++;
			else if (c>='a' && c<='z') ans[c-'a']++;
		}
		
	}
	for (int i=0; i<26; i++){

		printf("%c %d\n",'A'+i, ans[i]);
	}
}
```
### 用很複雜的方式排序並印出來
```c
#include <stdio.h>
char line[1000];
int ans[26];
char alphabet []="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
int main()
{
	int n;
	scanf("%d\n",&n);
	
	for (int i=0;i<n;i++){
		gets(line);
	
		for(int k=0;line[k]!=0;k++){
			char c=line[k];
			if (c>='A' && c<='Z') ans[c-'A']++;
			else if (c>='a' && c<='z') ans[c-'a']++;
		}
		
	}
	for (int i=0;i<26;i++){
		for (int j=i+1; j<26; j++){
			if ( ans[i]>ans[j] || (ans[i] == ans[j] && alphabet[i]>alphabet[j]) ){
				int t=ans[i];
				ans[i]=ans[j];
				ans[j]=t;
				int c=alphabet[i];
				alphabet[i]=alphabet[j];
				alphabet[j]=c;
			}
		}
	}

	for (int i=0; i<26; i++){

		if (ans[i]>0) printf("%c %d\n",alphabet[i], ans[i]);
	}
}
```
### 改用 qsort 搭配 struct 再寫一次
```c
#include <stdio.h>
#include <stdlib.h>
char line[1000];
typedef struct {
	int ans;
	char c;
}box;
box array[26];
int compare ( const void *p1 , const void *p2){
	if (  ((box*)p1 )-> ans >  ((box*)p2)->ans ) return -1;
	else if (  ((box*)p1 )-> ans <  ((box*)p2)->ans ) return 1;
	else return 0;
}
int main()
{
	for (int i=0;i<26;i++) array[i].c='A'+i;

	
	int n;
	scanf("%d\n",&n);
	
	for (int i=0;i<n;i++){
		gets(line);
	
		for(int k=0;line[k]!=0;k++){
			char c = line[k];
			if (c >='A' && c<='Z') ans[c-'A']++;
			else if (c>='a' && c<='z') ans[c-'a']++;
		}
		
	}
	
	qsort ( array , 26 , sizeof(box) , compare);

	for (int i=0; i<26; i++){

		if (array[i].ans >0 ) printf("%c %d\n",array[i].c, array[i].ans);
	}
}
```
## 第十一周
### 認識typedef 
```c
#include<stdio.h>
unsigned char c;
typedef unsigned char unchar;
unchar d;
int main()
{
    c='A';
    d = c;
    printf("%c", d);
}
```
### 練習 typedef struct data
```c
#include<stdio.h>
typedef struct data{
    char c;
    int ans;
} DATA;
///struct data listA;
DATA listA;

int main()
{
    listA.c = 'A';
    listA.ans=1;

    printf("%c %d\n", listA.c, listA.ans );

}
```
### 適用qsort compare
```c
#include<stdio.h>
#include<stdlib.h>
int compare( const void*p1, const void*p2)
{
    int d1 = ( (int)p1 );
    int d2 = ( (int)p2 );
    if(d1>d2) return 1;
    if(d1==d2) return 0;
    if(d1<d2) return -1;
}
int a[10] = {4,8,3,7,5,2,9,1,6,10};
int main()
{
    qsort ( a, 10, sizeof(int), compare);
    for( int i=0 ; i<10 ; i++){
        printf("%d ", a[i] );
    }
}
```
### UVA 10008 練習
```c
#include <stdio.h>
char line [2000]; //其實[1001]就可以了
int ans[256];//統計出現的次數, ex. ans[65] 代表 必65個字母出現次數
int main()
{
	//迴圈
	//step01: Input 一次1行, 100字母 (Q:不知道有幾行)
				//一次1行: 成功時有指標,失敗變NULL
	for(int t=0; gets(line)!=NULL ; t++){
		//step5:把資料清空
		for( int i=0 ; i<256 ; i++) ans[i]=0;
		
		//step3: 在一行中,每個字母慢慢分析
		for( int i=0 ; line[i]!=0 ; i++){
			char c=line[i];
			ans[c]++;//這個字母++
		}
		
		//欠 排序
		
		if(t>0) printf("\n");//step02:跳行問題
		
		for(int i=0 ; i<256 ; i++){
			if(ans[i]>0) printf("%d %d\n", i, ans[i]);
		}
		
	}//奇怪的迴圈
}
```
### compare 複雜版練習
```c 

#include <stdio.h>
#include <string.h>
#include <stdlib.h>
char name[100][82];
char other[100];
int compare( const void *p1 , const void *p2)
{
	char d1= *( (int *)p1 );
	char d2= *( (int *)p2 );
	if (d1>d2)	return 1;
	if (d1==d2) return 0;
	if (d1<d2)	return -1;
}
int main()

{
	int n;
	scanf("%d",&n);
	for (int i=0;i<n;i++){
		scanf("%s",name[ i ]);
		gets(other);
	}
	qsort (name , n , 82 ,compare);
	
	int ans=1;
	printf("%s",name[ 0 ]);
	for (int i=0;i<n-1;i++){
		if ( strcmp( name[ i ] , name[ i+1 ] )!=0){
			printf(" %d\n",ans);
			printf("%s",name[i+1]);
			ans=1;
		}
		else {
			ans++;
		}
	}
	printf(" %d\n",ans);
}

```
## 第十二周
### UVA 10062 依字母頻率由少排到多
```c
#include <stdio.h>
char line[2000];
int main()
{
	for (int t=0; gets(line) ; t++){
		int ans[256]={};
		
		char ascii[256];
		for (int i=0; i<256;i++) ascii[i]=i;
			
		for (int i=0; line[i]!=0; i++){
			char c=line[i];
			ans[c]++;
		}
		
		for (int i=0;i<256; i++){
			for( int j=i+1; j<256;j++){
				if (ans[i]>ans[j]) {
					int t=ans[i];
					ans[i]=ans[j];
					ans[j]=t;
					char c=ascii[i];
					ascii[i]=ascii[j];
					ascii[j]=c;
				}
			}
		}
		if (t>0) printf("\n");
		for (int i=0; i<256; i++){
			if (ans[i]>0 ) printf("%d %d\n", ascii[i], ans[i]);
		}
	}
}
```
### UVA 10062 完成字母頻率相同時 字母大小順序
```c
#include <stdio.h>
char line[2000];
int main()
{
	for (int t=0; gets(line) ; t++){
		int ans[256]={};
		
		char ascii[256];
		for (int i=0; i<256;i++) ascii[i]=i;
			
		for (int i=0; line[i]!=0; i++){
			char c=line[i];
			ans[c]++;
		}
		
		for (int i=0;i<256; i++){
			for( int j=i+1; j<256;j++){
				if (ans[i]>ans[j]) {
					int t=ans[i];
					ans[i]=ans[j];
					ans[j]=t;
					char c=ascii[i];
					ascii[i]=ascii[j];
					ascii[j]=c;
				}
				if (ascii[i] < ascii[j] && ans[i]== ans[j]){
					int t=ans[i];
					ans[i]=ans[j];
					ans[j]=t;
					char c=ascii[i];
					ascii[i]=ascii[j];
					ascii[j]=c;	
				}
			}
		}
		if (t>0) printf("\n");
		for (int i=0; i<256; i++){
			if (ans[i]>0 ) printf("%d %d\n", ascii[i], ans[i]);
		}
	}
}
```
### UVA 299 交換火車 先解決input output
```c
#include <stdio.h>
int a[100];
int main()
{
	int n;
	scanf("%d",&n);

	for (int i=0;i<n;i++){
		int m;
		scanf("%d",&m);

	for (int i=0;i<m;i++){
		scanf("%d",&a[i]);
	}

	int ans=0;
	printf("Optimal train swapping takes %d swaps.\n",ans);
	}
}
```
### 接續上面 完成泡泡排序法 算出正確答案
```c
#include <stdio.h>
int a[100];
int main()
{
	int n;
	scanf("%d",&n);

	for (int i=0;i<n;i++){
		int m;
		scanf("%d",&m);

	for (int i=0;i<m;i++){
		scanf("%d",&a[i]);
	}

	int ans=0;
	
	for(int i=0;i<m;i++){
		for ( int j=i+1;j<m;j++){
			if (a[i]>a[j]){
				int t=a[i];
				a[i]=a[j];
				a[j]=t;
				ans++;
			}
		}
	}

	printf("Optimal train swapping takes %d swaps.\n",ans);
	}
}
```
### UVA 11321 排排排序 先解決input output 
```c
#include <stdio.h>
int a[10000];
int main()
{
	int n,m;
	while ( scanf("%d%d",&n,&m)==2 ){
		for (int i=0;i<n;i++){
			scanf("%d",&a[i]);
		}
		printf("%d %d\n",n,m);
		for(int i=0;i<n;i++){
			printf("%d\n",a[i]);
		}
	}

}
```
### 接續上面 看懂他的排序並算出正確答案
```c
#include <stdio.h>
int a[10000];
void swap(int i,int j)
{
	int t=a[i];
	a[i]=a[j];
	a[j]=t;
}
int main()
{
	int n,m;
	while ( scanf("%d%d",&n,&m)==2 ){
		
		for (int i=0;i<n;i++){
			scanf("%d",&a[i]);
		}
		
		for (int i=0;i<n;i++){
			for (int j=i+1;j<n;j++){
				if ( a[i]%m > a[j]%m ) swap(i,j);
				if ( a[i]%m == a[j]%m && a[i]%2==0 && a[j]%2!=0 ) swap(i,j);
				if ( a[i]%m == a[j]%m && a[i]%2!=0 && a[j]%2!=0 && a[i] < a[j] ) swap(i,j);
				if ( a[i]%m == a[j]%m && a[i]%2==0 && a[j]%2==0 && a[i] > a[j] ) swap(i,j);
			}
		}
		printf("%d %d\n",n,m);
		for (int i=0;i<n;i++){
			printf("%d\n",a[i]);
		}
	}
}
```
## 第十三周 

## Processing 

###  預設大小跟背景顏色
```c
size(1024, 400);
background( 52, 141, 247 );
```
### 配合 void setup(), void draw() 
```c
void setup(){//只做一次的設定
  size(1024, 400);
}
void draw(){//互動版本,每秒畫60次
  if( mousePressed ) background(255, 0, 255);//按下去時 紫色
  else background( 52, 141, 247 );//否則 淡藍色
}
```
###  利用 void mousePressed() 來做互動, 讓 text() 可以秀出不同的點擊次數
```c
void setup(){//只做一次的設定
  size(1024, 400);
}
void draw(){//互動版本,每秒畫60次
  if( mousePressed ) background(255, 0, 255);//按下去時 紫色
  else background( 52, 141, 247 );//否則 淡藍色
}
```
### 文字的大小textSize()還有文字的加法
```c
void setup(){//只做一次的設定
  size(1024, 400);
}
void draw(){//互動版本,每秒畫60次
  if( mousePressed ) background(255, 0, 255);//按下去時 紫色
  else background( 62, 141, 247 );//否則 淡藍色
  textSize(80);//文字的大小
  text("中文壞掉Now a is" + a, 212, 200);//畫出文字
}//目標:文字全系列都教一下!!!大小
int a=0;
void mousePressed(){
   a++; 
}
```
### 了解hour(),minute(),second() 再用字串加法加長起來
```c
void setup(){//開新的
  size(1024,400);
}|
void draw(){
  background(#3E8DF7);//色碼
  int s = second();   //Value from 0 - 59
  int m = minute();   //Value from 0 - 59
  int h = hour();     //Value from 0 - 23
  textSize(80);
  text( h + ":" + m + ":" + s, 100, 200);
}   //數字  字串 數字 字串 數字
```
### 將秒、分、時,換算出總秒數,目標總秒數-現在總秒數,得到剩下總秒數
```c
void setup(){//開新的
  size(1024,400);
  textFont( createFont("標楷體", 80));
}
void draw(){
  background(#3E8DF7);//色碼
  int s = second();   //Value from 0 - 59
  int m = minute();   //Value from 0 - 59
  int h = hour();     //Value from 0 - 23
  textSize(80);
  text( h + ":" + m + ":" + s, 100, 200);
  int total = s + 60*m + 60*60*h;//現在總秒數
  int closeH=17, closeM=40, closeS=0;//下課的精確時間
  int total2=closeS + 60*closeM + 60*60*closeH;//目標總秒數
  int ans = total2 - total;
  text( "剩下幾秒:" + ans, 100, 100);
}   //數字  字串 數字 字串 數字
```
### 把總秒數,用找零錢的方法,變出時、分、秒
```c
void setup(){//開新的
  size(1024,400);
  textFont( createFont("標楷體", 80));
}
void draw(){
  background(#3E8DF7);//色碼
  int s = second();   //Value from 0 - 59
  int m = minute();   //Value from 0 - 59
  int h = hour();     //Value from 0 - 23
  textSize(80);
  text( h + ":" + m + ":" + s, 100, 200);
  int total = s + 60*m + 60*60*h;//現在總秒數
  int closeH=17, closeM=40, closeS=0;//下課的精確時間
  int total2=closeS + 60*closeM + 60*60*closeH;//目標總秒數
  int ans = total2 - total;
  text( "剩下幾秒:" + ans, 100, 100);
  int ansH=ans/60/60%60,  ansM=ans/60%60, ansS=ans%60;
  text(ansH  +  ":" + ansM +  ":" + ansS, 100, 300);
}   //數字  字串 數字 字串 數字
```
## 第十四周
### 亂數random()抽個浮點數的數字,並畫出來
```c
void setup(){
   float ans=random(60);//亂數,會是<60的浮點數
   text(ans,20,20);
}
void draw(){
  
}
```
### 用mousePressed互動方式產生整數的亂數
```c
int ans=0;
void setup(){
   size(300,300);
   textSize(30);
}
void draw(){
  background(#435FF7);
  text( ans,150,150);
}
void mousePressed(){//按下去，就互動一次
   ans=(int )random(60); //浮點數不能變整數
}
```
### 洗牌 亂數1，亂數2
```c
int []a={1,2,3,4,5,6,7,8,9,10};
int i1,i2;
void setup(){
   size(400,100);
   textSize(30);
}
void draw(){
   background(#57869B);
   for (int i=0;i<10;i++){
     text( a[i], i*40, 50);      
   }
   rect(i1*40, 50 ,30 ,30);// (x座標 ,  y座標 ,框框長, 框框寬)
   rect(i2*40, 50 ,30 ,30);
}
void mousePressed(){
   i1= (int ) random(10);
   i2= (int ) random(10);
   int t=a[i1]; a[i1]=a[i2];a[i2]=t;
   
}
```
### 大樂透洗牌 配合mousePressed印出數字
```c
int []a= new int [47];
void setup(){
   size(500,200);
   textSize(30);
   for (int i=0;i<47;i++) a[i]=i;
   //讓a[i]的陣列裡，整齊放入正確數字
   for (int i=0;i<1000;i++){//洗1000次牌
        int i1=(int )random(47);
        int i2=(int )random(47);
        int t=a[i1]; a[i1]=a[i2]; a[i2]=t;
   }
}
int n=0;
void draw(){
   background( #57869B);
   for (int i=0;i<n;i++){//印出五個數
      text(a[i] , i*80,100); 
   }
}
void mousePressed(){
	n++;
}
```
### 文字對其中和加個圈圈
```c
int []a= new int [47];
void setup(){
   size(500,200);
   textSize(30);
   for (int i=0;i<47;i++) a[i]=i;
   //讓a[i]的陣列裡，整齊放入正確數字
   for (int i=0;i<1000;i++){//洗1000次牌
        int i1=(int )random(47);
        int i2=(int )random(47);
        int t=a[i1]; a[i1]=a[i2]; a[i2]=t;
   }
}
int n=0;
void draw(){
   background( #57869B);
   textAlign(CENTER,CENTER);//文字對齊: 中，中
   for (int i=0;i<n;i++){//印出五個數
      fill(255); ellipse( i*80+40, 100,55,55);
      fill(0); text(a[i],i*80+40,100);
   }
}
void mousePressed(){
 n++; 
}
```
## 第15周
### 利用奇偶數調顏色
```c
void setup(){
    size(400,200);
}  
void draw(){
   int s=second();
   if (s%2==0) background(#1B6C93);
   else background(#2AD1B9);
}
```
### 倒數計時_利用秒數、餘數、減法,做出10到0的倒數計時
```c
void setup(){
   size(400,200);
   textSize(40);
}
void draw(){
  int s=second();  
  background(#2AD1B9);
  text( 10-s%11 , 100,100);
}
```

### 按滑鼠發出tada
```c
import processing.sound.*;
SoundFile player;
void setup(){
 size(400,200);
 player=new SoundFile(this, "tada.mp3");
 			    ///要下載音樂
}
void draw(){
  background(#2AD1B9);
}
void mousePressed(){
 player.play(); 
}
```
### 用 player的isPlaying()來決定stop()或play()
```c
import processing.sound.*;
SoundFile player;
void setup(){
 size(400,200);
 player=new SoundFile(this, "bell.mp3");
}
void draw(){
  background(#2AD1B9);
}
void mousePressed(){
  if (player.isPlaying() ){
     player.stop(); 
  }
  else{
  player.play();
  }
}
```
### 整合倒數計時+tada
```c
import processing.sound.*;
SoundFile player;
void setup(){
   size(400,200);
   textSize(40);
   player=new SoundFile(this, "tada.mp3");
}
void draw(){
   int s=second();
   background(58,114,191);
   text(10- s%11, 100, 100);
   if (10 -s%11 ==0 && !player.isPlaying() ){
      player.play(); 
   }
}
```
