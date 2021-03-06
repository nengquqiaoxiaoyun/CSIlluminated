# CSIlluminated
计算机科学概论读书笔记

## 第一章 全景图

### 1.1 计算系统

#### 1.1.1 计算系统的分层

​	由内向外为：

1. 信息层
2. 硬件层
3. 程序设计层
4. 操作系统层
5. 应用程序层
6. 通信层

#### 1.1.2 抽象

​	我们分析的计算系统的层次是抽象的一种例子。所谓抽象，是一种心理模型，是一种思考事情的方式，它删除或隐藏了复杂的细节。抽象是计算的关键。

### 1.2 计算的历史

#### 1.2.1 计算硬件简史

##### 第一代 1951-1959

​	第一代商用计算机使用*真空管*存储信息。它会大量生热，不是非常可靠。使用真空管的机器需要重型空气调节装置以及不断地维修。

##### 第二代 1959-1965

`	晶体管`的出现标志着第二代商用计算机的诞生。晶体管代替真空管成为计算机硬件的主要部件。他比真空管更小、更可靠、更快、寿命更长，也更便宜。

##### 第三代 1965-1971

​	在第二代计算机中，晶体管个其他计算机元件都被手工集成在印刷电路班上。第三代计算机的特征是集成电路，这是一种具有晶体管和其他元件以及他们的连线的硅片。集成电路比印刷电路小，它更便宜、更快并且更可靠。

##### 第四代 1971-至今

​	大规模集成化是第四代的特征。

#### 1.2.2 计算软件简史

##### 第一代软件 1951-1959

​	第一代程序是用机器语言编写的。所谓机器语言，即内置在计算机电路中的指令。用机器语言进行程序设计不仅耗时，而且容易出错。由于编写及其代码非常乏味，有些程序设计员就开发了一些工具辅助程序设计。因此，第一代人工程序设计语言出现了。这些语言被称为汇编语言，它们使用助记忆码表示每条机器语言指令。

​	那些编写辅助工具的程序设计员简化了他人的程序设计，是最初的系统程序员。

##### 第二代软件 1959-1965

​	当硬件变得更强大时，就需要更强大的工具有效的使用他们。第二代软件见证了更强的语言开发。使用高级语言，程序设计员就能够用类似于英语的语句编写指令。

​	在第二代软件末期，系统程序员的角色变得更加明显。系统程序员编写诸如汇编器和编译器这样的工具，使用这些工具编写程序的人被称为应用程序设计员。随着包围硬件的软件变的越来越复杂，应用程序设计员离计算机硬件越来越远了。

##### 第三代软件 1965-1971

​	在前两代软件时期，实用程序用于处理频繁执行的任务。装入器把程序载入内存，连接器则把大型程序连接在一起。第三代软件改进了这些实用程序，使它们处于操作系统的引导之下。

​	起初，计算机用户和程序设计员是一体的。在第一代软件末期，为其他程序设计员编写工具的程序设计员的出现带来了系统程序设计员和应用程序设计员的区分。但是，程序设计员仍然是用户。在第三代软件中，系统程序员为其他人编写软件工具。计算机用户的概念骤然出现了，他们不再是传统意义上的程序员。

##### 第四代软件 1971-1989

​	20世纪70年代出现了更好的程序设计技术，即结构化程序设计方法，这是一种有逻辑、有规则的程序设计方法。此外，还出现了C语言，使用这种语言，用户可以在高级程序中使用一些汇编语句。

​	更好、更强大的操作系统也被开发出来了。

##### 第五代软件 1990-至今

​	第五代中有三个著名事件，即在计算机软件业具有主导地位的Microsoft公司的崛起、面向对象的设计和编程方法的出现以及万维网的普及。

​	第五代软件最重要的特征是用户概念的改变。首先出现的用户是程序设计员，他们编写程序来解决自己或他人的问题。接下来出现的用户是系统程序员，他们为其他程序员编写越来越复杂的工具。到20世纪70年代早期，应用程序员使用这些复杂的工具为非程序员编写应用程序。

### 1.3 计算工具与计算学科

​	对于那些工具制作者来说，计算是一种学科（低级工具），或者计算这种学科使他们的工具成为可行的（将一种应用程序构建在另一种应用程序之上）。

​	学科被定义为一种学习领域。

## 第二章 二进制数值与计数系统

### 2.1 数字与计算

### 2.2 位置记数法

	>基数：技术系统的基本数值，规定了这个系统中使用的数字量和数位位置的值

​	2进制的基数就是2，8进制的基数就是8以此类推

> 位置计数法：一种表达数字的系统，数位按顺序排序，每个数位都有一个位值，数字的值是每个数位和位值的乘积

#### 2.2.1 二进制、八进制和十六进制

​	任何计数系统中的最大数字比基数小1。要用任何基数表示计数值，只需要两个数字。0位于最右边，1在0的左边，这个数字表示基数值本身。

#### 2.2.2 其他记数系统中的运算

#### 2.2.3 以2的幂为基数的记数系统

​	把二进制转换成八进制只需要**从右往左**每三位一组，把每组数字转换成相应的八进制数。

> 11101100 转换成 011 101 100 对应的八进制 为
>
> 011: 3 , 101: 5, 100: 4 所以八进制为： 354

把八进制转换为二进制 只需要把每个数字转换成三位一组的二进制即可

---

​	二进制和十六进制的转换和八进制是一样的道理，只需要四位一组即可。

​	二进制可以和他们快速转换的原因在于8或16是2的幂。

#### 2.2.4 把十进制数转换成其他数制的数

​	用十进制数除以基数，得到商和余数，重复这一步骤知道商为0。转换的结果就是由下往上余数代表的对应的其他数制的值。

​	exp: 将十进制数161转换成16进制

​	161/16 = 10余1

​	10/16 = 0余10 结果为 A1

#### 2.2.5 二进制数值与计算机	

​	计算机中的所有信息都是用二进制数值表示的，原因在于计算机中的每个存储位只有高电平和低电平两种信号。

​	每个存储单元称为一个二进制数字，简称位。

## 第三章 数据表示法

### 目标

- 区分模拟数据和数字数据

  ​	模拟数据是一种连续表示法，模拟它表示的真实信息。数字数据是一种离散表示法，把信息分割成了独立的元素。

- 解释数据压缩和计算压缩率

  ​	数据压缩就是减少存储一段数据所需的空间。压缩率说明了压缩的程度，是压缩后的数据大小除以原始数据大小的值。压缩率的单位可以是任意的。压缩率是一个0到1之间的数。压缩率越接近0，压缩程度越高。

- 解释负数和浮点数的二进制格式

  ​	假定我们限制位数为8位，则有0-255个数字用来表示正负数。我们用00000000到01111111表示正数的0-127用11111111到10000000表示负数的-1到-128。负数的最左边一位用来表示这是负数。如果要将正数变为负数只需要对每一位取反再加1。这种表示法称为二进制补码。

  ​	十进制中的浮点数转换为二进制需要用这个数乘以2得到一个数，这个数的小数点左边就是第一位结果，右边是新的基数，用新基数不断乘以2，直至乘法结果中的小数部分为0。

  exp: 20.25 转换为二进制为

  20 -> 2进制 = 10100

  0.25 -> 2进制 = 0.25 * 2 = 0.5

  ​			= 0.5 * 2 = 1.0

  ​			= 10100.01

- 描述ASCII和Unicode字符集的特征

  ​	ASCII字符集用8位表示每个字符，所以一共可以表示256个字符。虽然足够表示英语，但是却无法满足国际需要。而Unicode把ASCII字符集作为了一个子集，每个字符的编码都为16位。为了保持一致，Unicode字符集被设计为ASCII的超集。也就是说Unicode字符集中的前256个字符与扩展ASCII字符集中的完全一致。

- 解释声音的本质和它的表示法

  ​	当一系列空气压缩震动我们的耳膜时，会给我们的大脑发送一些信号，我们就感觉到了声音。因此，声音实际上是由于我们的耳膜交互的声波定义的。要表示声音，必须正确地表示声波。

  ​	要在计算机上表示音频数据，必须数字化声波，把它分割成离散的、便于管理的片段。方法之一是真正数字化声音的模拟表示法。也就是说，采集表示声波的电信号，并用一系列离散的数值表示它。

- 解释RGB值如何定义颜色

  ​	在计算机中，颜色通常用RGB表示，这其实是三个数字，说明了每种原色相对份额。如果用0到255的数字表示一种元素的份额，那么0表示这种颜色没有参与，255表示它完全参与其中。

- 区分光栅图形和矢量图形

  ​	逐个像素存储图像信息的方法称为光栅图形格式。目前流行的几种光栅图形格式有位图（BMP）、GIF、JPEG。

  ​	矢量图形是一系列描述线段的方向、线宽和颜色的命令。由于不必记录所有的像素，所以采用这种格式的文件一般比较小。

- 解释时间和空间视频压缩

  ​	时间压缩：根据连续帧之间的差别压缩电影的技术

  ​	空间压缩：基于静态图像的压缩技术的电影压缩技术

## 第四章 门和电路

### 目标

- 识别基础的门并描述每种门的行为
  1. 与门：有0出0
  2. 或门：有1出1
  3. 非门：取反
  4. 异或门：相同出0，不同出1
  5. 与非门：有0出1
  6. 或非门：有1出0

- 描述如何用晶体管实现门

  ​	门使用晶体管建立输入值和输出值之间的映射。晶体管有三个接线端，即源极、基极和发射极，发射极通常被连接到地线。晶体管只能是开或关两种状态，由基极电信号决定。当基极信号是高电平，源极信号被接地、从而关闭了晶体管。如果基极信号是低电平，则源极信号是高电平，晶体管被打开。

  ​	非门的图解几乎与原始晶体管一样。与非门需要两个晶体管上面一个晶体管的发射极接到下面一个的源极。或非门的两个晶体管使用一个源极信号。在与非门和或非门再加上一个非门就有了与门和非门。

- 比较半加器和全加器之间的异同点

  ​	半加器有一个与门和异或门组成，只能执行两位数的和。求和是异或门，执行进位的是与门。

  ​	半加器能产生进位但是不能处理进位，而全加器可以。它们本质上是一样的，只是全加器比半加器多一个接收进位的输入端，这样全加器每一次都要考虑来自低位的进位，而半加器不用考虑，直接把两个二进制数相加就行。

- 描述多路复用器是如何运作的

  ​	多路复用器根据称为选择信号或选择控制线的输入信号选择用哪个输入信号作为输出信号。

  > 多路复用器：使用一些输入控制信号决定用那些输入数据线发送输出信号的电路

  ​	假设有一个多路复用器有三条控制线S0，S1，S2，有八条输入线D0-D7。因为三条控制线被译为一个二进制数，所以三条控制线就有八种控制输入的方式(2的3次方)。如果三条线都是0，那么控制的就是D0，其他的同理。

- 解释如何操作S-R锁存器

  ​	初始化S为0R为1，则X就为1，当S变为1，S-R锁存器将保持1的状态。把R设置为0S为1，则Y为1，当R变为1，电路保持-的状态。如果S和R都为1无论当前存储的值是什么，电路就保持为当前状态。

- 描述四代集成电路的特征

  ​	VLSI（超大规模集成）芯片上的门不像小规模集成电路中的门一样，它们不是独立的。VLSI芯片上嵌入的电路具有很高的门-引脚比。也就是说，许多门被组合在一起，创建的复杂电路只需要很少的输入和输出值。多路复用器是这种电路的一个例子。

## 第五章 计算部件

### 目标

- 列出冯诺依曼机的部件和他们的功能

  1. 存放数据和指令的内存单元

     ​	内存是存储单元的集合，每个存储单元有一个唯一的物理地址

  2. 对数据执行算数和逻辑运算的算数逻辑单元

     ​	算数逻辑运算单元能执行基本的算术运算和逻辑运算。ALU操作的是字，即与特定计算机设计相关联的数据的自然单位。大多数现代ALU都有少量的特殊存储单元，称为寄存器。寄存器能容纳一个字，用户存放立刻会被再次用到的信息。

  3. 把数据从外部世界转移到计算机中的输入单元

  4. 把结果从计算及内部转移到外部世界的输出单元

  5. 担当舞台监督，确保其他部件都参与了表演的控制单元

     ​	控制单元掌管着读取 **-** 执行周期，因此是计算机中的组织力量。由于ALU和控制单元的协作非常紧密，所以他们常常被看作一个单元，被称为中央处理器（CPU）

- 描述冯诺依曼机的读取 **-** 译解 **-** 执行周期

  处理周期中的四个步骤如下：

  - 读取下一条指令

    ​	程序计数器存放的是下一条要执行的指令的地址，因此控制单元将访问程序计数器中指定的内存地址，复制其中的内容，把副本放入指令寄存器中。此时，指令寄存器存放的是将要执行的指令。在进入周期中的下一步之前，必须更新程序计数器，使他存放当前指令完成时要执行的下一条指令的地址。**由于指令连续存储在内存中，所以给程序计数器加1就可以吧吓一跳指令的地址存入程序计数器。因此，控制单元将把程序计数器加1.也可能在指令执行完之后才更改程序计数器。**

  - 译解指令

    ​	为了执行指令寄存器中的指令，控制单元必须确定他是什么指令。**在这一阶段，指令将被译解成控制型号。也就是说，CPU中的电路逻辑将决定执行什么操作。指令本身被逐字地嵌入了电路。**

  - 如果需要，获取数据

    ​	被执行的指令要完成它的任务，可能需要额外的内存访问。例如，如果一条指令要把某个内存单元中的内容装入寄存器，控制单元就必须得到这个内存单元的内容。

  - 执行指令

    ​	一旦译解了指令并且读取了操作数（数据），控制单元就为执行指令做好了准备。执行指令要把信号发送给算术逻辑单元以执行处理。当执行完成时，下一个周期开始。

- 描述如何组织和访问计算机内存
- 命名并描述不同的辅助存储设备
  1. 磁带
  2. 磁盘
  3. CD\DVD
  4. 闪存（U盘）

- 解释嵌入式系统的概念

  ​	现在这一术语指代任一预编程的、为了完成某一特殊用途的、作为大型系统一部分的计算机。这意味着终端用户或操作员极少干预嵌入式系统的运行。

  ​	在实际情况中，程序必须编写并烧入在系统包含的只读内存中，这样嵌入式系统才能完成指定的功能。**程序不能在嵌入式处理其本身之中开发和测试，程序是在台式机中编写的，并且会根据目标系统进行编译，根据嵌入式系统的处理器生成可执行代码。**

## 第六章 低级程序设计语言与伪代码

### 目标

- 列出计算机能够执行的操作

  ​	计算机是能够*存储*、*检索*和*处理*数据的*可编程*电子设备

- 描述虚拟机Pep/8的重要特性

  ​	Pep/8的内存单元由65536字节的存储空间构成。它的字长是2字节，或者16比特。这样向算数/逻辑单元（ALU）流入的数据或从算数/逻辑单元流出的数据在长度上就是16比特。Pep/8有七个寄存器。

- 区分立即寻址模式和直接寻址模式

  ​	如果殉职模式是000，那么指令的操作数说明符中存储的就是操作数。这种殉职模式称为立即寻址（i）。如果寻址模式是001，那么操作数说明符中存储的是操作数所在的内存地址名称。这种寻址模式称为直接寻址（d）。

- 区分机器语言和汇编语言

  ​	汇编语言给每条机器语言指令分配了一个助记指令码，程序员可以用这些指令码代替二进制数字。因为在计算机上执行的每个程序最终都要被翻译成机器语言的形式，所以一个名为汇编器的程序将读取每条指令的助记码，然后把它翻译成等价的机器语言。因为每种类型的计算机都有自己的机器语言，所以有多少种机器，就有多少种汇编语言和翻译程序。

## 第七章 问题求解与算法设计

- 选择排序

  ​	给一个初始下标值，假定数组中的第一个元素是最小的，依次和其他元素比较，如果其他元素比第一个元素小，就记录该元素的索引，直到找到最小的一个元素的索引。交换最小的元素和第一个元素的位置，并且初始下标+1。初始下标移动小于数组的长度-1。

  ```Java
  	int firstUnsorted = 0;
  	while (firstUnsorted < length - 1) {
  		int indexOfSmallestItem = smallestItem(firstUnsorted);
          swap(firstUnsorted, indexOfSmallestItem);
          firstUnsorted++;
  	}
  ```

- 冒泡排序

  ​	冒泡排序从数组的最后一个元素开始，比较相邻的元素对，如果下面的元素小与上面的元素，就交换这两个元素的位置。通过这种方法，最小的元素会“冒”到数组的顶部。每次迭代都会把未排序的最小元素放到它的正确位置，不过这同时会改变数组中其他元素的位置。

- 插入排序
- 快速排序

## 第八章 抽象数据类型与子程序

- 栈

  ​	栈是一种抽象复合结构，只能从一端访问栈中的元素。会计师称为LIFO，即后进先出。把栈比作自助餐厅的餐具架，使他的插入和删除操作有了个惯用语，插入操作叫Push，删除操作叫Pop。我们把项目推进栈，从栈中弹出项目。栈没有长度数学，所以没有返回栈中项目个数的操作。我们需要的是确定栈是否为空(isEmpty)的操作，因为当栈为空的时候在弹出项目会报错。

- 队列

  ​	队列也是种抽象结构，队列中的项目从一端入，从另一端出。会计师称为FIFO，即先进先出。插入操作在队列的尾部进行，删除操作在队列的头部进行。与栈一样，插入操作没有任何约束；整个FIFO行为都体现在删除操作上。

- 列表

  ​	列表有三个属性特征：项目是同构的，项目是线性的，列表是变长的。不要把列表误认为是数组，数组是内嵌结构，列表式抽象结构。

- 二叉树

  ​	二叉树是一种抽象结构，其中每个节点可以有两个后继节点，叫做子女。每个子女任然是二叉树的节点，因此也可以有两子节点，而这些子女又可以有自己的子女，以此类推，这就形成了树的分支结构。树的头部是一个起始节点，叫做根，它不是任何节点的子女。除了规定每个节点至多有两个子女外，二叉树的定义还说明了根节点和每个节点之间有且只有一条路径。这就是说，除了根节点外，，每个节点都只有一个父母节点。

- 二叉搜索树

  ​	二叉搜索树具有二叉树的形状属性。此外，二叉搜索树还具有语义属性来刻画树中节点上的值，即任何节点的值都要大于它的左子树中的所有节点的值，并且要小于它的右子树中的所有节点的值。

- 图

  ​	树是表示存在的体系结构中关系的有效方式，也就是说，一个节点至多只有一个指向它的节点。如果去掉这种约束，就得到了另一种数据结构 **-** 图。图有一组节点和连接节点的线段构成，图中的节点叫做顶点，图中的线段叫做边。图中用的定点表示对象，边则描述了定点之间的关系。

- 值参与引用参数

  ​	如果一个形参是值参，调用单元将把实参的一个副本传递给子程序。如果一个形参是引用参数，调用单元将把实参的地址传递给子程序。这意味着，由于子程序接受的只是实参的一个副本，因此它不能改变实参的内容，而只能修改副本，不会改变原始变量。相反，子程序可以改变调用单元传递给引用参数的任何实参，因为子程序操作的是实际变量，而不是变量的副本。

> Java中都是值参

## 第九章 面向对象设计与高级程序设计语言

- 编译器

  ​	*翻译用高级程序设计语言编写的程序*的程序叫做编译器。早期编译器输出的是程序的汇编语言版本，这个版本还要经过汇编器处理才能得到可执行的机器语言程序。随着计算机科学该更加深入地了解翻译过程，编译器变得更加复杂，汇编语言的阶段通常被省略了。

  ​	任何计算机只要具有一种高级语言的编译器，就能运行用种语言编写的程序。注意，编译器是一种程序，因此，要编译一个程序，就必须具有这个编译器在特定机器上的机器码版本。

- 解释器

  ​	解释器是一种程序，用于翻译和执行语句序列，解释器在翻译过语句之后会立即执行这个语句。

  > ​	Java的设计中，可移植性是最重要的特性。为了达到最佳可移植性，Java被编译成一种标准机器语言 **—** 字节码。一种名为JVM的软件解释器接收字节码程序，然后执行它。也就是说，字节码不是某个特定硬件处理器的机器语言，任何具有JVM的机器都可以运行编译过的Java程序。
  >
  > ​	用高级语言编写的程序能够在任何具有适合的编译器的机器上编译和运行，程序将被翻译成计算机能够直接执行的机器码。而Java程序则是被编译成字节码，编译过的字节码程序可以在任何具有JVm解释器的机器上运行。也就是说，Java编译器输出的程序将被解释，而不是直接被执行。Java程序总是被翻译成字节码。

- 命令式泛型

  ​	命令式泛型具有顺序执行指令的特征，变量的使用代表了内存地址，而是用赋值语句则改变这些变量的值。

- 声明式泛型

  ​	声明式泛型是一个描述结果的模型，但是完成结果的过程则不被描述。

- 面向对象语言的功能性

  ​	面向对象语言中三个必要的组成部分：封装、继承和多态。

  1. 封装

     ​	信息隐蔽是隐蔽模块的细节，目的是为了控制对细节的访问。封装是把数据和动作集合在一起，数据和动作的逻辑属性与它们的实现细节是分离的。

     ​	另一种说法是封装是实施信息隐蔽的语言特性。他用具有正式定义的接口的独立模块把实现细节隐藏了起来。一个对象只知道自身的信息，对其他对象，则一无所知。如果一个对象需要另一个对象的信息，它必须向那个对象请求信息。

  2. 继承

     ​	继承是面向对象语言的一种属性，即一个类可以继承另一个类的数据和方法。继承通过允许应用程序使用已经被测试过的类和从一个类中继承应用所需的属性来促进重用。其他必要的属性和方法可以在之后加入派生类中。

  3. 多态

     ​	多态是一种语言的继承体系结构中具有两个同名方法且能够根据对象应用合适的方法的能力。

## 第十章 操作系统

​	计算机的操作系统是系统软件的核心。操作系统负责管理计算机的资源，并提供人机交互的界面。其他系统软件则支持特定的目的，如在屏幕上绘制图像的图形软件的库。操作系统允许一个应用程序与其他系统资源进行交互。

### 多道程序设计

​	多道程序设计是在主存中同时驻留多个程序的技术；这个程序为了能够执行，将竞争CPU的访问。所有现代操作系统都采用多道程序设计技术，因此，操作系统必须执行内存管理，以确定内存中有哪些程序以及他们驻留在内存的什么位置。

### 内存管理

​	内存管理是了解主存中载有多少个程序以及它们的位置的动作。

### 进程管理

​	进程管理是了解活动进程的信息的动作。

### CPU调度

​	内存管理和进程管理都需要CPU调度，即确定某个时刻CPU要执行内存中的哪个进程。也就是说，CPU调度算法将决定把CPU给予哪个进程，以便他能够运行。

- 先到先服务

  ​	在先到先服务（FCFS）调度方法中，进程按照他们到达运行状态的顺序转移到CPU。FCFS调度是非抢先的。一旦进程获得了CPU的访问权，那么除非它强制请求转入等待状态，否则将一直占用CPU。

  ​	FCFS算法很容易实现，但却因不注意某些重要因素（如服务时间的需求）而变得复杂。虽然我们在计算周转周期的时候使用了服务时间，但是FCFS算法却没有用这些信息来帮助确定最佳的进程调度顺序。

- 最短作业优先

  ​	最短作业优先（SJN）CPU调度算法将查看所有处于准备就绪状态的进程，并分派一个具有最短服务时间的。和FCFS一样，它通常被实现为非抢先算法。

  ​	SJN算法是基于未来信息的。也就是说，它将把CPU给予执行时需要最短时间的作业。这个时间基本上是不可能确定的。SJN算法是可证明最佳的，意思是如果知道每个作业的服务时间，那么相对于其他算法来说，SJN算法能使所有作业生成最短的周转周期。但是，由于我们不可能绝对地明了未来，所以只能猜测并且希望这种猜测是正确的。

- 轮询法

  ​	CPU的轮询法将把处理时间平均分配给所有准备就绪的进程。该算法建立单独的时间片，即在每个进程被抢占并返回准备就绪状态之前收到的时间量。被抢占的进程最终会得到其他的CPU时间片。这个过程将持续到进程得到了完成所需的全部时间从而终止了为止。

  > 时间片：在CPU轮询算法中分配给每个进程的时间量。

### 分时

​	分时系统允许多个用户同时与计算机进行交互。分时系统创建了每个用户都专有这台计算机的假象。也就是说，每个用户都不必主动竞争资源，尽管幕后的实时还是如此。用户可能知道他在和其他用户共享这台机器，但不必为此付出额外的操作。操作系统负责在幕后管理资源（包括CPU）共享。

### 内存管理

> 逻辑地址：对一个存储值得引用，是相对于引用它的程序的。
>
> 物理地址: 主存储设备中的真是地址。

### 进程管理

​	操作系统必须管理的一个重要资源是每个进程使用的CPU时间。要理解操作系统是如何管理进程的，必须了解进程在生存周期中的各个阶段，理解使进程在计算机系统中正确运行所要管理的信息。

#### 进程状态

​	在计算机系统的管理下，进程会经历几种状态，即进入系统，准备执行，执行，等待资源以及执行结束。

​	操作系统必须为每个活动进程管理大量的数据。这些数据通常存储在称为程序控制块（PCB）的数据结构中。PCB存储了有关进程的各种信息，包括程序计数器的当前值（说明进程中下一条要执行的指令）。PCB还存储了进程在其他所有CPU寄存器中的值。

## 第十一章 文件系统和目录

​	要用文本指示一个特定的文件，必须说明该文件的路径，即找到这个文件所必须历经的一系列目录。路径可以是绝对地，也可以是相对的。**绝对路径名从根目录开始，说明了沿着目录树前进的每一步，直到到达了想要的文件或目录。相对路径名则从当前工作目录开始**。

## 第十二章 信息系统

### 数据库管理系统

​	数据库可以简单定义为结构化的数据集合。数据库管理系统（DBMS）是一组软件和数据的组合，有下列几部分构成：

- 物理数据库 — 存放数据的文件的集合
- 数据库引擎 — 支持对数据库内容的访问和修改的软件
- 数据库模式 — 存储在数据库中的数据的逻辑结构的规约

​	数据库引擎与专用的数据库语言交互，这种语言允许用户指定数据的结构，添加、修改和删除数据，查询数据库以获取指定的存储数据。

​	数据库模式提供了数据库中的数据的逻辑视图，独立于数据的物理存储方式。

#### 关系模型

​	在关系DBMS中，用表组织数据项和它们之间的关系。表示记录的集合。记录是相关域的集合。数据库表的每个域都包含一个数据值。表中的每个记录都包含相同的域。

​	数据库表中的记录又叫做数据库对象或实体。通常，表中会有一个或多个域被标识为键域。键域在表的所有其他记录中唯一标识了这个记录。也就是说，存储在表的每个记录的键域中的值必须是唯一的。大多数DBMS可以自动生成这种域，以确保实体的唯一性。不过这并不要求键值是连续的。

​	关系数据库表只是数据的逻辑视图，与底层的物理组织（记录是如何存储在硬盘上的）毫无关系。

#### 数据库设计

​	一种常用的设计关系数据库的方法叫做**实体关系（ER）建模**。ER建模的主要工具是ER图。ER图用图形化的形式捕捉重要的记录类型、属性和关系。数据库管理员可以根据ER图定义必要的模式，创建适合的表来支持有图指定的数据库。

​	ER图用特定的形状来区分数据库的不同部分。矩形表示记录的类型（可以把它看作数据库对象的类），椭圆表示记录的域 （或属性），菱形表示关系。

#### 结构化查询语言

​	结构化查询语言（SQL）是一种用于管理关系数据库的综合性数据库语言，它包括制定数据库模式的语句和添加、修改及删除数据库内容的语句。顾名思义，它还具有查询数据库以获取特定数据的功能。

##### 查询

```sql
select attribute-list from table_name where condition
```

##### 修改

```sql
insert into table_name values ()

update table_name set attribute = 

delete from table_name where condition
```

## 第十五章 网络

### 网路的类型

- 局域网（LAN）是连接较小地理范围内的少量计算机的网络。管理LAN的各种配置叫做拓扑。

- 广域网（WAN）是连接两个或多个相距较远的局域网的网络。广域网使得较小的网络之间可以互相通行。LAN中通常会有一个特殊节点作为网关，处理这个LAN和其他网络之间的通信。我们熟知的Internet（因特网）本质上就是一个最大的广域网。

- 城域网（MAN）有时用来指覆盖校园或城市的大型网络。与一般广域网相比，MAN更适合于特定的组织或区域使用。

> 网关（gateway）：处理它的LAN和其他网络之间通行的节点

#### 包交换

​	为了提高在共享线路上传输数据的有效性，消息被分割为大小固定、有编号的包。每个包将独立在网上传输，直到到达目的地，它们将在此被重新组合为原始的消息。这种方法叫做包交换。

​	包在到达最终目的地之前，会在各种网络的计算机之间跳跃。用于指导包在网络之间传输的设备叫做**路由器**。

​	如果通信线跨越的距离很长，那么线路上将安装**中继器**，以周期性地加强和传播信号。

### 开放式系统与协议

#### 开放式系统

​	开放式系统的基础是网络体系结构的通用模型，它的实现采用了一系列协议。开放式系统最大化了互通性的可能。

​	国际标准化组织（ISO）建立了开放系统互连（OSI）参考模型来简化网络技术的开放。它定义了一系列网络交互层。每一层处理网络通信的一个方面。

![image-20200702100258359](assets/image-20200702100258359.png)

#### 网络协议

​	网络协议参照OSI参考模型的基本概念也进行了分层，以便OSI参考模型中的每一层都能依靠自己的基础协议。这种分层有时也叫作协议栈。采用分层的方法可以在不舍弃低层基础结构的前提下开发新的协议。此外，这样还最小化了新网络协议对网络处理其他方面的影响。

​	TCP(UDP)/IP构成了Internet通信的基础。其他协议有事叫座高层协议，负责处理特定类型的网络通信。

#### TCP/IP

​	TCP是传输控制协议的缩写，IP是网际协议的缩写。它指的是一组协议和支持低层网络通信的工具程序。TCP是在IP的基础之上的。

​	IP软件处理的是包通过互相连接的网络传递到最终目的地的路由选择。TCP软件负责把消息分割成包，交给IP软件传递，目的地机器上的TCP则负责包包排序，重新组合成消息。TCP软件还要处理所有发成的错误，如一个包永远不能到达目的地。

​	UDP是用户数据报协议的缩写，它是TCP的替代品，UDP的软件角色基本上与TCP软件一样。主要的不同之处在于TCP牺牲了一定的性能，提供了更高可靠性，而UDP更快，但不那么可靠。UDP是TCP/IP协议组的一部分。由于TCP是高度可靠的，并且出于一定的历史原因，所以这套协议叫做TCP/IP协议。

#### 防火墙

​	防火墙是一台机器，它的软件作为网络的特殊网关，保护它免受不正当的访问。防火墙过滤到来的网络通信，尽可能地检查消息的有效性，可能会拒绝某些消息。

### 网络地址

​	主机名是Internet上的计算机的唯一标识。网络软件要把主机名翻译成对应的IP地址，这样更便于计算机使用。IP地址通常是四个十进制数，中间由点号分割。

​	一种形式的IP地址长为32位，称为IP4.IP地址中的每个数对应IP地址中的一个字节。IP地址中数字的范围是0到255。

​	IPv6是IPv4协议的继承者，它使用了8个组别的16位共128位地址。IPv6通常写作十六进制数字来保持长度可控。

#### 域名系统

​	主机名由计算机名加域名构成。域名由两个或多个部分组层，它们说明了计算及所属的组织或组织的一个子集。域名中的最后一部分叫做顶级域名（TLD）。

​	域名系统（DNS）主要用于把主机名翻译成数字IP地址。DNS是一种分布式数据库，没有一个组织负责跟新主机名/IP映射。