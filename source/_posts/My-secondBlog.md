---
title: My secondBlog
date: 2019-05-06 11:25:08
tags:
---
## This is my second try

--------------------
判断语句
- [x] 计算时间差
```c
#include <stdio.h>
int main ()
{   int hour1, minute1;
    int hour2, minute2;
    printf("请输入第一个时间，格式5:30:");
    scanf("%d:%d", &hour1, &minute1);

    printf("请输入第二个时间，格式5:30:");
    scanf("%d:%d", &hour2, &minute2);

    int ih = hour2 - hour1;
    int im = minute2 - minute1;
    if (im < 0){
    /*判断minute2是否不够减minute1*/
        im = im + 60;
        ih --;
    }
    printf("时差是%d小时%d分\n", ih, im);
    return 0;
}
```
- [x] 关系运算的结果0或1
```c
#include <stdio.h>
int main ()
{
    printf("%d\n", 5==3);//输出结果为0
    printf("%d\n", 5>3);//输出结果为1
    printf("%d\n", 5<3);//输出结果为0
    printf("%d\n", 7 >= 3 + 4);//输出结果为1
    printf("%d\n", 5 > 3 == 6 > 4);//输出结果为1

    return 0;
}
```

- [x]关系运算符的优先级比算术运算符的优先级低，但是比赋值运算符的优先级高

如  7 >= 3 + 4 是先把3 + 4的结果算出来再与左边的7比较而不是先比较7 >=3

--------------------------
我们可以将计算机这样理解
它是读取一些输入，
在模型里面做一些计算，
再把计算的结果做一些输出。
虽然有时计算的模型有些复杂



--------------------------
- [x] 找零
```flow
st=>start: 开始
e=>end: 停止
op=>operation: 初始化
cond=>condition: bill>=price?
io=>inputoutput: 输入price和bill
ou=>inputoutput: 输出price和bill

st->op->io->cond
cond(yes)->ou->e
cond(no)->e

```
```c
#include <stdio.h>
int main (void)
{
    // 初始化
    int bill = 0;
    int price = 0;
    int change = 0;

    // 读入金额和票面
    printf ("请输入金额（元）：");
    scanf ("%d", &price);
    printf ("请输入票面（元）：");
    scanf ("%d", &bill);

    //计算找零
    if (bill >= price)
    {
        change = bill - price;
        printf ("找你%d元。\n", change);    
    }
    
    
   

    getchar ();
    return 0;
}
```




- [x] 程序变式 判断年龄

```flow
st=>start: 开始
e=>end: 停止
op=>operation: 初始化
cond=>condition: age<MIONR?
io=>inputoutput: 输入“你的年龄是”+age
ou1=>inputoutput: 输出
“年龄决定了你的精神世界，
好好珍惜吧”
ou2=>inputoutput: 输出
“年轻是美好的。” 

 
st->op->io->cond
cond(yes)->ou1->e
cond(no)->ou2->e

```
```c
#include <stdio.h>
int main (void)
{   
    const int MINOR = 35;
    int age = 0;

    printf ("请输入你的年龄：");
    scanf ("%d", &age);
    printf ("你的年龄是%d岁。\n",age);

    if (age < MINOR)
    {
        printf ("年轻是美好的");
    }
    printf ("年龄决定了你的精神世界，好好珍惜吧。\n");
    
    return 0;
}
```

- [x] 找零更新
```flow
st=>start: 开始
e=>end: 停止
op=>operation: 初始化
cond=>condition: bill>=price?
io=>inputoutput: 输入price和bill
ou1=>inputoutput: 输出price和bill
ou2=>inputoutput: 输出钱不够

st->op->io->cond
cond(yes)->ou1->e
cond(no)->ou2->e

```



## The fact is I can't count thwm, so  I just make a number

-----------------
