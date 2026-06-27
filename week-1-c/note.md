
##  Week 1 知识点速览

```text
Scratch 思维
     ↓
源代码(Source Code)
     ↓
编译器(Compiler)
     ↓
机器代码(Machine Code)
     ↓
C语言基础语法
     ↓
变量 + 条件 + 循环 + 函数
     ↓
编写规范（Correctness / Design / Style）
```

---

## 1. 什么是 C？

计算机只能看懂 **0 和 1**。

因此：

```text
你写的 C 代码
        ↓
      Compiler
        ↓
CPU 可以执行的机器码
```

例如：

```c
#include <stdio.h>

int main(void)
{
    printf("Hello, world!\n");
}
```

这是你写的 **源代码（Source Code）**，编译后才会变成机器代码。

---

## 2. 学会使用终端（CLI）

CS50 开始让你离开图形界面，进入命令行：

```bash
pwd
ls
cd
mkdir
cp
mv
rm
```

以及：

```bash
make hello
./hello
```

其中：

* `make` = 编译程序
* `./程序名` = 运行程序

---

## 3. 数据类型（Types）

CS50 介绍了最常见的数据类型：

```c
int      // 整数
float    // 浮点数
char     // 单个字符
bool     // 真/假
string   // 字符串（CS50库提供）
```

例如：

```c
int age = 20;
float pi = 3.14;
char grade = 'A';
```


---

## 4. 条件判断（Conditionals）

相当于 Scratch 的：

> 如果……那么……

例如：

```c
if (x < y)
{
    printf("less\n");
}
else if (x > y)
{
    printf("greater\n");
}
else
{
    printf("equal\n");
}
```

重点：

* `==` 表示比较
* `=` 表示赋值


---

## 5. 循环（Loops）

CS50 介绍三种循环：

### while

```c
while (true)
{
    printf("meow\n");
}
```

---

### for

```c
for (int i = 0; i < 3; i++)
{
    printf("meow\n");
}
```

---

### do while

```c
int n;
do
{
    n = get_int("Number: ");
}
while (n < 1);
```

作用：

> 至少执行一次。 

---

## 6. 函数（Functions）

函数就是：

> 给代码起名字。

例如：

```c
void meow(int n)
{
    for (int i = 0; i < n; i++)
    {
        printf("meow\n");
    }
}
```

然后：

```c
meow(3);
```

输出：

```text
meow
meow
meow
```

这是 CS50 非常强调的思想：

> 不要复制代码，要抽象代码。 

---

## 7. Mario 金字塔（本周最大练习）

这是本周最经典的问题：

```text
   #
  ##
 ###
####
```

这个练习的真正目的不是打印图案，而是训练：

* 获取用户输入
* 输入验证
* 嵌套循环
* 逻辑拆解能力

也就是：

```text
for 行
    for 空格
    for #
```


---

## 8. 运算符（Operators）

```c
+
-
*
/
%
```

以及：

```c
++
--
+=
```

例如：

```c
i++;
```

等价于：

```c
i = i + 1;
```



---

## 9. 两个重要陷阱

### 整数溢出（Integer Overflow）

```c
int x = 2147483647;
x++;
```

结果：

```text
-2147483648
```

因为 int 的大小有限。

---

### 浮点数误差（Floating Point Imprecision）

例如：

```c
0.1 + 0.2
```

实际上可能得到：

```text
0.30000000000004
```

因为计算机内部使用二进制表示小数。

---

## 10. CS50 最重要的新思想

David Malan 在 Week1 反复强调：

程序不仅要：

正确（Correctness）

还要：

设计良好（Design）

以及：

风格优秀（Style）

例如：

错误❌：

```c
printf("meow\n");
printf("meow\n");
printf("meow\n");
```

正确✔：

```c
for (int i = 0; i < 3; i++)
{
    printf("meow\n");
}
```

因为：

> 程序员的工作不是让计算机理解代码，而是让人类理解代码。

---

# 如果浓缩成 5 个关键词：

```text
编译 (Compiler)
      ↓
变量 (Variables)
      ↓
条件 (Conditionals)
      ↓
循环 (Loops)
      ↓
函数 (Functions)
```

