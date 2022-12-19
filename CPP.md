`CPP` 学习教程

##       基本语法

   变量：数据类型 变量名 = 变量初始值

   常量：1

```c++
.#define   常量名 常量值（注意：定义在函数体外）
```



                  2.  const  数据类型 常量名 = 常量值（注意：定义在函数体内）

### **标识符命名规则**

1.标识符不能是关键字

2.标识符（字母，下划线，数字）

3.标识符的第一个不能是数字，只能是字母和下划线

4.标识符不可以是关键字

5.标识符区分大小写

### **数据类型**

数据类型存在的意义:给变量分配合适的内存空间

整型：1.短整型（-32768~323767）

​            2.整型

​            3.长整型

​            4.长长那个整型

### **`sizeof`关键字**

作用：可以统计数据类型所占内存大小

语法：`sizeof`(数据类型/变量名)

`og：cout<<“short占用的内存空间为”<<sizeof(short)<<endl;`

### **整型数据**

单精度：float(4个字节)

注意：使用float时如：`float B=3.14f`;(注意初始值后面不要忘记加小f)

双精度：double(8个字节)

### **字符型**

作用： 字符型常量用于显示字符

语法：char ch = 'a';

### **注意，一次只能创建一个字符。**

查看字符变量所占内存大小：`cout<<"char 字符型变量所占的内存"<<sizeof(char)<<endl;`

注意，在`cout`输出时，只能要单引号。

将字符型强转成整型：（int）ch然后在输出，就可以查看ASCII值。

### **转义字符**

换行符：\n

水平制表：\t（补齐8个字符）

### **字符串型**

C语言风格：`char str[] ="hello";`

`cpp`风格:`string str="hello";`

注意：在使用`cpp`风格时，要加一个使用字符串的头文件（`#include<string>`)

### **布尔类型`bool`**

创建`bool`数据类型：`bool flag=true\false；`

`true=1，false=0`

查看布尔数据类型的所占空间大小：`cout<<"bool所占大小为"<<sizeof(bool)<<endl`;

### **数据的输入**

作用：用于从键盘获取数据

`cin>>变量`

基本格式举例：`string str=“hello";`

`cout<<"请给字符串str赋值"<<endl;`

`cin>>str;`

`cout<<"字符串str="<<str<<endl;`

注意：布尔类型输出时，除了0输出的是0，其他书输出的都是1；

### **递增运算符**

#### **后递增运算：**

****

```
  `int a1 = 10;`

​	`int a2 = a1++ * 10;`
`​	cout << "a1=" << a1<<endl;`
`​	cout << "a2=" << a2<<endl;`
```

运算结果a1=11，a2=100；a1先去运算再去+1；

#### 	**前递增运算：**

```
    `int b1 = 10;`
`​	int b2 = ++b1 * 10;`
`​	cout << "b1=" << b1 << endl;`
`​	cout << "b2=" << b2 << endl;`
```

运算结果`b1=11，b2=110；b1`先加+1，然后再带进公式计算；

### **比较运算符**

| 运算符 | 术语     | 示例  | 结果 |
| ------ | -------- | ----- | ---- |
| ==     | 相等于   | 4==3  | 0    |
| ！=    | 不等于   | 4！=3 | 1    |
| <      | 小于     | 4<3   | 0    |
| >      | 大于     | 4>3   | 1    |
| <=     | 下于等于 | 4<=3  | 0    |
| >=     | 大于等于 | 4>=3  | 1    |

```
``int a = 10;`
	`int b = 20;`
	`cout << (a == b) << endl;`//输出结果为0
	`cout << (a != b) << endl;`//输出结果为1
	`cout << (a > b) << endl;`//输出结果为0
	`cout << (a < b) << endl;`//输出结果为1
	`cout << (a >= b) << endl;`//输出结果为0
	`cout << (a <=b) << endl;`//输出结果为1
```



### **逻辑运算符**

| 运算符 | 术语 | 示例   | 结果                                               |
| ------ | ---- | ------ | -------------------------------------------------- |
| ！     | 非   | ！a    | 如果a为真，则！a为假，反之同理                     |
| &&     | 与   | a&&b   | 只有a，b同为真，结果才为真，反之不成立             |
| \|\|   | 或   | a\|\|b | a或者b一者为真，则为真，两个同时为假，a\|\|b才为假 |

注意：`cpp中只有0为假，其余都是为真`。

### **选择结构**

#### if语句：1.单行if语句：K

```
`int score = 0;`
	`cout << "请输入你的分数：" << score << endl;`
	`cin >> score;`
	`cout << "你输入的分数为：" << score<<endl;`
	`if (score > 600)`
	`{`
		`cout << "恭喜你！" << endl;`
	}
```

注意：if条件后面不要加“；”**`

#### 2.多行if条件语句：

```
``int score = 0;`
	`cout << "请输入你的分数：" << score << endl;`
	`cin >> score;`
	`cout << "你输入的分数为：" << score<<endl;`
	`if (score > 600)`
	`{`
		`cout << "恭喜你！" << endl;`
	`}`
	`else`
	`{`
		`cout << "没关系，再接再厉" << endl;`
	}`
```



#### **3.多条件if语句：**

if（条件1）{条件1满足执行的语句}else if（条件2）{条件2满足执行的语句}...else{都不满足条件执行的语句}

```
``int score = 0;`
	`cout << "请输入你的分数：" << score << endl;`
	`cin >> score;`
	`cout << "你输入的分数为：" << score<<endl;`
	`if (score > 600)`
	`{`
		`cout << "恭喜你上一本！" << endl;`
	`}`
	`else if(score>500)`
	`{`
		`cout << "恭喜你，上二本" << endl;`
	`}`
	`else if (score > 400)`
	`{`
		`cout << "恭喜你，上三本" << endl;`
	`}`
	`else`
	`{`
		`cout << "恭喜你，获得良田一亩！" << endl;`
	}`
```

#### 4.嵌套条件if

```
``int score = 0;`
	`cout << "请输入你的分数：" << score << endl;`
	`cin >> score;`
	`cout << "你输入的分数为：" << score<<endl;`
	`if (score > 600)`
	`{`
		`cout << "恭喜你上一本！" << endl;`
		`if (score > 700)`
		`{`
			`cout << "恭喜你考上了清华大学" << endl;`
		`}`
		`else if (score > 650)`
		`{`
			`cout << "恭喜你考上了北京大学" << endl;`
		`}`
		`else`
		`{`
			`cout << "恭喜你考上人民大学" << endl;`
		`}`
	`}`
	`else if(score>500)`
	`{`
		`cout << "恭喜你，上二本" << endl;`
	`}`
	`else if (score > 400)`
	`{`
		`cout << "恭喜你，上三本" << endl;`
	`}`
	`else`
	`{`
		`cout << "恭喜你，获得良田一亩！" << endl;`
	`}`
	return 0;`
```

#### 小猪比体重问题

```
#include<iostream>
using namespace std;
int main()
{
	int p1 = 0;
	int p2 = 0;
	int p3 = 0;
	cout << "请分别输入小猪1的体重:" << endl;
	cin >> p1;
	cout << "请分别输入小猪2的体重:" << endl;
	cin >> p2;
	cout << "请分别输入小猪3的体重:" << endl;
	cin >> p3;
	cout << "小猪1的体重为：" <<p1<< endl;
	cout << "小猪2的体重为：" <<p2<<endl;
	cout << "小猪3的体重为：" <<p3<<endl;
	if (p1 > p2)
	{
		if (p1 > p3)
		{
			cout << "小猪1是最重的" << endl;
		}
		else
		{
			cout << "小猪3是最重的" << endl;
		}
	}
	else
	{
		if (p2 > p3)
		{
			cout << "小猪2是最重的" << endl;
		}
		else
		{
			cout << "小猪3是最重的" << endl;
		}
	}

​	

	return 0;

}
```

### **三目运算符操作**

```
#include<iostream>
using namespace std;
int main()
{
	int a = 10;
	int b = 20;
	int c = 0;
	c = a > b ? a : b;
	cout << "c=" << c << endl;
	(a > b ? a : b) = 100;
	cout << "a=" << a << endl;
	cout << "b=" << b << endl;
	cout << "c=" << c << endl;
	return 0;

}
```

**注意：三目运算符返回的是变量，可以重新赋值；**

### `swith循环语句`

**（给电影打分循环）**

```c++
int score = 0;
	cout << "请您给电影打分" << endl;
	cin >> score;
	cout << "您给电影的打分为：" <<score<< endl;
	switch (score)
	{
	case 10:
			cout << "电影是经典电影" << endl;
			break;
	case 9:
		cout << "电影是经典电影" << endl;
		break;
	case 8:
		cout << "电影是好电影" << endl;
		break;
	case 7:
		cout << "电影是好电影" << endl;
		break;
	case 6:
		cout << "电影是一般的电影" << endl;
		break;
	case 5:
		cout << "电影是一般的电影" << endl;
		break;
	default:
		cout << "这是烂片" << endl;
		break;
	}


```

### **生成随机数的函数：**

`rand（）%100`表示生成0到99的总共100个数字组成的随机数。

### **while循环语句**

随机生成一个数猜的去猜：

```c++
#include<iostream>
#include<ctime>
using namespace std;
int main()
{
	srand((unsigned int)time(NULL));//添加随机数种子，防止每次生成的随机数都是同一个。但要注意使用#include<ctime>的头文件

	int num = rand() % 100 + 1;
	int val = 0;
	cout << "请你猜一个数" << endl;
	while (1)
	{
		cin >> val;
		if (val > num)
		{
			cout << "猜大了" << endl;
		}
		else if (val < num)
		{
			cout << "猜小了" << endl;
		}
		else
		{
			cout << "你猜对了" << endl;
			break;
		}
	
	}
	return 0;

}


```

### **`do while循环语句`**

与while循环的区别就是先执行一一遍循环，再来判断是否符合条件。

```c++
int num = 0;
do
{
	cout << num << endl;
	num++;

} while (num < 10);
```

其输出结果就是0，1，2.，3，4，5，6，7，8，9

**水仙花数的求解**

```
#include<iostream>
using namespace std;
int main()
{
	int num = 100;
	do 
	{
		int a = 0;
		int b = 0;
		int c = 0;
		a = num % 10;
		b = num / 10 % 10;
		c = num / 10;
		if (a*a*a+b*b*b+c*c*c== num)
		{
			cout << num << endl;
		}
		num++;
	} while (num < 1000);
	system("pause");
	return 0;
}
```

### **for循环语句**

![image-20221019152503854](C:\Users\lee\AppData\Roaming\Typora\typora-user-images\image-20221019152503854.png)

注意循环语句执行顺序：`int i=0`;语句从头到尾只执行一次

**案例一：酒吧游戏:"7"的游戏，就是个位或者十位含有7，和7的倍数的就敲一下桌子。**

![image-20221019153121195](C:\Users\lee\AppData\Roaming\Typora\typora-user-images\image-20221019153121195.png)

	for (int i = 1; i <= 100; i++)
	{
		if (i % 7 == 0 || i % 10 == 7 || i / 10 == 7)
		{
			cout << "敲桌子" << endl;
		}
		else
		{
			cout << i<< endl;
		}
	}

**案例二：打印星图的游戏**

```
#include<iostream>
using namespace std;
int main()
{
	for (int i = 0 ;i < 10; i++)
	{
		for (int j = 0;j < 10; j++)
		{
			cout << "* ";
		}
		cout << endl;
	}
	system("pause");
	return 0;
}        注意：外循环执行一次，内循环执行一周。
```

### 跳转语句

break的使用时机：

1.出现在switch中:

```
cout << "选择副本难度" << endl;
	cout << "1、普通" << endl;
	cout << "2、中等" << endl;
	cout << "3、困难" << endl;
	int select = 0;
	cin >> select;
	switch (select)
	{
	case 1:
		cout << "普通难度" << endl;
		break;
	case 2:
		cout << "中等难度" << endl;
		break;
	case 3:
		cout << "困难难度" << endl;
		break;
	default:
		break;
	}




```

2.出现在for循环语句中

```
for (int i = 0; i < 10; i++)
	{
		if (i == 5)
		{

break;

}

cout<<i<<endl;

}
```



3.出现在for循环中打印“*”符号的循环中

```
for (int i = 0; i < 10; i++)
	{
		for (int j = 0; j < 10; j++)
		{
			if (j == 5)
			{
				break;
			}
			cout << " *";
		}
		cout << endl;

}
```

### continue语句

作用：可以筛选数字。

于break循环的区别，break是直接结束循环，而`contiune`是执行到`contiune`语句的时候就不往后执行，而是重新开始一次新的循环，并且每次循环都是到`contiune`结束。

	for (int i = 0; i < 100; i++)
	{
		if (i % 2 == 0)
		{
			continue;
		}
		cout << i << endl;
	}//这个循环语句就是筛选出1到一百的奇数。

### goto无条件跳转语句

无条件的跳转到标记点：

```
cout << "1" << endl;
	cout << "2" << endl;
	goto FLAG;
	cout << "3" << endl;
	cout << "4" << endl;
	FLAG:
	cout << "5" << endl;
```

运行结果为：1、2、5；其直接跳过了3和4；

### 数组

三种定义方法：

1.

```
int arr[5];
	arr[0] = 0;
	arr[1] = 10;
	arr[2] = 20;
	arr[3] = 30;
	arr[4] =40;
	cout << arr[0] << endl;
```

2.

```
int arr2[5] = { 0,1,2,3,4 };
	cout << arr2[0]<<endl;
```

3.

	int arr3[] = { 10,20,55,45,27,87 };
	cout << arr3[3] << endl;//其输出结果为45；

数组的一些基本操作：

```
int arr3[] = { 10,20,55,45,27,87 };
	cout << sizeof(arr3)<< endl;
	cout << sizeof(arr3[0])<< endl;
	cout << "整个数组所占空间大小为" << sizeof(arr3) << endl;
	cout << "数组的首地址为： " << arr3 << endl;//可以在arr3前面加一个（int）强转类型转为16进制
	cout << "第一个数组的首地址" << (int)&arr3[0] << endl;
```

数组元素逆置：

```
int arr[5] = { 1,2,3,4,5 };
	cout << "逆置前的顺序为：" << endl;
	for (int i = 0; i < 5; i++)
	{
		cout << arr[i] << endl;
	}
	int start = 0;//起始下标
	int end = sizeof(arr) / sizeof(arr[0]) - 1;//结束下标
	while (start < end)
	{
		int temp = arr[start];
		arr[start] = arr[end];
		arr[end] = temp;//实现元素互换
		start++;//下标更新
		end--;//下标更新
	}
	cout << "逆置后的顺序为：  "  << endl;
	for (int i = 0; i < 5; i++)
	{
		cout << arr[i] << endl;
	}
```

### 冒泡排序

排序的总轮数：元素个数减一

元素对比次数：元素个数-排序轮数-1

```
int arr[9] = { 33,45,87,96,54,82,47,14,1 };
	cout << "排序前的顺序为：" << endl;
	for (int i = 0; i < 9; i++)
	{
		cout << arr[i] << endl;
	}
	for (int i = 0; i < 9 - 1; i++)
	{
		for (int j = 0; j < 9 - i - 1; j++)
		{
			if (arr[j] > arr[j + 1])
			{
				int temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
			}
		}
	}
	cout << "冒泡排序后的顺序为： " << endl;
		for (int i = 0; i < 9; i++)
		{
			cout << arr[i] << endl;
		}
```

### **二维数组：**

4种定义方式：

1.数据类型 数组名【行数】【列数】；

2.数据类型 数组名【行数】【列数】={{数据1，数据2}，{数据3，数据4}};

3.数据类型 数组名【行数】【列数】={数据1，数据2，数据3，数据4}；

4.数据类型 数组名【 】【列数】={数据1，数据2，数据3，数据4}；

![image-20221021093724299](C:\Users\lee\AppData\Roaming\Typora\typora-user-images\image-20221021093724299.png)

![image-20221021094043738](C:\Users\lee\AppData\Roaming\Typora\typora-user-images\image-20221021094043738.png)

**二维数组成绩统计的案例：**

```
int scores[3][3] = {
		{78,65,95},
		{99,34,81},
		{55,68,100}
	};
	string names[3] = { "张三","李四","王五" };
	for(int i=0;i<3;i++)
	{
		int sum = 0;
		for (int j = 0; j < 3; j++)
		{
			sum += scores[i][j];
		}
		cout << names[i] << "的总分为： " << sum << endl;
	}
```

其结果就是把每个人对应的总分给计算出来了。

### **函数的定义:**

函数返回值类型  函数名（参数列表）

注意：函数的声明可以有多次，但是函数的定义只有一次。

**函数的分文件编写：**

分别创建一个头文件和一个`cpp`源文件，头文件中可以包含函数的声明，而源文件中要包含函数的定义，要注意的是在源文件头还要包含一个#include "头文件名"

### **指针的定义及使用**

定义指针：数据类型 * 指针变量名；

`og：int * p;`

指针的使用：间接访问内存。

*p=1000；指的是指针p所指向的数据；

	int a = 10;
	int* p;
	p = &a;
	cout << p << endl;
	cout << &a << endl;
	*p = 1000;
	cout << a << endl;
	cout << *p << endl;

### 指针的所占内存大小

```
int a = 10;
	int* p;
	p = &a;
	cout << sizeof(p) << endl;
```

32位操作系统都是占4个字节，64位操作系统占的是8位字节。

### **空指针和野指针**

空指针用于给指针变量初始化；

空指针是不可访问的；

野指针：指针变量指向非法的内存空间；

`const修饰指针`：

1.常量指针：`const int *p=&a;`

特点：指针的指向可以修改，但是指针指向的值不可以修改。

如：*p=20：错误，指针指向的值不可以修改；

​          p=&b：正确，指针的指向可以修改。

2.指针常量：`int *const p=&a；`

特点：指针的指向不可以修改，指针指向的值可以修改。

如：*p=20：正确，指向的值可以修改；

​         p=&b：错误，指针的指向不可以修改。

### 指针与数组

利用指针来访问数组中的每一个元素；

```
int arr[10] = { 0,1,2,3,4,5,6,7,8,9 };
    cout << "数组的第一个元素为:" << arr[0] << endl;
    int* p = arr;
    cout << "数组的第一个元素为： " << *p << endl;
    p++;//让指针向后偏移四个字节
    cout << "数组的第二个元素为： " << *p << endl;
    int* p2 = arr;
    for (int i = 0; i < 10; i++)
    {
        cout << *p2 << endl;
        p2++;
    }
```

###         **指针与函数**

1.值传递

注意：值传递不会改变实参

2.地址传递：地址传递会改变实参；

![image-20221022161329044](C:\Users\lee\AppData\Roaming\Typora\typora-user-images\image-20221022161329044.png)

###         **结构体的定义和使用**

语法：自定义的数据类型，一些类型集合组成的一个类型。

```
结构为：`1.struct 结构体名 变量名`

例1：`struct Student{`

`string name;`

`int age;`

`int score;`

`}`这是先在主函数外给结构体的内容先定义结构体，这个是必须的，有了这个才能有下面三个。

例1.1：

`struct Student s1；`

`s1.name="张三"；`

`s1.age=18;`

`s1.score=100;
```

  

```
 `2.struct 结构体名 变量名=（成员1值，成员2值...)`

 `例1.2struct Student s2={"李四",19,80};
```



​    `3.定义结构体时顺便创建变量。`

例1.3

```
struct Student{`

`string name;`

`int age;`

`int score;`

`}s3；`

`s3.name="王五"；`

`s3.age=18；`

`s3.score=98；
```

注意：1.定义结构体的关键字是`struct`，不可省略。（就是例1不可以省略）

​            2.创建结构体变量时，关键字struct可以省略。

​            3.结构体变量利用操作符“.”访问成员。

### **结构体数组**

语法：struct 结构体名 数组名[元素个数]={{}，{}，{}......}

先在函数体外定义结构体数组

```
struct student{

string name;

int age;

int score;

}

**然后再创建结构体数组**

struct Student stuArray[3]=

{

{"张三",18,100}

{"李四"，19,26}

{"王五"，20,75}

};

**如果要修改结构体内的数组的内容**

stuArray[2].name="赵六";

stuArray[2].age=80;

stuArray[2].score=60;
```



### **结构体指针**

```
#include<iostream>`
`#include<string>`
`using namespace std;`
`struct student`
`{`
    `string name;`
    `int age;`
    `int score;`
`};//先定义结构体`
`int main()`
`{`
   `student s = { "张三",18,98 };//student前面的struct可要可不要`
   `student *p = &s;//student前面的struct可要可不要`
    `cout << "姓名 " << p->name << "年龄" << p->age << "得分为： " << p->score << endl;``//可用p指针指向结构体里面的变量值。`


    return 0;

`}
```



### 结构体的嵌套的例子

```
`#include<iostream>`
`#include<string>`
`using namespace std;`
`struct student`
`{`
    `string name;`
    `int age;`
    `int score;`
`};//现在主函数外定义学生的结构体`
`struct teacher`
`{`
    `int id;`
    `string name;`
    `int age;`
    `struct student stu;`
`};//然后再定义老师的函数体，因为老师函数体内包含学生函数体，所以学生函数体要定义在前；`
`int main()`
`{`
    `teacher t;`
    `t.id = 2012002;`
    `t.name = "张哥";`
    `t.age = 51;`
    `t.stu.name = "小王";函数体嵌套，所以要有两个"."`
    `t.stu.age = 16;函数体嵌套，所以要有两个"."`
    `t.stu.score = 87;函数体嵌套，所以要有两个"."`
    `cout << "老师的id为" << t.id << "老师的名字为" << t.name << "老师的年龄为： " << t.age << endl;`
    `cout<<"老师的学生名字为： " << t.stu.name << "学生的年龄为： " << t.stu.age << "学生的成绩为： " << t.stu.score << endl;`
    `return 0;`
`}`
```



### 结构体做函数参数

```
#include<iostream>`
`#include<string>`
`using namespace std;`
`struct student`
`{`
    `string name;`
    `int age;`
    `int score;`
`};`
`void printfstu1(struct student s)`
`{`
    `s.score = 100;`
    `cout << "名字为：" << s.name << "年龄为： " << s.age << "成绩为： " << s.score << endl;`
`}`
`void printfstu2(struct student* p)`
`{`

    cout << "名字为： " << p->name << "年龄为： " << p->age << "成绩为： " << p->score<<endl;

`}`
`int main()`
`{`
    `struct student s;`
    `s.name = "王五";`
    `s.age = 23;`
    `s.score = 87;`
    `printfstu1(s);`
    `printfstu2(&s);`
   `// cout << "在main函数中打印 名字=" << s.name << "年龄为： " << s.age << "成绩为： " << s.score << endl;`
    `return 0;`
`}
```

注意：主要区分了值传递和地址传递

1.值传递只是改变了形参，而没改变形参（主函数里的值）

2.地址传递改变了实参，也改变了形参（主函数里的值）

所以，如果不想改变主函数的值，用值传递，反之就用地址传递。



### **`const`的使用场景**

`const student *p;`

### **结构体的应用例子**



