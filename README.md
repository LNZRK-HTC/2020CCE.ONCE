# 2020CCE.ONCE
# 大一上程式語言

## 第一周正課題目
Hello World : 本題目希望你試著印出 Hello World 並請注意 (1) 字母大小寫, (2) 句子後面的跳行
```c
#include <stdio.h>
int main()
{

printf("Hello World\n");

}
```
## 第一周實習課題目
[printf] 輸出* : 以＊輸出三角形

```c
#include<stdio.h>
int main()
#include<stdio.h>
int main()
{

  printf("          *\n");
   printf("         **\n");
    printf("        ***\n");
     printf("       ****\n");
      printf("      *****\n");
       printf("     ******\n");
        printf("    *******\n");
         printf("   ********\n");
          printf("  *********\n");
           printf(" **********\n");
            printf("***********\n");
           
}
```

## 第二周實習課
平方和 : 輸入3個整數，輸出其平方和。
```c
#include <stdio.h>
int main()
{


 int a;
 int b;
 int c;
 
 scanf("%d %d %d",&a,&b,&c);
 printf("平方和=%d",a*a+b*b+c*c);

}

/*平方和
2 3 4 
平方和=29*/
```

```c
成績計算 : 請輸入國英數三科的成績並算出其總和及平均
****參考結果**** 國文：80 英文：95 數學：65 總和：240 平均：80 
#include <stdio.h>
int main()

{

int a;
int b;
int c;

printf("請輸入國文成績:\n");
scanf("%d",&a);
printf("請輸入英文成績:\n");
scanf("%d",&b);
printf("請輸入數學成績:\n");
scanf("%d",&c);
printf("總和為：%d\n",a+b+c);
printf("總平均為：%d\n",(a+b+c)/3);

}
```


## 實習課補課
程式會考-零錢兌換 : 假設有一換幣機提供了1元、5元、10元三種硬幣的兌換，寫一程式模擬此換幣機的行為，
當使用者輸入要兌換的金額後，算出應支付的最少硬幣個數。 

提示:/*假設有一換幣機提供了1元、5元、10元三種硬幣的兌換，寫一程式模擬此換幣機的行為，
當使用者輸入要兌換的金額後，算出應支付的最少硬幣個數。
找回:10元XX個    5元XX個    一元XX個*/
```c
#include <stdio.h>
int main()
{
int a;
printf("輸入:");
scanf("%d",&a);
printf("找回:10元%d個、5元%d個、一元%d個",a/10,a%10/5,a%5/1);

}
```


BMI : 請任意輸入體重(k.g.)與身高(M)計算其BMI值公式：BMI=體重/身高2(求到小數點第二位)
若BMI< 18.5 則輸出"太瘦囉" 若 18.5<=BMI<24 則輸出 "標準喔!!" 若 BMI>24 則輸出 "太胖囉"
提示:/*請輸入身高(公尺):1.68
  請輸入體重(公斤):40
  BMI=10.00
  太瘦囉*/
```c
#include <stdio.h>
float main()
{

float a,b,bmi;

printf("請輸入身高(公尺):");
scanf("%f",&a);

printf("請輸入體重(公斤):");
scanf("%f",&b);

bmi=b/(a*a);

printf("BMI=%.2f\n",bmi);


if(bmi<18.5)
printf("太瘦囉");


else if(18.5<=bmi&&bmi<24)
printf("標準喔");


else 
printf("太胖囉");

}
```

## 第三周正課
兩數相加 : 輸入兩整數，輸出兩數之和。
```c
#include <stdio.h>
int main()
{

int a,b;
scanf("%d %d",&a,&b);
printf("%d",a+b);

}
```
## 第五周正課
用if堆疊出金字塔
```c
#include<stdio.h>
int main()
{
int a;
scanf("%d",&a);
if(a>0)printf("  *\n");
if(a>1)printf(" ***\n");
if(a>2)printf("*****\n");
}
```
## 第五周實習課
三角形判斷 : 請輸入三角形三邊邊長(整數),其中第一個輸入的邊長為最長邊. 
請跟據三邊長,判斷是何種三角形(鈍角,銳角或直角)? 
例: 7 3 2 錯誤 例: 5 4 3 直角 例: 13 12 5 直角 例: 5 3 3 鈍角
三角形成立: 兩邊長的和要大於第三邊
例如:變數a,b,c(a為邊長最長邊)
直角:兩短邊平方和==最長邊平方和
銳角:兩短邊平方和>最長邊平方和
鈍角:兩短邊平方和<最長邊平方和

***參考結果****
6 3 2
錯誤

6 3 4
鈍角*/

```c
#include<stdio.h>
int main()
{
	int a,b,c;
	scanf("%d%d%d",&a,&b,&c);


	if(b+c<a)
	printf("錯誤");

	else if(b*b+c*c==a*a)
	printf("直角");
	
	else if(b*b+c*c>a*a)
	printf("銳角");
	
	else 
	printf("鈍角");

}
```

用電度數 : 輸入用電度數 R，計算電費 P。未超過 20°的部份只收基本費 80 元；
超過 20°在 50°以內的部份每度加收 3 元；超過 50°在 100°以內的部份每度加收 5 元；
超過 100°以上的部份，每度加收 8 元。
```c
#include<stdio.h>
int main()
{
	int R;
	scanf("%d",&R);
	
	if(R<=20)
	printf("P=%d\n",80+(R-20)*3);
	
	else if(20<R&&R<=50)
	printf("P=%d\n",170+(R-50)*5);

	else if(50<R&&R<=100)
	printf("P=%d\n",170+(R-50)*5);
	
	else
	printf("P=%d\n",420+(R-100)*8);

}
```
[if-else] 溫度轉換 : 溫度轉換（攝氏<-->華氏）  
//1021-03-03  
//溫度轉換（攝氏<-->華氏）  
//f = 9 * c / 5  + 32;  
// c = ( f - 32 ) * 5 / 9;  
```c
#include <stdio.h>
int main( void )
{
    int t,f,c;
    printf( "Temperature Conversion: \n" );
    printf( "Enter 0 to convert C to F\n" );
    printf( "Enter 1 to convert F to C\n" );
    printf( "Enter 0 or 1: " );
    scanf( "%d", &t );

    if(t==0)
    {
    printf("Enter Celsius: ");
    scanf("%d\n",&c);
    printf("Fahrenheit: %d\n",f=9*c/5+32);
    }
   
   else
    {
    printf("Enter Fahrenheit : ");
    scanf("%d\n",&f);
    printf(" Celsius : %d\n",(f-32)*5/9);
    }

    return 0;
}
```
## 第六周正課
級數: 一次方和 : 輸入一整數n，輸出1+2+3+4+...+n。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);

	int ans=0;
	for(int i=1;i<=n;i++)
	{
		ans += i;
	}
	printf("%d",ans);

}
```

級數: 平方和 : 輸入一整數n，輸出12+22+32+42+...+n2。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	int ans=0;
	for(int i=1;i<=n;i++)
	{
		ans += i*i;
	}
	printf("%d",ans);


}
```

級數: 三方和 : 輸入一整數n，輸出13+23+33+43+...+n3。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	int ans=0;
	for(int i=1;i<=n;i++)
	{
		ans += i*i*i;
	}
	printf("%d",ans);
}
```

級數: 四方和 : 輸入一整數n，輸出14+24+34+44+...+n4。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	int ans=0;
	for(int i=1;i<=n;i++)
	{
		ans += i*i*i*i;
	}
	printf("%d",ans);

}
```

級數: 1*2+2*3+3*4+... : 考慮數列 1*2, 2*3, 3*4 , 4*5, 5*6, 6*7,... 
輸入一整數n，輸出該數列前n項之和。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	int ans=0;
	for(int i=1;i<=n;i++)
	{
		ans +=i*(i+1);
	}
	printf("%d",ans);
}
```

級數: 1*n+2*(n-1)+3*(n-2)+... : 輸入一整數n，
輸出 1*n+2*(n-1)+3*(n-2)+4*(n-3)+...+(n-1)*2+n*1。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	int ans=0;
	for(int i=1;i<=n;i++)
	{
		ans += i*(n-(i-1));
	
	}

	printf("%d",ans);
}
```

## 第六周實習課
請利用for迴圈輸出下列圖形 ****** 
```c
#include <stdio.h>
int main(void)
{
    int i;
	
	
	for(int i=1;i<=6;i++)
	{
		
		printf("*");
	}

    return 0;
}
```
撰寫程式從鍵盤讀入n,利用迴圈求1到n的和。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	int ans=0;
	for(int i=1;i<=n;i++)
	{
		ans += i;
	
	}
	printf("%d",ans);

}
```
階乘計算 : 輸入n(>=0)，輸出 n!
```c
#include <stdio.h>
int main()
{
	int n=1,ans=1;
	scanf("%d",&n);
	for(int i=1;i<=n;i++)
	{
		ans *= i;
	}
	printf("%d",ans);
}
```

平均成績 : 輸入:人數以及每個學生的分數輸出:全班平均成績(至小數第2位) 
例: 7 65 39 54 88 91 74 63 67.71 
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	int sum=0;
	for(int i=1;i<=n;i++)
	{
		int s;
		scanf("%d",&s);
		sum =sum+s;
	}
	float avg;
	avg=(float) sum/n;
	printf("%.2f",avg);
}
```
平行四邊形 : 輸入，利用for迴圈輸出平行四邊形。執行範例如下：請輸入大小:4 
```c
#include <stdio.h>
int main( void )
{
   int i,j;
   int n;

   printf("請輸入大小:\n");
   scanf("%d",&n);
   
   for(i=1; i<=n;i++)//幾行
   {
   		for(j=1;j<=i;j++)//每行裡面的東西
   			printf(" ");
   		for(j=1;j<=n;j++)//同上
   			printf("*");
   		printf("\n");
   }
   
   	
   return 0;
}
```
## 第七周實習課
[while2] 以*輸出直角三角形 : 輸入正整數n，用while輸出直角三角形。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	int i=1;
	while(i<=n)//控制行數
	{
		int j=1;
		while(j<=n)//要印出幾個
		{
			if(j<=n-i)printf(" ");
			
			else printf("*");
			j++;
		}
		printf("\n");
		i++;
	}

}
```
[for2] 以*輸出直角三角形 : 輸入正整數n，用for輸出直角三角形。
```c
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	for(int i=1;i<=a;i++)
	{
		for(int j=1;j<=a-i;j++)
		{
			printf(" ");
		}
		for(int j=1;j<=i;j++)
		{
			printf("*");
		}
	printf("\n");
	}
}
```
印出等差數列 : 輸入首項、公差與項數ｎ，輸出前 n 項。
/*等差級數列印
輸入首項、公差、項數，輸出前n項
*/
```c
#include <stdio.h>
int main()
{
	int a,d,n;
	scanf("%d%d%d",&a,&d,&n);
	int an=a;
	printf("%d",a);
	for(int i=1;i<n;i++)
	{
		an+=d;
		printf(",%d",an);
	}
```
 N 到 M 乘法表 : 請輸入最小與最大兩值 n 與 m 產生乘法表例: 輸入 3 6 3x 3= 9 
 3x 4=12 3x 5=15 3x 6=18 4x 3=12 4x 4=16 4x 5=20 4x 6=24 5x 3=15 5x 4=20 
 5x 5=25 5x 6=30 6x 3=18 6x 4=24 6x 5=30 6x 6=36  
  /*
請輸入最小與最大兩值 a 與 b
產生乘法表
例: 輸入 3 6
 3x 3= 9   3x 4=12   3x 5=15   3x 6=18   
 4x 3=12   4x 4=16   4x 5=20   4x 6=24
 5x 3=15   5x 4=20   5x 5=25   5x 6=30   
 6x 3=18   6x 4=24   6x 5=30   6x 6=36
*/

```c
#include <stdio.h>
int main()
{
	int n,m;
	scanf("%d%d",&n,&m);
	for(int i=n;i<=m;i++)
	{
		for(int j=n;j<=m;j++)
		{
			printf("%2dx%2d=%2d  ",i,j,i*j);
		}
		printf("\n");
	}

}

}
```

## 第十周正課
百數反印 : 輸入100個正整數，反向印出此100個數。
```c
#include <stdio.h>
int main()
{
	int a[100];
	for(int i=0;i<100;i++)
	{
		scanf("%d",&a[i]);
	}
	for(int i=99;i>=0;i--)
	{
		printf("%d\n",a[i]);
	}
}
```
百數最大值 : 輸入一百個正整數，印出最大值及此一百個數。
```c
#include <stdio.h>
int main()
{
	int a[100];
	int big=0;
	for(int i=0;i<100;i++)
	{
		scanf("%d",&a[i]);
		if(a[i]>big)big=a[i];
	}
	printf("%d\n",big);
	
	for(int i=0;i<100;i++)
	{
		printf("%d\n",a[i]);
	}
}
```
前三名分數 : 輸入:人數以及每個學生的分數輸出:全班最高分前三名績(由高而低) 提示:
宣告三個變數來記錄第1,2,3名分數, 每次新輸入一個分數,就與原來前3名比較,必要時進行替換. 
如果新輸入的分數高於原來第1名,則第2名變成第3名,則第1名變成第2名,新輸入的分數變成第1名;
如果新輸入的分數高於原來第2名,則第2名變成第3名,新輸入的分數變成第2名; 如果新輸入的分數
高於原來第3名,則新輸入的分數代掉第3名. 例: 7 56 83 41 28 91 67 95 95,91,83 
/*
輸入:人數以及每個學生的分數
輸出:全班最高分前三名績(由高而低)

提示: 宣告三個變數來記錄第1,2,3名分數,
     每次新輸入一個分數,就與原來前3名比較,必要時進行替換.
     如果新輸入的分數高於原來第1名,則第2名變成第3名,則第1名變成第2名,新輸入的分數變成第1名;
     如果新輸入的分數高於原來第2名,則第2名變成第3名,新輸入的分數變成第2名;
     如果新輸入的分數高於原來第3名,則新輸入的分數代掉第3名.

****參考結果*****

7 56 83 41 28 91 67 95
95,91,83

```c
#include <stdio.h>
int main()
{
	int n;
	int a[100];
	int big1=0,big2=0,big3=0;
	scanf("%d\n",&n);
	for(int i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
		if(a[i]>big1)
		{
			big3=big2;
			big2=big1;
			big1=a[i];
		}
		else if(a[i]>big2)
		{
			big3=big2;
			big2=a[i];
		}
		else if(a[i]>big3)
		{
			big3=a[i];
		}
	}
	printf("%d,%d,%d",big1,big2,big3);
}
```
質數判別 : 輸入一個正整數，如果是質數，則輸出 Yes，如果不是，則輸出 No。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	int a=0;
	for(int i=2;i<n;i++)
	{
		if(n%i==0)a=1;
		
	}
	if(n==1)printf("No");
	else if(a==0)printf("Yes");
	else printf("No");
}
```
## 第十周實習課
do...while]計算蝸牛爬牆天數 : 小學的數學問題，有一隻蝸牛每天白天能爬5公尺晚上會往下滑2公尺，
請同學任意輸入高牆的高度，計算要幾天蝸牛才能爬到頂端(需要超越過頂端才算)？請使用do...while的結構思考。
```c
#include <stdio.h>
int main ( void )
{
	int h,day=0;
	printf("請輸入蝸牛欲爬行的高度：");
	scanf("%d",&h);
	
	do
	{
		day++;	
		if((h=h-5)>=0)
		h=h+2;
		
	}while(h>0);
	
    printf("%d天可爬到頂端",day);
}
```
陣列資料反轉 : 陣列資料反轉輸入整數n(最大30)，再輸入n個整數，將其反轉順序輸出。
```c
#include <stdio.h>
int main()
{
	int n,a[30];
	scanf("%d",&n);
	for(int i=0;i<n;i++)
	{
		scanf("%d\n",&a[i]);
	}
	printf("\n\n");
	for(int i=n-1;i>=0;i--)
	{
		printf("%d\n",a[i]);
	}
}
```
找出高分與低分 : 輸入人數n,再輸入n個分數, 先找出所有>=80分的分數, 再找出所有<40分的分數
```c
#include <stdio.h>
int main()
{
	int n,a[100];
	scanf("%d",&n);
	printf("\n");
	for(int i=0;i<n;i++)
	{
		scanf("%d\n ",&a[i]);
		if( a[i] >= 80)
		{
			printf("%d ",a[i]);
		}
	}
		printf("\n");
	for(int i=0;i<n;i++)
	{
		if( a[i] < 40)
		{
			printf("%d ",a[i]);
		}
	}
	
}
```
及格與不及格 : 及格與不及格, 輸入個數,再輸入分數, 其中<0 與 >100 不計需要重新輸入, 輸出所有及格與不及格的分數.
```c
#include <stdio.h>
int main()
{
	int n,a[100];
	scanf("%d",&n);
	printf("\n");
	for(int i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
		if(a[i]<0||a[i]>100)
		i--;
	}
	printf("pass:");
	for(int i=0;i<n;i++)
	{
		if(a[i]>=60)printf("%4d",a[i]);
	}
	printf("\n");
	printf("down:");
	for(int i=0;i<n;i++)
	{
		if(a[i]<60)printf("%4d",a[i]);
	}
}  
```
## 第十一周正課
陣列資料反轉 : 陣列資料反轉輸入整數n(最大30)，再輸入n個整數，將其反轉順序輸出。
```c
#include <stdio.h>
int main()
{
	int a[30];
	int n;
	scanf("%d",&n);
	for(int i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
	}
	for(int i=n-1;i>=0;i--)
	{
		printf("%d\n",a[i]);
	}
	
}
```
質數判別 : 輸入一個正整數，如果是質數，則輸出 Yes，如果不是，則輸出 No。
```c
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	int a=0;
	for(int i=2;i<n;i++)
	{
		if(n%i==0)a=1;
	}
	if(n==1)printf("No");
	else if(a==0)printf("Yes");
	else printf("No");
}
```
## 第十一周實習
股票最佳買點與賣點 : 輸入:n 以及n天的股價輸出:最佳買點與賣點,以及獲利
例. 10 5 7 10 8 4 6 9 11 14 10 最大利潤=14-4=10  
```c
#include <stdio.h>
int main()
{
	printf("請按任意鍵繼續 . . . \n");
	int n,p=0,buy,sale,a[100];
	scanf("%d",&n);
	for(int i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
	}
	for(int i=0;i<n;i++)
	{
		for(int j=i+1;j<n;j++)
			if(a[j]-a[i]>p)
			{
				buy=a[i];//低
				sale=a[j];//高
				p=a[j]-a[i];
			}
		}
	
	printf("最大利潤=%d-%d=%d\n",sale,buy,p);
}
```
矩陣順時針旋轉 : 輸入M 與 N, 再輸入MxN 的2-D陣列, 將此一陣列順時鐘旋轉90度之後輸出
```c
#include <stdio.h>
int main()
{
	int m,n,a[30][30];
	scanf("%d%d",&m,&n);
	for(int i=0;i<m;i++)
	{
		for(int j=0;j<n;j++)
		{
			scanf("%d",&a[i][j]);
		}
	}
	
	printf("\n");
	
	for(int i=0;i<n;i++)
	{
		for(int j=0;j<m;j++)
		{
			printf("%2d ",a[m-j-1][i]);
		}
		printf("\n");
	}
	
}
```
矩陣乘法 : 輸入n,再輸入兩個nxn的整數矩陣, 將兩個矩陣相乘後輸出
```c
#include <stdio.h>
int main()
{
	int a[10][10],b[10][10],c[10][10];
	int i,j,k,n;
	scanf("%d",&n);
	
	for(i=0;i<n;i++)
	{
		for(j=0;j<n;j++)
		{
			scanf("%d",&a[i][j]);
		}
	}
	
	for(i=0;i<n;i++)
	{
		for(j=0;j<n;j++)
		{
			scanf("%d",&b[i][j]);
		}
	}
	
	for(i=0;i<n;i++)
	{
		for(j=0;j<n;j++)
		{
			c[i][j]=0;
			for(k=0;k<n;k++)
			{
				c[i][j]+=a[i][k]*b[k][j];
			}
		}
	}
	for(i=0;i<n;i++)
	{
		for(j=0;j<n;j++)
		{
			printf("%3d ",c[i][j]);
		}
		printf("\n");
	}

}
```
## 第十二周正課
百數排序-泡泡排序法 : 輸入一百個正整數，將這些數依照泡泡排序法從小排到大。
```c
#include <stdio.h>
int main()
{
	int a[100];
	for(int i=0;i<100;i++)
	{
		scanf("%d",&a[i]);
	}
	for(int j=0;j<100;j++)
	{
		for(int i=0;i<100-1;i++)
		{
			if(a[i]>a[i+1])
			{
				int temp=a[i];
				a[i]=a[i+1];
				a[i+1]=temp;
			}
		}
	}
	for(int i=0;i<100;i++)
	printf("%d\n",a[i]);
}
```
## 第十三周正課
矩陣加法 : 矩陣加法

會先輸入正整數 n, m (都不大於10), 表示想要處理 n*m 的矩陣。
接著出現2個 n*m 的矩陣 (矩陣A 及 矩陣B) 裡面每個數字。
```c
#include <stdio.h>
int a[10][10],b[10][10],c[10][10];
int main()
{
	int n,m;
	scanf("%d%d",&n,&m);
	
	for(int i=0;i<n;i++)
	{
		for(int j=0;j<m;j++)
		{
			scanf("%d",&a[i][j]);
		}
	}
	
	for(int i=0;i<n;i++)
	{
		for(int j=0;j<m;j++)
		{
			scanf("%d",&b[i][j]);
		}
	}
	
	for(int i=0;i<n;i++)
	{
		for(int j=0;j<m;j++)
		{
			c[i][j]=a[i][j]+b[i][j];
			printf("%d ",c[i][j]);
		}
		printf("\n");
	}
}
```
## 第十三周實習課
計算1到10的整數平方 : 請撰寫一square的函數來計算1~10的整數平方
```c
#include <stdio.h>
void square()
{
	int i;
	for(i=1;i<=10;i++)
	{
		printf("%d ",i*i);
	}
	printf("\n");

}
int main()
{
	square();
}


/*#include <stdio.h>
int square(int x)
{
	return x*x;
}
int main()
{
	int i;
	for(int i=1;i<=10;i++)
	{
		printf("%d",square(i));
	}
	printf("\n");
}*/
```
函式-三角形列印 : 請輸入一值傳入函式中，並列印出此數值階層的倒三角形。
```c
#include <stdio.h>
void triangle(int n);
int main()
{
	int n;
	printf("請輸入一個數:");
	scanf("%d",&n);
	triangle(n);
	
}
void triangle (int n)//印出階層三角形
{
	int i,j;
	for(i=0;i<n;i++)//控制行數
	{
		for(j=0;j<i;j++)
		{
			printf(" ");//印空格
		}
		for(j=n;j>i;j--)
		{
			printf("%d",j);//印值
		}
		printf("\n");
	}
}
```
Function-反轉數字 : 請撰寫一函式(Fun)，傳回整數參數值的反轉。
舉例: 參數為9876，反轉後為6789。 參數為98765，反轉後為0。 
(注意:輸入的值介於1~9999，超過請回傳0)
```c
#include <stdio.h>
int Fun(int n)
{
	int p,num=0;
	if(n<1 || n>9999)
	{
		return 0;
	}
	else
	while(n>0)//終止n=0
	{
		p=n%10;
		num=num*10+p;
		n=n/10;
	}
	return num;
}
int main()
{
	int n;
	printf("請在1到9999輸入一個數字:");
	scanf("%d",&n);
	printf("數字反轉為:%d\n",Fun(n));
	
}
```
## 第十四周實習課
遞迴計算 a+(a+1)+(a+2)+...+b : 輸入 a 與 b, 以遞迴方式計算 a+(a+1)+(a+2)+...+b, 
如果 a>b, 結果為0. 如果 a<=b , 則先遞迴計算出 (a+1)+...+b，最後再加上 a． 例. 3 7 25 
```c
#include <stdio.h>
int sum(int a,int b)
{
	if(a>b) return 0;
	else 
	return sum(a+1,b)+a;
}
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("%d",sum(a,b));
}
```
遞迴函數計算N! : 遞迴函數計算N! 例. 9 362880 例. 0 1 例. 5 120 
```c
#include <stdio.h>
int fact(int n)
{
	if(n<=1) return 1;
	else return fact(n-1)*n;
}
int main()
{
	int n;
	scanf("%d",&n);
	printf("%d",fact(n));
}
```
數字反轉(recursion) 
/*禁止使用土法煉鋼*/
```c
#include <stdio.h>
void Reverse(int n);
int main()
{
	int n;
	scanf("%d",&n);
	Reverse(n);
}
void Reverse(int n)
{
	printf("%d",n%10);
	if(n>=10)Reverse(n/10);
}
```
階乘函數計算n取m的組合數 : 請設計一個計算n!函數 fact, 配合主程式來計算n取m的組合數.
註: n取m的組合數為 (1) n!/(m!*(n-m)!), 0<=m<=n (2) 0 , 其他 例. 4 2 6 例. 5 3 10 例. 4 -1 0 
```c
#include <stdio.h>
int fact(int n)//計算階層
{
	int p=1;
	for(int i=1;i<=n;i++)//跑n次
	
		p=p*i;
		return p;
	
}
int main()
{
	int n,m,p;
	scanf("%d%d",&n,&m);
	if(0<=m&&m<=n)
	p=fact(n)/fact(m)/fact(n-m);
	else p=0;
	printf("%d",p);
}
```
## 第十五周正課
最大公因數(2數) : 輸入2整數，輸出其最大公因數。
```c
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	if(a<0)a=-a;
	if(b<0)b=-b;
	

	int c=a%b;
	while(c=a%b)
{
		a=b;
		b=c;
		c=a;
}
	printf("%d",b);
}
```
遞迴函數計算N! : 遞迴函數計算N! 例. 9 362880 例. 0 1 例. 5 120 
```c
#include <stdio.h>
int fan(int n)
{
	if(n<1)return 1;
	else return fan(n-1)*n;
}
int main()
{
	int n;
	scanf("%d",&n);
	printf("%d",fan(n));
}
```

前置印出 n! 遞迴的計算式 : 前置印出 n! 遞迴的計算式 例. 5 5*4*3*2*1=120 例. 0 1=1
```c
#include <stdio.h>
int p1(int n)
{
    if(n<=0)return 1;
    else return p1(n-1)*n;
}

void p2(int n)
{
    if(n==1)
    {
        printf("%d=",n);
    }
    else
    {
        printf("%d*",n);
        p2(n-1);
    }
}

int main()
{
    int n;
    scanf("%d",&n);
    p2(n);
    printf("%d",p1(n));
    
}
```
