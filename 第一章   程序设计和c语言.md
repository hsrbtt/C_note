# **程序设计和c语言**

## **1.什么是计算机程序**

**程序就是计算机能够识别和执行的指令，每一条指令让计算机执行特定的操作。**

## **2什么是计算机语言**

**机器语言    计算机工作基于2进制，根本上说，计算机能够识别和接受0和1组成的指令，一般的计算机指令长度为16，既以16个二进制数组成的指令，16个1和0可以组成各种排列组合。这种计算机能够直接识别和接受的二进制代码成为机器指令，机器指令的集合就是机器语言。**

**符号语言    用英文字母和数字表示一个指令，例如ADD代表”加“，SUB代表”减“，LD代表从”传送“等。计算机不能直接识别和接受符号语言的指令，需要一种称为汇编程序的软件把符号语言的指令转化为机器指令。转换的过程称为”代真“或”汇编“，因此符号语言又被称为符号汇编语言或汇编语言**

**高级语言    为了克服低级语言的缺点，20世纪50年代创造了第一个计算机高级语言FORTRAN这种语言功能很强，且不依赖于具体机器，写出的语言任何型号计算机都能适用（或只做出很少修改）。**

**计算机也不能直接识别高级语言程序，也要进行翻译，用一种称为编译程序的软件把高级语言写的程序（称为源程序）转化为机器指令的程序（称为目标语言)，然后让计算机执行机器指令程序，得出结果。高级语言的一个语句往往对应多条指令。**

**高级语言发展的不同阶段：**

**1.非结构的语言   初期语言未非结构语言，风格随意，符合语法规则即可，没有严格规范要求，程序中的流程可随意跳转。是程序难以阅读和维护。**

**2.结构化语言   为了解决问题提出”结构化程序设计方法“，规定程序必须由具有良好特性的基本结构（顺序结构，选择结构，循环结构）构成。**

3. **面向对象语言  在处理大规模问题时，采用面向对象的语言。**

## ***任何写出的程序在提交前一定要调试一下***

## **3.最简单的c语言**

   ```c
   #include <stdio.h>
   int main()
       //int 函数类型，，main是主函数
   {
       printf("hello world!\n");
       retunr 0;
   }
   ```

   **![image-20220802213156589](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220802213156589.png)**

- **Printf("Heelo world！\n")	；**


- **“”里面的内容较做“字符串”，printf会把其中的内容原封不动的输出**

-    **\n表示需要在输出的结果后面换一行**


- ​      **“”以外不能用中文输入法，里面可以用中文**



### **注释**

- **以"//"插入在程序中，用来向读者解释信息的，用于单行注释。对程序没有任何影响。**
- ![image-20220809222313851](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220809222313851.png)



**做计算**

- **printf("%d",12+23);**


- **%d说明后面有一个整数要输出在这个位置上**


- **输出结果:35**


- **printf("12+23=%d",12+23);**


- **""里面的12+23=原封不动输出，然后后面的值填在%d的位置**


- **输出结果：12+23+35**

## **4.变量**



```c
#include<stdio.h>
int main()
{
    int price=0;
        printf("请输入金额（元）：");
    scanf("%d",&price);
        int change=100-price;
    printf("找您%d元。\d",change);
    
}
```

**int price=0**

- **这一行，定义了一个变量。变量名字是price，类型是int，初始时0。**


- **变量是一个保存数据的地方，当我们需要在程序里保存数据时，比如上面一个例子中要记录用户输入的价格，就需要一个变量保存它。用一个变量保存了数据，它才能参加到后面的计算，比如计算找零。**


### **变量的一般形式**

- **<类型名称><变量名称>**

- **int price；**


- **int amount；**


- **int price， amount；（定义了2个变量，一行中可以定义多个变量）**


### **变量的名字**

- **变量需要一个名字，变量的名字是一种“标识符”，意思是用它来识别这个和那个的不同的名字。**

- **标识符有标识符的构造规则。基本原则是：标识符只能由字母, 数字和下划线组成，数字不可以出现在第一个位置上，c语言的关键字（有的地方叫保留字）不可以用做标识符。**
- **保留字**

**![image-20220805203737274](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220805203737274.png)**

### **赋值和初始化**

```c
#include<stdio.h>
int main()
{
    int price=0;
        printf("请输入金额（元）：");
    scanf("%d",&price);
        int change=100-price;
    printf("找您%d元。\d",change);
    
}
```

- **int price=0;**
- **price=0这个式子，这里“=”是赋值运算符号，表示“=”右边的值赋给左边的变量。**
- **有“=”的式子叫表达式**

**赋值**

- **和数学不同，a=b在数学中表示关系，即a和b的值一样，而在程序设计中，a=b要求计算机做一个动作：将b的值赋给a。关系是静态的，而动作是动态的。在数学中，a=b和b=a是等价的，而在设计程序中，二者的意思完全相反。**

**初始化**

- **c语言并没有强制要求所有变量都在定义的地方做初始化，但是所有的变量第一次被使用的（出现赋值运算符号的右边）之前应该被赋值一次**

- **变量初始化的基本形式：**

  **<类型名称> <变量名称>=<初始化>；**

  - **int price=0；**
  - **int amount=100；**
  - **组合变量定义的时候，在这个定义中单独给单个变量赋初值，如：**
    **int price=0，amount=100；**

**变量的类型**

- **int price=0；**
- **int 是变量的类型。**
- **c语言是一种有类型的语言，所有的变量在使用之前必须定义或声明，所有的变量必须具有数据类型。数据类型表示在变量中可以存放什么样的数据，变量中只能存放指定类型数据，程序运行过程中也不能改变变量类型。**

### **多个变量**

- **一个程序可以有很多变量**
- **int change=100-price；**
- **定义了第二个变量change**
- **并且做了计算**
- **这种写法是c99的写法，c99允许在程序的任何地方定义变量只要在第一次这个变量出现之前定义了这个变量；**
- **![image-20220805212215772](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220805212215772.png)**

### **读整数**

- **scanf（“%d”，&price）;**

- **要求scanf这个函数读入下一个整数，读到结果赋值给变量price**

- **小心price前面的&**

- **scanf意思是输入，printf是输出**

### **交换变量**

**例如：交换a=5，b=4，这两个值不能直接的a=b，b=a，这表达时关系而程序执行的是动作，要让t=a，a=b，b=t，这样程序才会将a，b的值进行交换。**





## **5.常量**

- **int change=100-price;**
- **固定不变的数，是常数，。直接写在程序里，称为直接量。**
- **更好的方式，是定义一个常量：**
  - **const int AMOUNT=100;  C99的写法**

**![image-20220805213731703](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220805213731703.png)**

- **const**

- **const是一个修饰符，加在int前面，用来给这个变量加上一个不变的属性。这个const的属性表示这个变量的值一旦初始化，就不能修改。**

- **int change=AMOUNT - price;**

- **如果试图对常量做修改，把他放在赋值运算符号的左边，就会被编译器发现，指出为一个错误。**

  

- **用一个scanf读2个或多个变量只需要在字符串内放够多的%d**

  

**![image-20220805220554492](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220805220554492.png)**



## **6.浮点数**

- **因为整数运算的结果只能是整数**
- **10/3*3=?**
- **10和10.0在c中完全不同的数**
- **10.0是浮点数**
- **带小数点的数是浮点数。**

### **浮点数计算**

- **当变量为浮点数时，把变量定义的int类型换成double类型，int是整型的变量，double（有双的意思）来表示浮点数类型，在输入那一栏将%d转换成%lf（除了double还有float）**

**![image-20220805231143549](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220805231143549.png)**

- **当浮点数和整数在一起运算时，c会将整数转换成浮点数，然后进行浮点数的运算。**

## **7.表达式**

- **一个表达式是一系列运算符和算子的组合，用来计算一个值。**

- **运算符是指进行运算的动作，比如运算符“+”...![image-20220807220026641](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220807220026641.png)**

- **算子是指参与运算的值，这个值可能是常量也可能是变量，还可能是一个方法的返回值。**

### **运算符的优先级**

**![image-20220807222834073](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220807222834073.png)**



-   **嵌入式的表达式不易于阅读和理解，容易造成读程序时的误解。**

### 交换变量

- **2个变量需要交换变量时，要设置一个临时变量存放其中一个变量需要交换的值。**

- **int c=a;**

  **a=b;**

  **b=c;**

## **8.复合赋值和递增递减**

### **复合赋值**

- **五个运算符可以和赋值运算符“=”结合起来**
  - **a += 5；**
  - **a =a+5**

- **2个运算符相结合时中间不能有空格。**

### 递增递减运算符

![image-20220807230900973](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220807230900973.png)

![image-20220807231754265](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220807231754265.png)

- **++ ，--，可以单独使用最好不要组合进行表达**



## 9.做判断

### **if语句**

- **if(条件){..........}**

- **只有条件成立时，程序才会运算{.....}里的东西，否者直接跳过。**

- **if(条件)后面可以没有{ }，但是(条件)后不能加“；”也只能接受一条语句。**

  

### 关系运算

- **关系（比较）运算符**
- ![image-20220809213704284](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220809213704284.png)

- **关系运算的结果**
  - **当两个值的关系符合关系运算符的预期时，关系运算结果为整数1，否则为整数0。**
- **优先级**
  - **所有的关系运算符的优先级比算数的低，但是比赋值运算的高。**
  - **判断是否相等==和!=的优先级比其他的低，而连续的关系运算是从左往右进行的。**



### 否则的话

**else**

- **在if(条件){.........}后面加else{........}**

### 嵌套的if—else

```c
if(....){
    if(...)........；
    else ......；
}
else{...........}
```





- **当if的条件满足或不满足的时候要执行的语句也可以是一条if或if-else语句，这就是嵌套的if语句。**

- **else的匹配总是和最近的那个if匹配,当if语句被{}限制的时候{}外的else与被限制的if语句前的if匹配。**

### 级联的if-else

![image-20220811221652298](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220811221652298.png)

### 多支分路switch

```c
switch(控制表达式){
    case 常量:语句········;
        case 常量：语句·······;break;
            default：语句······;
}
```

- **控制表达式只能是整数型的结果**
- **常量可以说常数，也可以是常数计算的表达式**
- **break是终止语句的执行，因为switch一种基于计算的跳转，计算控制表达式的值后，程序会自动调转到相对应的case处，执行分支内的语句然后在转到下一个case中，直到遇到break才会终止或者switch结束，case相当于内部位置的路标并不能阻止程序的运行。**
- **default，当每一个case都不匹配执行default语句**

## 10.循环

### while循环 

```c
while(条件){循环语句·············}
```

**先满足条件后再做while内的循环语句，做一轮循环后还要再判断一次条件看是否满足，满足继续做循环，不满足结束**

![image-20220816215810217](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220816215810217.png)

### do while 循环

```c
do
{
   循环语句·········
} while(条件);
```

- **先进行一轮语句循环在看是否满足条件，满足继续下一轮循环，不满足则结束循环**
- **注意while（）后的  ；**



### for循环

- ![image-20220826212426972](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220826212426972.png)

- **for循环像一个计数循环：先设定一个计数器，初始化它，然后计数器达到某值之前，重复执行循环体，而每执行一轮循环，计数器值以一定步进进行调整，例如+1或-1**

- ```c
  for(i=0;i<=5;i=i++){
      printf("%d",i);
  }
  ```

- **上面的例子就是对于一开始的i=0，当i<=5时，重复做循环体，每一轮做完循环体语句后，使得i++**

- ![image-20230407000315904](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20230407000315904.png)

- **for语句中3个表达式每一个都可以省略但不能省略分隔它们的“；”**

- ![image-20220826212525757](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220826212525757.png)

- **c++里可以在for循环中定义变量**

  - ![image-20220826211615262](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220826211615262.png) 

- **for和while循环是等价的可以互换**

  - ![image-20221224174841903](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224174841903.png)


### 循环的选择

![image-20220826213053790](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220826213053790.png)

### 跳出循环和跳过循环

![image-20220827145926062](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220827145926062.png)

- **break只能跳出它所在的单个循环**

### 嵌套的循环

- **循环的嵌套可以是同一种循环的嵌套也可以是不同种循环的嵌套，看具体使用情况**
- **除非特殊情况尽量使每一层使用的变量不同**
- **嵌套循环的执行，最内层的循环执行到不满足循环条件，再跳到他的上一层继续向下执行循环，以此类推**

### 跳出多重循环

1. **接力break**：![image-20220827160040317](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220827160040317.png)

   **先定义一个变量在break前再初始化它，每跳出一次循环就进行一次判断**

2. **goto语句**![image-20220827160650044](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20220827160650044.png)

**goto后面要有一个标号，要跳转的标号的位置自己设定，意思是goto要跳到所指的标号位置去。注意跳转到的位置的标号结尾要用 ：**

**建议只在多重循环内用**

## 11.数据类型

### c语言的类型

- ![image-20221224195019223](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224195019223.png)
- **类型的不同**
  - ![image-20221224195917741](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224195917741.png)

### **sizeof**

- **是一个运算符，给出某个字节或变量在内存中占据的字节数**

- **sizeof(int)意思是int在内存中占据的字节数**

- **sizeof(i)意思i这个变量再内存中占据的字节数**

- **是静态运算符，他的结果再编译时就决定的**

- **不要在sizeof的括号内做运算，这些运算不会做的**

### 整数的大小

![image-20221224203448516](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224203448516.png)

- **字长是计算机里寄存器是多少宽的，也就是说这个寄存器是多少bit**
- **int就是表达的就是寄存器的大小**

### 整数的内部表达

- **计算机内部一切都是二进制**
- **18------00010010**
- **0-------00000000**
- **1个字节（8位）可以表达的数：00000000---11111111（0---255）**

### 二进制负数

- **原码：最高位为符号符，0为正数，1为负数**

  - **5------>0000 0101**

  ​       **-5------>1000 0101**

- **反码：正数的反码与原码一致，负数的反码对原码取反，最高位不变**

  - **5------>0000 0101**
  - **-5------>1111 1010**

- **补码：正数的补码与原码一致，负数补码先取反再加1**
  - **-5------>1111 1011**


![image-20221224205616756](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224205616756.png)

### 数的范围

![image-20221224205757053](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224205757053.png)

### 整数的范围

![image-20221224210257303](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224210257303.png)

### unsigned

![image-20221224210908739](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224210908739.png)

- **unsigned是整数不以补码的形式表示负数，这个整数没有负数部分只有0和正整数部分，用unsigned时表达的正数范围扩大，但不能表达负数了**

### 整数越界

![image-20221224211800374](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224211800374.png)

### 整数的输入输出

![image-20221224212526934](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224212526934.png)

### 8进制和16进制

![image-20221224213156857](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224213156857.png)

![image-20221224213301274](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224213301274.png)

### 选择整数类型

![image-20221224213713470](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224213713470.png)

- **没有特殊需要就选int**

## 12.浮点类型

![image-20221224214120895](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224214120895.png)

### 浮点数输入输出

![image-20221224214637913](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224214637913.png)

- **“%e” 输出的是科学计数法的数**

- ​	**科学计数法**

​	![image-20221224214854598](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224214854598.png)

- **输出精度**

![image-20221224215124559](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224215124559.png)

### 浮点数的范围与精度

![image-20221224215704435](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224215704435.png)

- **浮点数运算精度**
  - **浮点数运算是不精确的，因为它的有效数字是有限的**
  
  - **带小数点的字面量是double而非float**
  - **float需要用f或F后缀来表明身份**

### 浮点数内部表达

![image-20221224220730643](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221224220730643.png)

### 选择浮点类型

- **没有特殊需要只用double**

## 字符类型

![image-20221225140307574](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225140307574.png)

### 字符‘1’的输入输出

![image-20221225141116076](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225141116076.png)

- **当输入的是49，把49赋给c时，输出的字符c就是‘1’，输出的数字c是49；**

- **‘1’的ASCII编码是49，所以当c==49时，他代表的就是字符‘1’**

- **c在赋值时可以赋给它49，也可以scanf里用%c输入1**

### 字符计算

![image-20221225142306079](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225142306079.png)

### 字符大小写转换

![image-20221225142425540](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225142425540.png)

### 混合输入

```c
int i;
char c;
scanf("%d %c",&i,&c);
```

- **%d后的空格表示在读取完整数i后还会再读取一个空格，然后再读取下一个变量；而不加空格则表示整数读取到整数结束为止，把剩下的交给下一个读取**

- **建议没读取一个变量加一个空格**

### 逃逸字符

![image-20221225145714793](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225145714793.png)

**以反斜杠“\”开头，后面跟上另一个字符，这两个字符合起来组成一个字符，用来表达无法印出的控制字符或特殊字眼。**

![image-20221225145639659](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225145639659.png)

**\t相当于让输出的不同结果上下对齐**

## 类型转换

### 自动类型转换

![image-20221225151454062](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225151454062.png)

- **对于printf来说，任何小于int的类型会被转换成int；float会被转换成double**
- **但是scanf不会，要输入哪个类型，要用对应的%多少**

### 强制类型转换

![image-20221225152203041](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225152203041.png)

- **注意小的变量不一定能表达大的量**

- **强制类型转换只是从那个变量计算出一个新的类型的值，并不改变那个变量，无论是值还是类型都不改变**

- **强制转换的优先级是比四则运算高的**

## 逻辑类型

### bool

- **#include<stdbool.h>**
- **之后就可以使用bool和true、false**

### 逻辑运算

![image-20221225161410787](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225161410787.png)

- **优先级**

![](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20230206112711157.png)

**！单目运算符最高，&&和||优先级比关系运算符还低比赋值高**

![image-20221225162751722](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225162751722.png)

- **逻辑运算是自左向右进行的，如果左边的结果已经能够决定结果了，就不会做右边计算**

![image-20221225163641054](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225163641054.png)

- **不要把赋值，包括符合赋值组合进表达式**

## 条件运算符

![image-20221225163935003](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225163935003.png)

- **？前面是条件？后面是条件满足时的值：后面是不满足时的值**

- **相当于**![image-20221225164154576](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225164154576.png)

- **条件运算符的优先级高于赋值运算符，但比其他所有运算符都低**

- **不要使用嵌套条件表达式**

## 逗号运算符

- **逗号用来连接两个表达式，并以其右边的表达式的值作为它的结果。逗号的优先级是所有运算符中最低的，所以会有先计算它两边的表达式，逗号的组合关系是自左向右的，所以左边会先算，而右边表达式的值就留下来作为逗号运算的结果**

- **一般用于for循环中连接两个表达式**

![image-20221225165606852](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225165606852.png)

## 函数

### 函数定义

~~~void sum(int begin,int end){
void sum(int begin,int end){
	int i;
	int sum=0;
	for(i=begin;i<=end;i++){
		sum+=i;
	}
	printf("%d到%d的和是%d\n",begin,end,sum);
}
~~~

- **void sum(int begin,int end)这是函数头**

- **void是返还类型，sum是函数名**

- **int begin,int end是参数表，每一个参数都要写成一个类型一个名字的组合**

- **函数头后面的{ }里面的是函数体**

### 函数调用

- **函数名（参数值）；**
- **（）起到表示函数调用的重要作用**
- **即使没有参数也需要（）**
- **如果有参数，则需要给出正确的数量和顺序**
- **这些只会被按照顺序依次用来初始化函数中的参数**
- **调用函数的参数可以是字面量、变量、函数返回值、计算结果**

### **函数的返回**

**函数会返回到调用它的地方的下面的地方**

### 从函数中返回的值

- **如果函数需要返回一个结果要用return把结果返回给调用它的地方**

- **return 表达式**
- **返回的值可以赋给变量，也可以在传递给函数作为调用时的参数，也可以丢掉（不把返回的值丢给任何地方）**
- **有返回值必须用return**

### 没有返回的值

- **函数名前面的类型要用void**
- **不能使用代指的return**
- **可以不用return**
- **调用的时候不能做返回值的赋值**

### 函数的原形声明

- **要把函数名（）写在开头是因为c的编辑器是自上而下的顺序分析你的代码，在它看到你调用函数的时候他需要知道你调用函数的样子，函数的样子就是函数名（），它要知道有几个参数，参数的类型，返回什么类型，然后它在检查你对函数的调用是否正确**

- **把函数放在调用的下面就要在调用前面加一个函数声明，就是在调用前面在加上一个函数头+“；”**

- ![image-20221225204005765](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225204005765.png)

### 参数的传递

![image-20221225204953363](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225204953363.png)

- **c语言在调用时，永远只能传值给函数，当把变量的值传递给函数后，函数内参数无论怎么交换，都不会影响函数外面变量的值。**

- **c无法用函数完成变量的交换**
- **每个函数有自己的变量空间，参数也位于这个独立的空间中，和其他函数没有关系**

### 本地变量

![image-20221225210532431](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225210532431.png)

**变量的生存期和作用域**

![image-20230206113852182](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20230206113852182.png)

**本地变量的规则**

![image-20221225212521058](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221225212521058.png)

### 函数庶事

- **没有参数时**

  - **函数名（void）**

  - **函数名（）表示参数不确定，不代表没有参数**

- **调用函数时圆括号里的逗号是标点符号，不是运算符**
- **f（（a,b））只有再加一个园括号才表示运算符**

- **c语言不允许函数的嵌套定义**

- **关于main**
  - **main也是一个函数**
  - **也可以写成int main(void)**

- **return 0是可以看的，可以起作用的**

## 数组

![image-20221226215613679](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221226215613679.png)

### 定义数组

- **类型+名称[元素数量]；**
- **int number[100];**
- **元素数量必须是整数**
- **c99之前：元素数量必须是编译时刻确定的字面量**

![image-20221226220740942](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221226220740942.png)

![image-20221226220912329](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221226220912329.png)

- **下标可以是数字也可以是常量**

### 有效的下标范围

![image-20221226221507925](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221226221507925.png)

### 集成初始化

- **数组不能先定义在初始化**

  - **int a[19];**

    **a={1,2,3,4,5,6};**

    **这是错误的！**

- **int a[]={1，2，3，4，5}；**
  - **直接用大括号{}给出数组的所有元素的初始值**
  - **不需要给出数组大小，编译器会替你数**
- **int a[5]={a[1]=1,2,a[4]=4};  只有c99可以做定位初始化**
  - **对数组中的某一位进行赋值，2是给a[1]的后面一位，也就是a[2]，其他位置没有得到赋值的就是0**

- **int a[5]={2};**
  - **a[0]的值是2，其他全为0这就是补0**

### 数组的大小

![image-20221227141521362](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227141521362.png)

### 数组的赋值

![image-20221227142243225](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227142243225.png)

### 遍历数组

![image-20221227142422161](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227142422161.png)

### 数组作为函数的参数

![image-20221227143242649](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227143242649.png)

- **必须再用另一个参数来传入数组的大小**
- **不能在[]中给出数组的大小**
- **不能利用sizeof来计算数组的元素个数！**

###  二维数组

![image-20221227150616085](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227150616085.png)

### 二维数组遍历

![image-20221227150904788](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227150904788.png)

- **a[i，j]逗号的意思是是做逗号运算符**

### 二维数组的初始化

![image-20221227151121809](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227151121809.png)

## 运算符&

- **scanf("%d",&i);里的&**

- **获取变量的地址，他的操作必须是变量**

- **int i; printf("%x"，&i)；**
- **地址的大小是否与int相同取决于编译器**
- **int i;printf("%p",&i);**
- **&不能对没有地址的东西取地址**

## 指针

- **就是保存地址的变量**
- **int i**
- **int*  p=&i; 表示p是一个指针用于存放地址，指向int，把i的地址交给p**
- **int*  p,q;**
- **int  *p,q;**
- **可以靠近int也可以靠近p，意思一样的，q表示int类型变量**

### 指针变量

- **变量的值是内存的地址**

  - ​	**普通变量的值是实际的值**

  - **指针变量的值是具有实际值的变量的地址**

### 指针作为参数

**void f(int *p);**

**在被调用时侯得到某个变量的地址：**

**int i=0; f(&i);**

**在函数里可以通过指针访问外面的这个i**

**函数通过指针访问到外面变量的地址值，这个地址值传入到函数，仍然称为值的传递，但因为传的是地址，所以在函数内可以通过*指针对外面地址值进行修改**

### 访问那个地址的变量

***是一种单目运算符，用来访问指针的值所表示的地址上的变量**

**可以做右值也可以做左值**

**int i=*p;**

***p=k+1;**



## *p和**p的区别

**int *p ：一级指针，表示p所指向的地址里面存放的是一个int类型的值**

__int **p ：二级指针，表示p所指向的地址里面存放的是一个指向int类型的指针（即p指向的地址里面存放的是一个指向int的一级指针）__

**例：**

```c
int a=5;     //定义整形变量
int *p=&a;   //定义一个指针指向这个变量
int **p1=&p; //定义一个二级指针指向p指针
/*   那么取出5的方式都有哪些呢？ */
printf("a=%d",a);
printf("a=%d",*p);
printf("a=%d",**p1);
```

## *&p和&\*p

**`根据运算优先级，*&p 等价于*(&p)。&*p 等价于&(*p)。`**

**`1、如果p是int *指针变量，那么*&p = p，&*p = p，都是p，但还没定义p指向哪，存的是谁的地址。`**

**`2、如果p是一个int变量，那么*&p = p；而&*p是非法的，因为*p非法。`**

**`比如int p =10；那么*&p = *(&p) = p = 10（即从p的地址取值），而&*p = &(*p) 则非法，因为p=10，*10是取内存地址为10的值，这在c语言中是不合法的。`**

### **指针的使用场景**

- **指针可以在函数内对外面的变量进行值的交换**

- **函数返回多个值，某些值只能通过指针返回**
  - **传入的参数实际上是需要保存带回的结果的变量**

- **函数返回运算的状态，结果通过指针返回**
  - **常用的套路是让函数返回特殊的不属于有效范围内的值来表示出错** 
  - **但当任何数值都是有效的可能结果时，就得分开返回**

- **传入数组对数组做操作**

### 指针常见错误

**定义了一个指针变量，没有让它指向任何变量，就开始使用指针**



### 数组与指针

**函数参数表中的数组实际上是指针**

![image-20221227221600498](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227221600498.png)

- **只有在函数参数表中他们是等价的**

- **数组变量是特殊的指针**

- **数组本身表达地址，所以对数组不需要用&取地址**
  - **int a[5];**
  - **int*p=a;**

- **但是对数组里每一个单元表达的是变量，对单个的单元需要&取地址**
  - **int a[5];**
  - **int *p=a; == int *p=&a[0];//对a取地址就等于对a[0]的地址**

- **[]运算符可以对数组做，也可以对指针做**
  - **int a=2；**
  
  - **int *p=&a;**
  - **p[0]==*p;//p[0]是指把p所指的地方当作一个int a[1]的数组**
  
- ***运算符可以对指针做，也可以对数组做**
  - ​	**int a[]={1，2，3，4，}；**
  
  - ***a==1；//就是取数组a的第一位的地址**
  
- **数组变量就是const的指针（常量指针），所以初始化以后不能赋值**
  - **int a[]==int*const a**

### 数组指针与指针数组

- **数组指针  int(*p)[n];**

  - **定义了指向有n个元素的一维数组的指针**

  - **当进行p+1，是指p跨过了有n个整形数据的长度**

  - **当指向一维数组**

    - ```c
      int main(void)
      {
          char a[5]={'A','K','C','G','L'};    
          char (*p)[5]=&a;//&a代表的是整个数组的首地址
          //char (*p)[5]=a;这样是错误的，因为a代表第一个元素的首地址
          printf("%c %c %c",**p,*(*p+1),*(*p+3));//输出：A K G
          return 0;
      }
      ```
  
      **ps**：**`&a是指整数组的首地址，a是数组的第一个元素的地址，虽然值相同但意义不一样。&a+1代表向后挪5个字节的地址，a+1是指向下一个元素的地址。而在这里p指向整个数组的地址，*p也就是取整个数组的首地址（与数组的第一个元素地址相同），**p也就是取出第一个元素的值。`**
  
  - **数组指针指向二维数组**
  
    - ```c
      int a[3][4]={{0,1,2,3},{4,5,6,7},{8,9,10,11}};
      int (*p)[4];//定义了指向有4个元素的一维数组的指针
      p=a;//将二维元素的第一行地址赋给了p
      p++;//跨过a[0]行指向下一行a[1]行
      *(*(p+1)+2);//取a[1][2]地址的值也就是6
      ```

​	**`ps :在二维数组中数组名代表的第一行的地址不需要用&，二维数组名就代表第一行的地址，指针来引用二维数组：一种为 * （ * （a+n)+m) 表示第n行第m列元素；另一种为 *（a[n]+m)。这里要注意，利用使用二维数组地址时，*(a+i)与a[i]与a+1是等价的`**

- **指针数组  int* p[n]；**

  - **是一个由n个指针类型元素组成的指针数组，或者说这个当一个数组里含有的元素为指针类型的时候，它就被成为指针数组**

  - **当p+1时，则p指向下一个数组元素**

  - **`ps：p=a；这种赋值方法是错的，因为p是一个不可知变量，只存在p[0],p[1],p[2]，但可以这样 *p=a; 这里*p表示指针数组第一个元素的值，a的首地址的值`**

  - **指针数组指向二维数组**

    - ```c
      int *p[3];     //定义指针数组
      int a[3][4];
      for(i=0;i<3;i++)
      p[i]=a[i];   //通过循环将a数组每行的首地址分别赋值给p里的元素  
      * (* (p+i)+j)、(* (p+i) )[j]、p[i][j]、 * (p[i]+j) //表示数组中第i行第j列的值
      ```

### 指针是const

![image-20221227230702313](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227230702313.png)

![image-20221227230801267](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227230801267.png)

- **const在*前面表示指针所指的东西不能被修改**
- **const在*后面表示指针不能修改**

- **转换**![image-20221227231321336](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227231321336.png)

- **const数组**![image-20221227231516227](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221227231516227.png)

- **保护数组值**![image-20230206124421755](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20230206124421755.png)

### 指针运算

- **当用指针+1时，不是在指针所指的地址值上加一，而是加一个sizeof( )括号里是指针所指的类型，**
  - **也可理解为指针指向了他所指的单元的下一个单元**
  - **如果指针指向的不是一片连续分配空间，如数组，则这种运算没有意义**


- **可以对指针做的运算**
  - **加一个整数，或减一个整数，减一个整数就是往前挪多少个单元**
  - **递增递减（++/--），就是递增或递减到下一个位置**
  - **两个相同类型指针可以相减，两个相同类型的指针相减就是，所指的两个地址之间能放多少个这个类型的变量**

- ***p++**
  - **取出p所指的地址的数据来，然后顺便把p指向下一个单元去**
  - ***的优先级虽然高，但没有++高**
  - **常用于数组连续空间的操作，如遍历**

- **指针可以做比较**
  - **<, <= , == , > , >= , != 都可以对指针做**
  - **比较指针指向的地址内存的大小**
  - **数组的单元的地址肯定是线性递增的**

- **0地址**
  - **0地址是一个不能随便碰的地址**
- **0地址可以做一些特殊的事**
  - **返回的指针是无效的**
  - **指针没有被真正的初始化（先初始化为0），对赋了0的指针做任何事情都会崩溃**
  - **想用0地址可以用NULL符号表示0地址，有的编译器不愿意你用0来表示0地址**

### **指针的类型**

- **指针有很多类型，但所有的指针的大小都是一样的，因为都是地址**

- **但是不同的指针不能直接相互赋值，这是为了避免用错指针**

### 指针的类型转换

![image-20221228162359778](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228162359778.png)

### 动态内存分配

**告诉输入数据的个数，在进行输入，要记录每个数据**

- **c99可以用变量做数组数组定义的大小，c99以前用**
  - **`int *a;`**
  - **`a=(int*)malloc(n*sizof(int));`**

**malloc**

- **向系统申请空间**

- **头部文件用#include<stdlib.h>**

- **void*malloc(size_t size); 是malloc的原形**

- **向malloc申请的的空间大小是以字节为单位的**

- **返回的结果是void*，需要什么类型转换为自己需要的类型**

- **`(int*)malloc(n*sizeof(int))`    n是需要的类型的个数，需要n个int类型大小的内存空间，返回的类型转换为int**

- **如果申请的空间太大没空间了，申请失败则会返回0，或则叫NULL**

**free（）**

- **把申请的空间还给系统**
- **申请过的空间，都要还**
- **只能还申请来的空间的首地址**
- **常见问题：**
  - **申请了没有free会导致内存逐渐下降**
  - **free过了再free**
  - **地址变了，直接free**
- **当申请的动态内存不够用时，可以用**
  - **`void*realloc(void*ptr，size_t size)`;**

### 函数指针

- **就是存放函数地址的指针，指向函数的指针**

  - **原形为typdef int (*fun_prt)(int,int)**	

    - ```c
      int add(int x,int y){
          return x+y;
      }
      int main(){
      int (*p)(int,int);
          p=add;
          int a=10;
          int b=20;
          int sum=0;
          sum=p(a,b);
      }
      ```

    - 

## 字符串

 **char a['H','E','C','B','\0'];**![image-20221228223026495](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228223026495.png)

![image-20221228225536297](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228225536297.png)

### **字符串变量**

- ​	**表现形式：**
  - **char *a="Hello";    有一个指针a指向一个字符数组，里面放的是Hello**
  - **char a[]="Hello";   有一个字符数组a ，里面的内容是Hello**
  - **char a[10]="Hello";  有一个数组a，a的大小10个字符，Hello占据6个字符，因为结尾有个0**
    - **字符串的赋值不能先定义在赋值，必须在同一行！**
  
- **字符串常量**
  - **"Hello"就是一个字符常量，**
  
  - **“Hello”会被编译器放在字符数组的某处，这个数组长度为6，结尾有0**
    - **字符数组的长度是看见的字符的长度加一**
  
  - **相邻的字符会自动连接起来**
  - ![image-20221228231155723](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228231155723.png)

**字符串表现形式的选择**

![image-20221228231346857](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228231346857.png)

**char*不一定是字符串**

![image-20221228231608423](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228231608423.png)

### 字符串的输入输出

- **字符串的赋值**
  - ![image-20221228232055467](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228232055467.png)
- **输入输出**
  - **char a[8];**
  - **scanf("%s",a);**
  - **printf("%s",a);**
  - **scanf读的是一个单词 （单词不一定是真的单词），到空格、tab、或回车为止**
  - **这个scanf是不安全的，不知道读入的内容是多大，可能超过字符数组的大小**
  - **为了安全可以在%和s之间加一个数字，告诉这个scanf最多可以读到多少个字符，多的字符丢到不读**
  - **char s[10];**
    - **ges(s);  从键盘输入一个字符串以回车为结束**
    - **fges(s,10,stdin); 从键盘输入一个字符串以回车为结束,fgets可以防止你输入字符的溢出，它的原型是，`fgets(char *str,int,stdin)`**
- **注意：scanf在输入一个字符串是以回车或空格为结束，如果在scanf后面有gets( )它会吃掉回车或空格，导致程序出问题**
- **常见错误**

![image-20221228233558388](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228233558388.png)

![image-20221228233934970](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221228233934970.png)

### 字符串数组

- **char a[ ] [10];**
  - **意思是有个二维字符数组每一行都有10个字符；**

- **char*a[ ];**
  - **意思是a这个数组里每一个单元都相当于一个指针，每一个都指向外面某处不同的字符数组**

**程序参数**![image-20221229000512282](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229000512282.png)

### 单字符的输入输出

- **putchar**
  - **int outchar(int c);**
  - **向标准输出写一个字符,需要一个参数**
  - **参数int所能接受的也就1个字符，也就是给他一个char放到int里**
  - **返回类型也是int,返回写了几个字符，返回EOF(-1)表示失败**

- **getchar**
  - **int getchar(void);**
  - **向标准输出写入一个字符，不需要参数**
  - **返回类型是int是为返回EOF(-1)表示输入结束了**
  - **Windows上输入ctrl+z让程序强制结束输入程序**
  - **Unix上输入ctrl+d让程序强制结束输入程序**

### 字符串函数

- **用字符串处理函数要用头文件#include<string.h>**

- **strlen**
  - **size_t strlen(const char*s);**
    - **返回s的字符串长度（不包括结尾的0）**
    - **数字符串长度只数到第一个\0**
  
- **strcmp**
  - **int strcmp(const char*s1,const char *s2);**
    - **比较2个字符串**
    - **返回0是s1==s2**
    - **返回1是s1>s2**
    - **返回-1是s1<s2**

- **strcpy**
  - **`char*strcpy(char*restrict dst,const char*restrict src)`;**
    - **把src的字符串拷贝到dst**
    - **restrict表明src和dst不重叠（c99）**
    - **返回dst为了能链起代码来**
    - **拷贝时会将结尾的\0一同拷贝**
  
- **strcat**
  - **`char*strcat(char*s1, const char*s2);`**
    - **在s1字符串后面接上一段字符串s2**

 **字符串中找字符**

- **`char*strchr(const char*s,char c);`**
  - **在字符串s里从左边寻找字符c第一次出现的位置，返回的是指针**

- **`char*strrchr(const char*s,char c);`**
  - **在字符串s里从右边寻找字符c第一次出现的位置，返回的是指针**

- **返回NULL表示没找到，返回指针则指向第一次出现的位置**

**找第二个位置**

~~~c
char a[]="hello"
char *p=strrchr(a,'l');//p所指的是第一个l的位置
p=strrchr(p+1,'l');//p所指的是第二个l的位置


~~~

**字符串里找字符串**

- **`char*strstr(const char*s1,const char *s2);`**
  - **在s1字符串里找s2字符串的位子**

- **`char*strstr(const char*s1,const char *s2);`**
  - **在字符串里找s2字符串位置时忽略大小写**

## 结构

### 枚举

![image-20221229161912905](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229161912905.png)

- **c语言使用自己枚举的数据类型时要加上enum，枚举的符号可以当作int类型的变量进行输入输出**

- **可以在枚举的最后一个常量符号后加一个Num+类型名称，Num+类型名称表示的是枚举了多少个常量符号**
  - **这样需要遍历所有的枚举量或者需要建立一个用枚举量做下标的数组的时候很方便**

- **枚举量**![image-20221229182101650](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229182101650.png)



![image-20221229182336300](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229182336300.png)

### 结构类型

![image-20221229184535867](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229184535867.png)

**一个结构就是一个复合的数据类型，在里面可有很多各种类型的成员，然后用一个变量表达结构里的数据**

- **结构声明的形式**

**![image-20221229183159517](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229183159517.png)**

**第一和第三种都声明了结构point，但是第二种形式没有声明point，只定义了两个变量**

**函数内部声明结构的类型只能在函数内部使用，所以通常在函数外部声明结构类型，这样就可以被多个函数所使用**

### 结构变量

**声明了结构类型可以用这种类型定义很多的变量，每个变量都按照声明的形式**

- **结构变量初始化**
  - **struct a{int x;int y;};**

​				**struct a z={3,2};**

​				**struct a z={.x=3,.y=2};**

- **没有初始化的成员的结果就是0**
- ![image-20221229185740000](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229185740000.png)

- **输入结构变量的值**
- **struct a {int x;int y;};**
  
- **struct a p;**
  
- **scanf（"%d %d",&p.x,&p.y）;**

### 结构运算

![image-20221229190359471](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229190359471.png)

### 结构指针

![image-20221229190747811](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229190747811.png)

### 结构与函数

- **结构作为函数的参数**

![image-20221229191139025](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229191139025.png)

- **输入结构**

![image-20221229204740435](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229204740435.png)

**C在调用函数时传入的只是值**

**相当于传入的是克隆了一个外面的结构，p与main中的y是不同的**

**在函数读入了p的值后，没有任何东西返回到main，所以y还是{0，0}**

**为了让y与p的值相等，可以在输入函数中，创建一个临时的结构变量，然后把这个结构返回给调用者**

![image-20221229210325978](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229210325978.png)

- **指向结构的指针** 

![image-20221229210829945](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229210829945.png)

**—>表示指针指向所指的结构变量中的成员**

**结构体函数传回的指针可以被复用和再赋值**

### 结构数组

- **struct date dates[100]; 有100个date结构组成的数组，数组的名字是dates，数组的每一个元素是一个date结构变量**

  - **struct date dates[]={**
    **{4,5,2005},{2,4,2005}**    

  **};**     

  -  **对date结构数组进行初始化，{4.5.2005}是dates[0]的值，一次类推**

- **结构中的结构**

  - **struct and{**

    **struct date sdate;**

    **struct time stime;**

    **};**

    - **已经有了一个date和time类型的结构，然后可以定义一个and的结构，结构里第一个成员变量是date，第二个成员变量是time**

- **嵌套的结构**![image-20221229214826143](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229214826143.png)

![image-20221229215124389](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229215124389.png)

**结构中的结构的数组**

![image-20221229215432525](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229215432525.png)



## 自定义数据类型

- **typedef**

- **c语言提供一个叫typedef的功能来声明一个已有的数据类型的新名字**
- **typedef int length;**
- **使得length成为int类型的别名**
- **这样length这个名字可以代替int出现定义变量和参数声明的地方**
  - **length a，b，len；**
  - **length numer[10];**

**typedef可以改善程序的可读性**

![image-20221229222734542](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229222734542.png)

**把typedef到Date中间的结构体用Date来表示**

## 链表

- **链表是常见的重要数据结构，根据需要使用的内存空间开辟内存**
- **链表的形式（单向）![img](https://gitee.com/HSRBT_T/picture/raw/master/img/2d1dcb64e8d044128e5868bd99dd8528.png)**
  - **phead是“头指针”变量，它存放的是地址，该地址指向下一个元素，每个元素称为“结点”**
  - **结点包括两个部分：1.需要使用的具体数据    2.下一个结点的地址**
  - **最后一个元素不再只想其他元素称为“表尾”，它的的地址为NULL表示链表到此结束**

- **链表中元素的内存地址可以是不连续的，要找一个元素，必须找到它的上一位元素，根据他提供的下一位地址才能找到下一位元素，如果不提供“头指针”，则整个链表无法访问**

- **链表必须利用指针变量才能实现，即结点必须包含一个指针变量，指向下一个结点**

- **链表的建立常用结构体变量实现，在结构体变量中用一个指针成员指向下一个结点地址**

  ```c
  struct student{
      int num;
      float score;
      struct student *next;//next是指向下一个结点的指针，num,score 是用户用的数据
  }
  ```

  - **指针成员不仅可以指向其他结构体数据类型，也可以指向自己所在的结构体数据类型**



### 链表的创建

- **简单的静态链表**

- ```c
  #include <stdio. h>
  struct Student                            //声明结构体类型struct Student
  　　{int num;
  　　float score;
  　　struct Student*next;              
  　　} ;
  int main()
  　　{struct Student a,b,c,*head,*p;       //定义3个结构体变量a，b，c作为链表的结点
  　　a. num=10101;a. score=89.5;           //对结点a的num和score成员赋值
  　　b. num=10103;b. score=90;             //对结点b的num和score成员赋值
     c. num=10107;c. score=85;             //对结点c的num和score成员赋值
     ⁤⁤head=&a;⁤                              //将结点a的起始地址赋给头指针head
     a.next=&b;                            //将结点b的起始地址赋给a结点的next成员
     ⁤⁤b.next=&c;⁤⁤                            //将结点c的起始地址赋给a结点的next成员
     c.next=NULL;                          //c结点的next成员不存放其他结点地址
     p=head;                               //使p指向a结点
  do
  {printf("%ld %5.lf\n",p->num,p->score);  //输出p指向的结点的数据
  p=p->next;                               //使p指向下一结点
  }while(p!=NULL);                         //输出完c结点后p的值为NULL，循环终止
  return 0;
  〕
  ```

- **动态链表**

- ```c
  #include<stdio.h>
  #include<stdlib.h>
  #define LET sizeof(struct student)
  struct student{
  	int num;
  	double score;
  	struct student *next;
  }; 
  int n;
  struct student *creat(){                   //定义一个建立链表函数，返回头指针
  	struct student *head,*p1,*p2;
  	p1=p2=(struct student *)malloc(LET);   //开辟新的内存空间，也就是结点
  	n=0;
  	scanf("%d %lf",&p1->num,&p1->score);   //第一个学生的编号和成绩
  	head=NULL;
  	while(p1->num!=0){
  		n++;
  		if(n==1){                        //让头指针指向第一个结点
  			head=p1;
  		}else{
  			p2->next=p1;               //为了让前一个结点和后一个链起来
  		}
  		p2=p1;
  		p1=(struct student *)malloc(LET); //开辟新的结点
  			scanf("%d %lf",&p1->num,&p1->score);
  	}
  	p2->next=NULL;   //为了让链表结束
  	return(head);
  }
  int main(){
  	struct student *p;
  	p=creat();                             //让p指向第一个结点
  	do{
  		printf("%d %.3f\n",p->num,p->score); //输出一个节点的数据
  		p=p->next;                          //让p指向下一个结点位置
  	}while(p!=NULL);                        //当p不为空执行
  	
  }
  ```

### 遍历输出

```c
int main(){
	struct student *p;
	p=creat();                             //让p指向第一个结点
	do{
		printf("%d %.3f\n",p->num,p->score); //输出一个节点的数据
		p=p->next;                          //让p指向下一个结点位置
	}while(p!=NULL);                        //当p不为空执行
	
}
```

- 先定义一个结构体指针，让它指向头指针所指的第一个结点，再输出第一个结点数据，再让	p=p->next;   指向下一个结点位置，从一个结点按顺序输出，直到碰到NULL

### 插入

```c
struct stu

{ int a;

 struct stu *next;

}  *p,*s;
```

![image-20230416233254587](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20230416233254587.png)

- ```c
  s->next=p->next;//让s所指的结点指向p所指的结点里next指向的结点，也就是序号1的步骤
  p->next=s;//再让p所指的结点里next指向s所指的结点，也就是序号2的步骤
  ```

### 删除

![](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20230416234613514.png)

```c
q=p->next;      //q指向要删除的结点
p->next=q->next; // 为了把q所指的结点删除
free(q);         // 释放q所指结点所占的内存空间
```



## 联合

- **union**

![image-20221229223629736](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229223629736.png)

## 全局变量

- **全局变量是定义在函数外的变量**

- **全局变量具有全局生存期和作用期**

- **他们与任何函数都无关**

- **在任何函数内部都可以使用**

- **全局变量初始化**![image-20221229224328810](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229224328810.png)

**全局变量会被函数内定义的同名的变量隐藏**，**在更小的地方定义更大地方出现过的变量，更大的地方的变量会被隐藏掉**

- **注意**![image-20221229231335546](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229231335546.png)

## 静态本地变量

![image-20221229225321857](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221229225321857.png)

- **静态本地变量实际上是特殊的全局变量**
- **它们位于相同的内存区域**
- **静态本地变量具有全局的生存期，函数内部的局部作用域**
- **static在这里意思是局部作用域（本地可访问）**

## 后记：*返回指针的函数

**返回本地变量的地址是危险的，函数返回一个本地变量的地址，函数结束以后，会让外面的程序继续分配给别的地方使用**

**返回全局变量或静态本地变量的地址是安全的**

**返回在函数内malloc的内存是安全的，但是容易造成问题，最好的做法是返回传入的指针** 

## 宏定义

- **#define pi 3.14**

  - **#define 是宏。名字是pi，值是3.14**

  - **结尾没有分号，因为不是c语句**

  - **名字必须是一个单词，值可以是任何东西**
  - **在c语言的编译器开始编译之前，编译预处理程序会把程序出现的宏名字换成值**

  - **完全文本替换**

- **如果一个宏的值是其他宏的名字，也会被替换的**

- **如果一个宏的值超过一行，最后一行之前的行末需要加`\`**

- **宏的值后面出现的注释不会被当作宏值的一部分**

![image-20221230145928689](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230145928689.png)

- **没有值的宏**
  - **#define_DEBUG**
  - **这类是条件编译的，后面有其他的编译预处理指令来检查这个宏是否已经被定义过了**

- **预定义的宏**
  - **`_LINE_`是表达当前源代码所在的行号**
  - **`_FILE_`是表达当前源代码的文件名**
  - **`_DATE_`是表达当期源代码编译的日期**
  - **``_TIME_``是表达对当前源代码编译的时间**
  - **`_STDC_`是表达判断文件是不是c程序**

- **带参数的宏（像函数的宏）**
  - **`#define cube(x) ((x)*(x)*(x))`**
  - **cube（x）是名字，x是参数但没有类型，出现cube（x）的地方会被替换成`(x)*(x)*(x)`**
  - **宏可以带参数**

- **带参数宏的原则**
  - **一切都要括号**
  - **整个值都要括号，参数出现的地方都要括号**
  - **#define R1(x) ((x)*57)**
  - **#define R2(x) x*57  不加括号会导致我们想要的运算顺序，和实际运行的运算顺序不一致，导致结果不同，编译器不会显示编译错误**

- **带参数的宏可以有多个参数**
  - **#define MIN(a,b) ((a)>(b)?(b):(a))**
  - **也可以组合（嵌套）使用其他的宏**

- ![image-20221230153355021](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230153355021.png)

## 多个源代码文件

- **有多个.c文件需要使用项目，把它们放进项目里**

![image-20221230155159873](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230155159873.png)

- **一个.c文件是一个编译单元**
- **编译器每次编译只会处理一个编译单元**

### **头文件**

- **把函数原形放到一个头文件（.h结尾）中，在需要调用这个函数的源代码文件（.c文件）中#include这个头文件，就能让编译器在编译的时候知道函数的原型**

- **#include**![image-20221230160957972](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230160957972.png)

![image-20221230161221547](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230161221547.png)

- **自己的头文件用双引号，系统给的用<>**



- **#include的误区**

![image-20221230161922742](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230161922742.png)

- ![image-20221230162205593](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230162205593.png)

- **不对外公开的函数**

![image-20221230162248456](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230162248456.png)

## 声明

- **变量的声明**
  - **int i;是变量的定义**
  - **extern int i; 是变量声明**

- **声明是不产生代码的，定义是会产生代码的**

- **声明与头文件**![image-20221230162949491](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230162949491.png)

- **重复声明**![image-20221230163016301](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230163016301.png)

- **标准头文件结构**

![image-20221230163652566](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230163652566.png)

## 格式化的输入输出

![image-20221230164123066](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230164123066.png)

**%到type中间叫格式字符串**

- **Flag**![image-20221230164253333](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230164253333.png)

- **width或prec**![image-20221230164529026](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230164529026.png)

- **hIL**

  ![image-20221230164814152](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230164814152.png)

- **输出的类型**

![image-20221230165114158](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230165114158.png)

- **scanf**

![image-20221230165532528](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230165532528.png)

![image-20221230165732567](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230165732567.png)

- **printf和scanf的返回值**

  ![image-20221230170018224](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230170018224.png)



## 文件输入输出

- **用>和<做重新定向**
- **打开文件的标准代码![image-20221230181339759](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230181339759.png)**
  - **FILE相当于结构代表着需要打开的文件的信息**
  - **fp一定指向fopen函数**
  - **两个参数第一个是文件名，r表示打开那个文件夹来读**
  - **返回值NULL表示没有打开，所以需要判断打没打开**
  - **返回不是NULL代表打开了文件可以做接下来的程序，最后fclose（fp）；关闭函数**
  - **如果是NULL可以告诉文件没有打开**
  - ![image-20221230182343690](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230182343690.png)

**x前面的省略号的意思是，可以在其他符号后面加x**

## 二进制文件

![image-20221230182825802](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230182825802.png)

- **文本文件和二进制文件的选这**

![image-20221230183142153](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230183142153.png)

![image-20221230183454527](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230183454527.png)

- **程序为什么需要文件**

![image-20221230183713267](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230183713267.png)

- **二进制读写**

  ![image-20221230184920444](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230184920444.png)

**fread读，fwrite写**

- **在文件中定位**![image-20221230210222145](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230210222145.png)

- **可移植性**

![image-20221230210336839](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230210336839.png)

## 按位运算

- **把整数当作二进制进行运算**

- **.c有这些按位运算的运算符**

![image-20221230212502265](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230212502265.png)

- **按位与&**

  - **两个2进制数，位数一致的数，两数为1则为1**

    - **5------>0101**

      **3------->0011**

      **5&3-------->0001**


![image-20221230212706945](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230212706945.png)

- **按位或|**

  - **两个2进制数，位数一致的数，只要有一个为1就为1**

    - **5------>0101**

      **3------->0011**

      **5|3-------->0111**


![image-20221230213128907](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230213128907.png)

- **按位取反~**

![image-20221230213257764](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230213257764.png)

- **按位异或^**

![image-20221230213805464](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230213805464.png)

- **左移<<**

  ![image-20221230214056687](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230214056687.png)

- **右移>>**

  ![image-20221230214339417](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230214339417.png)

- **逻辑运算和按位运算**

![image-20221230213556336](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230213556336.png)

## 位段

![image-20221230215115018](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230215115018.png)

![image-20221230215503167](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221230215503167.png)

## 全部运算符优先级

![image-20221231171437675](https://gitee.com/HSRBT_T/picture/raw/master/img/image-20221231171437675.png)

## 十进制转换为二进制

- 整**数转换为二进制**

  -  **除2之后将余数倒序排列， 直到商小于1** 

    **201 / 2 = 100······1**

    **100 / 2 = 50  ······0**

    **50 / 2 = 25    ······0**

    **25 / 2 = 12    ······1**

    **12 / 2 = 6      ······0**

    **6 / 2 = 3        ······0**

    **3 / 2 = 1        ······1**

    **1 / 2 = 0        ······1    (商小于1，结束计算并将余数倒序排列)**

- **其他进制转化同理**
- **二进制运算右边对齐左边缺多少补多少0**

## C语言标识符

**c语言中标识符是由字母（A-Z,a-z）、数字（0-9）、下划线“_”组成，并且首字符不能是数字，但可以是字母或者下划线。例如，正确的标识符：abc，a1，prog_to。C语言中把标识符分为三类：关键字，预定义标识符，用户自定义标识符。**

- **关键字：像int ，double，main，这样的**
- **预定义标识符像define，include这样的**
- **用户自定义标识符自定义的**
- **标识符不能使用关键字，可以用预定义标识符但失去原有含义**

## 常量

**E的两边必有数，右边必须是整数，点也不行**

**常量有整型，字符型，实型**

## 三大结构

**顺序结构，分支结构，循环结构**

## math函数

| 1    | [double acos(double x)](https://www.runoob.com/cprogramming/c-function-acos.html) 返回以弧度表示的 x 的反余弦。 |
| ---- | ------------------------------------------------------------ |
| 2    | [double asin(double x)](https://www.runoob.com/cprogramming/c-function-asin.html) 返回以弧度表示的 x 的反正弦。 |
| 3    | [double atan(double x)](https://www.runoob.com/cprogramming/c-function-atan.html) 返回以弧度表示的 x 的反正切。 |
| 4    | [double atan2(double y, double x)](https://www.runoob.com/cprogramming/c-function-atan2.html) 返回以弧度表示的 y/x 的反正切。y 和 x 的值的符号决定了正确的象限。 |
| 5    | [double cos(double x)](https://www.runoob.com/cprogramming/c-function-cos.html) 返回弧度角 x 的余弦。 |
| 6    | [double cosh(double x)](https://www.runoob.com/cprogramming/c-function-cosh.html) 返回 x 的双曲余弦。 |
| 7    | [double sin(double x)](https://www.runoob.com/cprogramming/c-function-sin.html) 返回弧度角 x 的正弦。 |
| 8    | [double sinh(double x)](https://www.runoob.com/cprogramming/c-function-sinh.html) 返回 x 的双曲正弦。 |
| 9    | [double tanh(double x)](https://www.runoob.com/cprogramming/c-function-tanh.html) 返回 x 的双曲正切。 |
| 10   | [double exp(double x)](https://www.runoob.com/cprogramming/c-function-exp.html) 返回 e 的 x 次幂的值。 |
| 11   | [double frexp(double x, int *exponent)](https://www.runoob.com/cprogramming/c-function-frexp.html) 把浮点数 x 分解成尾数和指数。返回值是尾数，并将指数存入 exponent 中。所得的值是 x = mantissa * 2 ^ exponent。 |
| 12   | [double ldexp(double x, int exponent)](https://www.runoob.com/cprogramming/c-function-ldexp.html) 返回 x 乘以 2 的 exponent 次幂。 |
| 13   | [double log(double x)](https://www.runoob.com/cprogramming/c-function-log.html) 返回 x 的自然对数（基数为 e 的对数）。 |
| 14   | [double log10(double x)](https://www.runoob.com/cprogramming/c-function-log10.html) 返回 x 的常用对数（基数为 10 的对数）。 |
| 15   | [double modf(double x, double *integer)](https://www.runoob.com/cprogramming/c-function-modf.html) 返回值为小数部分（小数点后的部分），并设置 integer 为整数部分。 |
| 16   | [double pow(double x, double y)](https://www.runoob.com/cprogramming/c-function-pow.html) 返回 x 的 y 次幂。 |
| 17   | [double sqrt(double x)](https://www.runoob.com/cprogramming/c-function-sqrt.html) 返回 x 的平方根。 |
| 18   | [double ceil(double x)](https://www.runoob.com/cprogramming/c-function-ceil.html) 返回大于或等于 x 的最小的整数值。 |
| 19   | [double fabs(double x)](https://www.runoob.com/cprogramming/c-function-fabs.html) 返回 x 的绝对值。 |
| 20   | [double floor(double x)](https://www.runoob.com/cprogramming/c-function-floor.html) 返回小于或等于 x 的最大的整数值。 |
| 21   | [double fmod(double x, double y)](https://www.runoob.com/cprogramming/c-function-fmod.html) 返回 x 除以 y 的余数。 |
