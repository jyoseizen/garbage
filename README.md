# 進み！
## what's this?
>这里即使我的JavaLearningHistory，也是markdown实践场地
> **Some birds are not close, because they are too bright.**
> 
> **Good Luck to myself**

---

## 目录

### 概述

-[what's this?](#what'sthis?)

### 计划清单(这里试用一下任务列表功能)

- [小计划](#小计划)
- [中计划](#中计划)
- [大计划](#大计划)

### JavaLearning

- [注释](#1注释)
- [关键字](#2关键字)
- [字面量](#3字面量)
- [变量](#4变量)
- [数据类型](#5数据类型)
- [标识符](#6标识符)
- [运算符](#7运算符)
- [控制语句](#8控制语句)
- [数组](#9数组)
- [方法](#10方法)

---

## 计划清单(这里试用一下任务列表功能)

### 小计划
- [x] 活着
- [ ] 死去

### 中计划

### 大计划

---

## JavaLearning

### 1.注释
- 单行注释:Ctrl + /
- 多行注释:Ctrl +Shift+ /

### 2.关键字
Java关键字是编程语言中的预定义的具有特殊含义的词汇,关键字字母全部小写,在编辑器中有特殊颜色标记
- 修饰符关键字:public、protected、private、static、final、abstract
- 访问控制关键字:public、protected、private、default（默认）
- 类、接口和包关键字:class、interface、enum、package、import、extends、implements
- 方法关键字:void、return、this、super
- 流程控制关键字:if、else、switch、case、default、while、do、for、break、continue、return
- 异常处理关键字:try、catch、finally、throw、throws
- 逻辑关键字:true、false、null
- 其他关键字:new、instanceof、synchronized、transient、volatile、assert

**关键字有很多,没有必要去一一记忆**
  
### 3.字面量

- 整数字面量：表示整数值，可以使用十进制、八进制（以0开头）和十六进制（以0x或0X开头）表示法。例如：42, 012, 0xFF 
- 浮点数字面量：表示浮点数值，包括普通的浮点数和科学计数法表示。例如：3.14, 2.0e-5。
- 字符字面量：表示单个字符，使用单引号括起来。例如：'A', '1', '@'
- 字符串字面量：表示一个字符串，使用双引号括起来。例如："Hello,World!","Java"
- 布尔字面量：表示布尔值，只有两个取值：true和false
- null 字面量：表示空引用，用于表示对象引用不指向任何有效的对象。
- 转义序列：一些特殊的字符序列，以反斜线 \ 开头，用于表示无法直接输入的字符，如换行符\n、制表符\t等
- 数组字面量：用花括号 {} 表示，用于初始化数组。例如：{1, 2, 3}
- 枚举常量：枚举类型的常量值，表示枚举中的特定选项
- 字符编码字面量：表示字符的Unicode编码，以\u开头，后面跟着四个十六进制数字。例如：\u0041 表示字符‘A’

一点小技巧：
- 不带小数点的数字都是整数类型的字面量
- 只要带了小数点，那么就是小数类型的字面量
- 只要用双引号引起来的，不管里面的内容是什么，不管里面有没有内容，都是字符串类型的字面量
- 字符类型的字面量必须用单引号引起来，不管内容是什么，但是个数有且只能有一个
- 布尔类型的字面量只有两个值，true、false
- 空类型的字面量只有一个值，null

### 4.变量

- 格式：数据类型 变量名 = 数据值;

变量名不能重复

在一条语句中，可以定义多个变量，但是这种方式影响代码的阅读，所以了解一下即可

变量在使用之前必须要赋值

### 5.数据类型

- 基本数据类型：double > float > long > int > short > byte
  - 整数类型
    - byte：-128~127
    - short：-32768~32767
    - int(默认)：-2147483648~2147483647
    - long：-9223372036854775808~9223372036854775807（如果要定义long型时，需要加一个L作为后缀）
  - 小数类型
    - float：-3.401298e-38~3.402823e+38（如果要定义float型时，需要加一个F作为后缀）
    - double(默认)：-4.9000000e-324~1.797693e+308
  - 字符类型
    - char：0~65535
  - 布尔类型
    - boolean：true，false
- 引用数据类型
  - 类（Class）：类是用来创建对象的模板。它定义了对象的属性（成员变量）和方法（成员方法）。通过实例化类，可以创建类的对象，并使用对象调用类的方法。
  - 接口（Interface）：接口定义了一组方法的规范，但没有实际的方法体。类可以实现一个或多个接口，从而获得接口定义的方法，并在类中实现这些方法。
  - 数组（Array）：数组是一种用于存储相同类型元素的数据结构。它可以是一维数组或多维数组，用于在内存中连续存储多个元素。
  - 枚举（Enum）：枚举是一种特殊的类，用于表示一组预定义的常量。枚举常常用于表示一组相关的值。
  - 字符串（String）：字符串是一种引用数据类型，但它具有特殊的性质，可以像基本数据类型一样进行操作。字符串实际上是一个字符序列，它有许多方法用于处理字符串操作。
  - 自定义引用类型：除了上述内置的引用数据类型，开发人员还可以创建自定义的类和接口，以及它们的实例，从而构建更复杂的数据结构和功能。
 
### 6.标识符

在Java中，标识符是用来标识程序中各种元素的名称，比如变量、方法、类、接口等。标识符是由字母、数字、下划线（_）和美元符号（$）组成的序列，且必须以字母、下划线或美元符号开头。标识符在编程中用于命名各种实体，使得程序易于阅读、理解和维护

- 硬性要求
  - 由数字、字母、下划线_和美元$组成
  - 不能以数字开头
  - 不能是关键字
  - 区分大小写
- 软性建议
  - 小驼峰命名法-变量名和方法名
    - 标识符是一个单词的时候，全部小写
    - 标识符由多个单词组成的时候，第一个单词首字母小写，其他单词首字母大写
  - 大驼峰命名法-类名
    - 标识符是一个单词时，首字母大写
    - 标识符由多个单词组成的时候，每个单词的首字母大写
  - 阿里巴巴命名规范细节
    - 尽量不要使用拼音，但是一些国际通用的拼音可以视为英文单词
    - 平时在给变量名、方法名、类名起名字的时候，不要使用下划线或美元符号。
   
### 7.运算符

- 算数运算符
  - '+'
  - '-'
  - '*'
  - '/'
  - '%'
- 自增自减
  - '++'
  - '--'
  - ++和--既可以放在变量的前边，也可以放在变量的后边，只要单独写一行结果都是一样的
- 赋值运算符
  - '='
  - '+='：左右相加，把结果赋给左边，a += b;等同于a = a + b;
  - '-='
  - '*='
  - '/='
  - '%='
- 关系/比较运算符(结果都是boolen类型)
  -  '=='
  -  '!='
  -  '>'
  -  '>='
  -  '<'
  -  '<='
- 逻辑运算符（全部执行）
  - '&'：与，并且
  - '|'：或，或者
  - '^'：异或，相同为false，不同为true
  - '!'：非，取反
- 短路逻辑运算符（短路）
  - '&&'：并且
  - '||'：或者
- 三元运算符
  - 关系表达式 ？ 表达式1 : 表达式2；
  - 求两个数的较大值—— int max = a > b ? a : b;
  - 必须使用
- 运算符优先级
  - 干()就完了
- 其他运算符
  - '<<'：左移，低位补0——乘2
  - '>>'：右移，高位补0或1（原0补0，原1补1）——除2

- 转换（不同数据类型计算）
  - 隐式转换（自动类型提升）
    - 取值范围小的，和取值范围大的进行运算，小的会先提升为大的，在进行运算
    - byte<short<int<long<float<double
    - byte、short、char三种类型在运算的时候，都会直接先提升为int，然后再进行运算
  - 强制转换
    - 如果把一个取值范围大的数值，赋值给取值范围小的变量，是不允许直接赋值的。如果一定要这么做就需要加入强制转换（会导致数据发生错误）
    - 目标数据类型 变量名 = (目标数据类型) 被强转的数据；

- “字符串”的“+”操作
    - 当“+”操作中出现字符串时，这个“+”是字符串连接符，而不是算术运算符。会将前后的数据进行拼接，并产生一个新的字符串
    - 连续进行“+”操作时，从左到右逐个执行。
- ‘字符’的“+”操作
    - 当“字符+字符”和“字符+数字”时，会把字符通过ASCII码表查询到对应的数字再进行计算
    - a-97，A-65

### 8.控制语句

- 流程控制语句
  - 顺序结构
    - 按照编写顺序依次执行
  - 分支结构
    - if
    - switch
      - switch(表达式){case 值1：语句体1；break；; case 值2：语句体2；break; ... default：语句体n+1；break；}
  - 循环结构       
    - for循环
      - for(初始化语句；条件判断语句；条件控制语句) { 循环体语句；}
    - while循环
      - 初始化语句；while（条件判断语句）{ 循环体语句；条件控制语句；} 循环下面的其他语句
      - 相同点
        - 运行规则相同，初始化语句只执行一次；判断语句为true，循环继续；判断语句为false，循环结束
      - 不同点
        - for循环中，控制循环的变量，因为归属for循环的语法结构中，在for循环结束后，就不能再次访问到了
        - while循环中，在控制循环的变量，对于while循环来说不归属其语法结构中，在while循环结束后，该变量可以继续使用
    - do...while
      - 初始化语句;do{循环体语句;条件控制语句;}while(条件判断语句);
       - 先执行后判断
    - 无限循环
      - for(;;){循环体语句;}
      - while(true){循环体语句;}
      - do{循环体语句;}while(true);
      - 无限循环下面不能再写其他代码，因为循环体永远停不下来，下面的代码永远执行不到
- 条件控制语句
  - continue：跳过本次循环，继续执行下次循环
  - break：结束整个循环

### 9.数组

- 数组指的是一种容器，可以用来存储同种数据类型的多个值
    - 数组容器在存储数据时，需要结合隐式转换考虑
    - 建议容器的类型和存储数据类型保持一致
- 数组的定义
    - int  []  array;
    - int  array[];
- 数组的静态初始化
    - 初始化：就是在内存中，为数组容器开辟空间，并将数据存入容器中的过程
    - 数据类型[] 数组名 = new 数据类型[] {元素1,元素2,元素3...};
    - 数据类型[] 数组名 = {元素1,元素2,元素3...};
- 数组元素的访问
    - 数组名[索引];
    - 索引(下标,角标)从0开始，逐个+1增长，连续不间断
- 数组遍历
    - 将数组中所有的内容取出来，取出来之后可以(打印,求和,判断...)
    - for(int i=0;i < arr.length;i++){System.out.println(arr[i]);}
- 数组动态初始化
    - 数据类型[] 数组名 = new 数据类型[数组长度];
    - 在创建的时候，由我们自己指定数组的长度，由虚拟机给出默认的初始化值
- 静动区别
    - 动态初始化：手动指定数组长度，由系统给出默认初始化值
    - 静态初始化：手动指定数组元素，系统会根据元素个数，计算出数组长度
- 数组长度：arr.length

### 10.方法

- 方法(method)是程序中最小执行单元
  - 把一些代码打包在一起，该过程成为方法定义
  - 方法定义后并不能直接运行，需要手动调用才能执行，该过程称之为方法调用
- 最简单的方法定义和调用
  - 定义格式：public static void 方法名(){ 方法体(就是打包起来的代码)； }
  - 调用格式：方法名()；
  - 注意：方法必须先定义后调用，否则程序将会报错
- 带参数的方法定义和调用
  - 定义格式：public static void 方法名(参数){... ...}
  - 调用格式：方法名(参数1,参数2,...);
  - 注意：方法调用时，参数的数量与类型必须与方法定义中小括号里面的变量一一对应，否则程序将报错
- 带返回值的方法定义和调用
  - 定义格式：public static 返回值类型 方法名 (参数) { 方法体; return 返回值; }
  - 调用
    - 直接调用：方法名(实参)；
    - 赋值调用：整数类型 变量名 = 方法名 (实参)；
    - 输出调用：System.out.println(方法名(实参))；
- 注意事项
  - 方法不调用就不执行
  - 方法与方法之间是平级关系，不能互相嵌套定义
  - 方法的编写顺序和执行顺序无关
  - 方法的返回值类型为void，表示该方法没有返回值，没有返回值的方法可以省略return语句不写。如果要编写return，后面不能跟具体的数据
  - return语句下面，不能编写代码，因为执行不到，属于无效代码
- 方法的重载
  - 同一个类中，方法名相同，参数不同的方法。与返回值无关。
  - 在同一个类中，定义了多个同名的方法，这些同名的方法具有同种的功能
  - 每个方法具有不同种的参数类型或参数个数，这些同名的方法，就构成了重载关系
        
