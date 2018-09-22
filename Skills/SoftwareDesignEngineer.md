`目录 start`
 
- [软考知识点](#软考知识点)
    - [【1.计算机组成与结构】](#1计算机组成与结构)
        - [【计算机中数据的表示】：](#计算机中数据的表示)
            - [【CPU】：](#cpu)
            - [【存储系统】：](#存储系统)
            - [【例题】](#例题)
            - [【输入输出系统】：](#输入输出系统)
            - [【总线系统】：](#总线系统)
            - [【加密算法】：](#加密算法)
            - [【补码】：](#补码)
            - [【访问方式】：](#访问方式)
    - [【2.程序设计语言】](#2程序设计语言)
        - [【基本概念】：](#基本概念)
            - [编译和解释：](#编译和解释)
            - [KMP模式匹配算法：](#kmp模式匹配算法)
        - [高级程序设计语言翻译流程：](#高级程序设计语言翻译流程)
        - [文法分析：](#文法分析)
        - [【考点】：正规式和DFA或NFA的转换](#考点正规式和dfa或nfa的转换)
    - [【3.操作系统】](#3操作系统)
            - [定义](#定义)
            - [进程管理](#进程管理)
            - [存储管理](#存储管理)
            - [处理机](#处理机)
            - [设备管理](#设备管理)
            - [文件管理](#文件管理)
            - [作业管理](#作业管理)
    - [【4.软件工程基础知识】](#4软件工程基础知识)
            - [成本估算](#成本估算)
            - [敏捷开发方法](#敏捷开发方法)
    - [【5.系统开发与运行】](#5系统开发与运行)
            - [【模块】](#模块)
            - [【测试方法】](#测试方法)
    - [【6.网络与多媒体基础知识】近几年没有考题](#6网络与多媒体基础知识近几年没有考题)
            - [【硬件设备】](#硬件设备)
            - [【网络安全】](#网络安全)
            - [动画与视频](#动画与视频)
            - [媒体类型：](#媒体类型)
    - [【7.数据库技术，基础】](#7数据库技术基础)
            - [关系模式（不是指表，但是是包含了表，在表的层次以上）](#关系模式（不是指表但是是包含了表在表的层次以上）)
            - [【数据依赖】](#数据依赖)
            - [【码】](#码)
            - [【范式】 应用于关系模式R<U,F>](#范式-应用于关系模式r<uf>)
            - [闭包](#闭包)
            - [模式分解](#模式分解)
    - [【8.算法与数据结构】](#8算法与数据结构)
    - [【9.面向对象技术】](#9面向对象技术)
            - [三大特性](#三大特性)
        - [关联关系：](#关联关系)
            - [面向对象分析（OOA）：](#面向对象分析（ooa）)
        - [设计模式【主要分三类】](#设计模式主要分三类)
                - [1.创建型设计模式](#1创建型设计模式)
                - [2.结构型设计模式](#2结构型设计模式)
                - [3.行为设计模式](#3行为设计模式)
    - [【常见设计模式】：](#常见设计模式)
    - [【10.标准化与知识产权】](#10标准化与知识产权)
            - [标准化](#标准化)
    - [【11.专业英语】](#11专业英语)
    - [【12.数据流图】](#12数据流图)
    - [【13.UML设计与分析】](#13uml设计与分析)
            - [图形元素讲解](#图形元素讲解)
            - [UML概念图](#uml概念图)
    - [【14.数据库设计】](#14数据库设计)
    - [【15.数据结构与算法】](#15数据结构与算法)
    - [【16.Java程序设计】](#16java程序设计)
    - [大学生们，你们知道软考的意义吗？（转）](#大学生们你们知道软考的意义吗（转）)

`目录 end` |_2018-09-22_| [码云](https://gitee.com/gin9) | [CSDN](http://blog.csdn.net/kcp606) | [OSChina](https://my.oschina.net/kcp1104) | [cnblogs](http://www.cnblogs.com/kuangcp)
****************************************
# 软考知识点
## 【1.计算机组成与结构】
### 【计算机中数据的表示】：

* **定点数**：所有数据的小数点位置是固定的，小数点位置在数据最高位是定点小数，在最低位是定点整数，会有溢出的情况发生
* **浮点数**：阶符，阶码，数符，尾数 组成， 尾数决定精度，阶码决定数据范围，最适合浮点数阶码的数字编码是移码
 - 数的机器码表示：
	- 		**原码**：符号位表示该数的符号，0正1负 。原码中分+0和-0
	- 		**反码**：符号位表示法和原码一样，正数不变，负数要取反（除掉符号位）
	- 		**补码**：正数和原码相同，负数=反码加一，最适合加减运算的数字编码
	- 		**移码**：在数X上增加一个偏移量来定义的，常用于表示浮点数的阶码部分，如果机器字长n，规定偏移量是2的n-1次方，
			移码定义：[X移]=2(n-1次方)+X(-2(n-1)<=X<2(n-1))
* **校验码**：
	* **奇偶检验码**：通过在编码中增加一位校验位来使编码中1的个数为奇数（奇校验）偶数（偶校验）
	* **海明码**：在数据位中插入k个校验码，通过扩大码距来实现检错和纠错。数据位n 校验位k 2(k次方)-1>=n+k
	* **循环冗余校验码**（CRC）:利用生成多项式的k个数据位和产生的r个校验码来进行编码，编码长度是k+r
 - 数制之间转换：2，8,10,16

#### 【CPU】：
- **运算器**：执行所有算术运算，执行所有逻辑运算并进行逻辑测试（与或非，值比较，零值测试）
- 指令寄存器（IR）：CPU执行指令的时候，先把它从内存中加载到缓冲寄存器中，再送入IR暂存，指令译码器根据IR的内容来产生各种微操作指令
- **程序计数器**（PC）：PC具有寄存信息和计数两种功能，又称为指令计数器。程序执行分为：顺序执行，转移执行。
	* 程序开始执行之前，将程序的起始地址送入PC，该地址在程序加载到内存时确定，因此PC的内容即是程序第一条指令的地址，
	执行指令时CPU会自动修改PC内容,确保永远是将要执行的下一条指令地址，顺序执行的话，只是简单的加一，
	转移指令时，指令地址根据当前地址加上一个向前或向后的偏移量得到，或者根据转移指令给出的直接转移地址得到
- **地址寄存器**（AR）：AR保存当前CPU所访问的内存单元的地址。是为了解决内存和CPU速度不匹配的问题
- **指令译码器**（ID）：指令分为操作码和地址码两部分，由该部分进行解析，协调硬件的运行
	- 		时序控制逻辑：控制指令的执行时间顺序
	- 		总线逻辑：为多个功能部件服务的信息通路的控制电路
	- 		中断逻辑：控制各种中断请求，根据优先级来对中断请求排队。逐个交给CPU执行

- **寄存器组**：
		专用寄存器，通用寄存器。上面的都是专用的，通用的可以给程序猿控制（提高速度，貌似没卵用）

####【存储系统】：
- **分类**：
	* 读写存储器（RAM）：
	* 只读存储器（ROM）：
		- 固定只读储存器（ROM）
		- 可编程的只读存储器（PROM）
		- 可擦除的可编程只读存储器（EPROM）
		- 闪速存储器（Flash Memory）

- **相联存储器** CAM 按内容寻址的存储器

- **Cache**：高速缓冲存储器：为了解决内存和CPU速度不匹配的问题而存在
    - **地址映像**：
        - 直接映像：主存按Cache的大小分成区，每个区的块数和Cache总块数相同，块号相同的映像到Cache中同一个块号那里(多个区中的同号块映像到Cache同号块上)
        - 全相联映像：主存的块调入Cache不受限制（任意位置）
        - 组相联映像：介于全相联和组相联之间
    - **替换算法** 
        - 随机替换算法 RAND：随机的
        - 先进先出 FIFO : 总是把最先调用的Cache替换出去
        - 最近最少使用 LRU：把当前近期Cache使用次数最少的那块替换出去（先看访问，再看修改状态）
        - 优化替换算法：先执行一次程序统计Cache使用情况，第二次执行程序再选择最优的算法来替换
	
- **磁盘**：
	* 磁盘存储器：由盘片，驱动器，控制器和接口组成。其存储容量有两种指标：格式化容量和非格式化容量。
		* 非格式化容量 = 面数*（磁道数/面）*内圆周长*最大位密度
		* 格式化容量 = 面数 *（磁道数/面）*（扇区数/道）*（字节数/扇区）
	* 光盘存储器：。。。

#### 【例题】
**内存按字节编址从 A5000H 到 DCFFFH的区域，其存储容量为224KB 若用16K * 4bit 的存储器芯片构成该内存，需要（ 28） 片**
		（因为位数来计算的4bit的话，前面的单位是减半的,所以最好是使用bit来计算）
		解析：DCFFFH - A5000H = 38000H (16进制)  转换成二进制 0011 1000 0000 0000 0000b 
		去掉十个0 单位就成了kb,然后就是2的5,6,7次方求和   得到224KB

#### 【输入输出系统】：
	DMA方式：
		无需CPU介入，流程：向CPU申请DMA传送，获取CPU允许后，DMA控制器接管系统总线的控制权；过程中不需要CPU结束回到CPU控制
#### 【总线系统】：
- **内部总线**： 用于芯片一级的互联，分为芯片内总线和元件级总线。芯片内总线用在集成多芯片，元件级总线用于一块电路板内元器件的连接
- **系统总线**：插件板一级的互联，用于构成计算机各组成部分（CPU，内存，接口）
- **外部总线**：又称通信总线，用于设备一级的互联，通过该总线与其他设备进行信息与


#### 【加密算法】：
- **非对称加密的算法中使用了** 私钥和公钥，私钥用于解密和数字签名，公钥用于加密和认证证书的真实性
- **数字证书**：CA组织会给用户颁发数字证书，	由CA的私钥进行创建数字证书，数字签名，然后接收方使用CA的公钥来检查其真实性和数字签名
		（检查文件内容是否被篡改）

#### 【补码】：
	一般用于浮点数的阶码，简化计算机运算部分设计，因为 符号位可以运算，减作加处理
#### 【访问方式】：
	寻址方式访问： 直接 ， 顺序 ， 随机
	内容方式访问：相联存储器
*************************************************************************
## 【2.程序设计语言】
### 【基本概念】：
#### 编译和解释：
- **编译**：词法分析，语法分析，语义分析，中间代码生成，代码优化，生成目标代码（汇编语言/机器语言）
- **解释**：分析部分：词法分析，语法分析，语义分析，然后把源程序翻译成中间代码（常用逆波兰表现形式，树，后缀式，四元，三元式）
			解释部分：对中间代码进行解释运行

	
#### KMP模式匹配算法：
求解模式串 p 中的next 函数值
next={ 
	0  ， j=1;
	max{k|1<k<j,'p 1 p 2……p k-1 '='p j-k+1 …… p j-1'}；
	1  ，其他情况（没有符合要求的k）；
}
假设 p 为 abaabaca  那么函数值为01122341
【答案的解释】：

		j: 1 2 3 4 5 6 7 8
		p: a b a a b a c a
next(j): 0 1 1 2 2 3 4 1
【自己的理解】：
	当 j=1 函数值必然是0
	当j=2 函数值必然是1
	当j=3 比较p1 和 p2 相同就是2 不同就是1
	当j=4 比较p1-> 和 <-p3 有几个相同k就是几个再加1，没有就是1
	当j=n 比较p1-> 和 <-p n-1 假设有m个相同 那么k=m+1,没有则k=1

参数传递（值传递和引用传递）：
		
*****************************************************

### 高级程序设计语言翻译流程：
	词法分析，语法分析，词义分析，中间代码重构，目标代码生成（汇编语言，机器语言）
	高级程序设计语言使用的语法一般是 上下文无关法
### 文法分析：
	是编译的一个理论支持
	推导和直接推导————规约和直接规约 相对应的
	文法G的开始符号推导出一串字符串，直到终结符，称为句型。只含终结符的句型是一个句子
	由开始符号，推导出的所有句子的全体是语言

### 【考点】：正规式和DFA或NFA的转换
	DFA：有限自动机
	NFA：无限自动机
	自动机是用来读取输入的字符串并做对应的操作
	自动机 有初态和终态，初态到终态的任意一条路径就是一个完整的字符串
![](http://i.imgur.com/7ZxejMD.png)
***************************************************************************

## 【3.操作系统】

####定义

* **分类**
	* 批处理 
	* 实时
	* 嵌入式
	* 个人
	* 网络
	* 分布式

* **特性**
	* 并发
	* 共享
	* 虚拟性
	* 确定性

* **资源管理**
	* 文件管理
	* 存储管理
	* 处理机管理
	* 设备管理
	* 作业管理

#### 进程管理
* 同步是进程间的直接制约---：进程合作的等待问题
* 互斥是进程间的间接制约---：进程竞争一个资源（进程独占）
* PV操作：
	* 实现进程同步，互斥的常用方法
	* P操作，S:=S-1 如果S>=0，执行P操作的线程继续执行，否则阻塞
	* V操作，S:=S+1 如果S>0，执行S操作的线程就会继续，否则从阻塞队列中唤醒一个线程

* **进程资源图**（分辨死锁，线程竞争）灵活辨别是否是安全序列
	* 临界资源值 = 线程数 × ( 最大需求-1) + 1
	* 不发生死锁的临界：即有一个不是阻塞，其他的线程都是只差一个资源（阻塞等待中）

#### 存储管理

* 分页
* 分段
* 页段混合

#### 处理机
* 图灵机里：有限和无限的区别就是后继码是否唯一，唯一就是有限
* 要特别注意表达式的写法，一般这种题目看读取字符结尾就可以快速选择答案

#### 设备管理

* **磁盘读取**
	* SCAN 扫描算法 磁头按当前运动方向，至最大/最小再逆序折回读取（一来一返）
	* CSCAN 单向扫描算法 磁头按当前运动方向，至最大/小，立马到最小/大又按初始的运动方向进行读取（两个单向）
	* 注意：当柱面是一样的时候，比较扇区的顺序

#### 文件管理

* **位视图存储**
    * **概括：用某号物理块除以字长得到第几个字，容量就要再除以物理块的大小再除字长**
	* 系统字长**x**，物理块大小**y**，那么第**z**号物理块需要第**z/x**个字来描述（注意是字长的区间）。容量为**w(G)** 需要 **w×1024/y/x**个字来表示

* **文件索引**
	* 分直接索引项，一级间接索引项，二级间接索引项
	* **公式**
    	* **a位直接，b位一级，c位二级**，数据块和索引块大小是**dk**，每个地址项是**e字节**，求逻辑块号**X**区间：
        	* 直接 地址索引：0 <= X < a（0开始计数）
        	* 一级 地址索引：a <= X < **d×1024/e×b**+a
        	* 二级 地址索引：d×1024/e×b+a <= X < **(d×1024/e)^2×c**+d×1024/e×b+a 
	* 求**指向的内存**大小：
    	* 直接：直接数×数据块大小  **a×d**
    	* 一级：一级数×索引块大小/地址项大小×数据块大小 **b×d/e×d**
    	* 二级：二级数×(索引块大小/地址项大小)^2 ×数据块大小 **c×(d/e)^2×d** 

* **路径问题**
	* 全文件名，从根目录开始加上文件名 eg: \d\d\f.txt
	* 相对路径从当前路径(当前工作目录)开始的路径 eg:d\
	* 绝对路径从根目录开始的路径不含文件名 eg: \d\d\

#### 作业管理

* 调度级别：高级调度（作业调度），中级调度（交换调度），低级调度（进程调度）
* 优先级调度算法：将给出的图看成树，左上为根。同层就是并发，父子关系就体现了优先级


## 【4.软件工程基础知识】

* **软件生存周期**
	* 可行性分析
	* 需求分析：功能，性能，数据，界面
	* 概要设计：分模块，定功能和关系，详细的数据库设计，数据结构设计
	* 详细设计：模块的详细算法设计，数据库的物理设计
	* 程序编码：
	* 软件测试
	* 维护：纠错维护，改错维护


* **软件生存周期模型**
	* 瀑布模型：线性顺序模型，适用于对需求有完善了解，开发周期快
	* 原型/演化模型：通过原型来不断演化
	* 螺旋模型：综合了瀑布和原型的优点，增加了风险分析
	* 增量模型：先发布核心产品，然后根据需求不断增量，调试，直到完善
	* 喷泉模型：面向对象开发过程，以用户需求为动力，以对象为驱动的模型，使开发具有迭代性和无间隙性
	* V模型：瀑布模型演化而来，强调了软件开发过程中若干个测试级别。
 
* **项目管理**
	* 启动
	* 度量
	* 估算
	* 风险分析
	* 进度安排
	* 追踪控制

****

#### 成本估算
* **估算策略**
	* 自顶向下 先确定整体时间，再按模块，分配时间
	* 自底向上 按模块分析需求时间，再向上累积得出全部时间
	* 差别估算 和类似项目比较
* **估算方法**
	* 专家估算 ：专家一人确定
	* 类推估算 ：自顶向下是类似项目总体参数对比，自底向上是两个相似的功能单元对比
	* 算式估算 ：上面两种带有主观性，这个是为了消除主观性
* **成本估算模型**
	* IBM 基于60项目的静态模型
	* Putnam（普特南）模型：动态多变量模型
	* COCOMO模型：
		* 基本COCOMO模型 静态单变量模型
		* 中级COCOMO模型 静态多变量模型
		* 详细COCOMO模型 将系统分为系统，子系统，模块三层次，
	      包含了中级并考虑了软件开发流程中每一步的成本驱动影响

****

* **风险分析**
	* 风险识别 ：
	* 风险评估 ：成本，进度，性能是三种典型的风险参考水准
	* 风险控制 ：
	* 风险策略管理
		* 避免风险
		* 控制风险
		* 分散和中和风险
		* 转移风险
* **进度管理**
	* Gantt 甘特图：描述了任务的开始和结束，并行关系，但是不能体现依赖关系
	* PERT技术：
		* 关键路径是耗时最长的路径
		* 任务松弛时间 = 最迟开始时间 - 任务最早开始时间
		> 最迟开始时间 = 从终点往回推，用最长时间（关键路径耗时）减去终点到该任务的时间
		* 任务的延时，推迟问题。应当计算由于各种原因引起的推迟路径，计算出总时间，减去原时间，不能只看一段。
* **文档管理**
	* 高质量文档
		* 针对性 分清阅读对象，来适应他们需求
		* 精确性 确切的语句，不能有二义性
		* 清晰性 简明，加以图表
		* 灵活性 各个软件项目，规模复杂性有很多差别，但是能一律看待
* **人员管理**
	* 主程序员组 ：住程序员，后备，资料员，若干程序员
	* 无主程序员组 ：相互平等，调动积极性，但是权责问题不明确
	* 层次式程序员组 ：组长，高级程序员，普通程序员。适合大型项目

* **软件过程管理**
	* UP的结构
		* 初始阶段： 建立商业案例，确定项目边界
		* 精化阶段： 分析问题领域，建立体系结构基础
		* 构建阶段： 剩余的构建和功能开发，集成为产品，此时是beta版
		* 移交阶段： 测试，基于反馈调整，交付系统

#### 敏捷开发方法
* **极限编程**
	* 将项目细分小模块，迭代编写，
	* 先测试再编程
	* 结对编程
* **水晶法** ： 每一个项目都要有一套不同的策略和方法
* **并列争求法** ：该方法使用迭代的方法，将30天一次的迭代，称为冲刺
* **自适应软件开发方法**： 
	* 1.一个使命作为指导
	* 2.特征视为客户的关键点
	* 3.过程中的等待很重要
	* 4.变化视为实际的调整，不看做改正
	* 5.确定的交付时间，迫使开发人员考虑每一个版本的关键需求
	* 6.风险也在考虑范围内

****

* **CMM 能力成熟度模型**
	*  五个级别：
		*  初始级
		*  可重复级
		*  已定义级
		*  定量管理级
		*  优化级
	* CMMI 的任务是将已有的CMM模型结合在一起，构造为集成模型
* **程序流程图**
	* 简单路径：个人看法，看到选择结构就加一，初始是一个路径（输入到输出）
	* **McCabe度量法**：V(G)=m-n+2p 
		* V(G)：路径复杂度
		* m:所有流程线
		* n:所有节点数
		* p:该有向图的强联通分量（图是有几块组成）

****

* **ISO/IEC软件质量模型中**，
	* 可靠性：
		* 成熟性，容错性，易恢复性，兼容性
	* 可维护性：
		* 易分析性：为 判定软件修改所需的努力
		* 易改变性：进行修改，适应环境变化所需的努力
		* 稳定性：与修改造成的风险后果相关
		* 易测试性：与确认修改所需的努力。

**************************************************
## 【5.系统开发与运行】

* **软件体系结构风格分类**
    * （1）**数据流风格**：批处理序列；管道/过滤器
    * （2）**调用/返回风格**：主程序/子程序；面向对象风格；层次结构
    * （3）**独立构件风格**：进程通讯；事件系统
    * （4）**虚拟机风格**：解释器；基于规则的系统
    * （5）**仓库风格**：数据库系统；超文本系统；黑板系统

* **结构化分析和设计**
	* 结构化分析方法： 是基于数据流的方法
	* 数据流图 DFD
		* 数据流：箭头表示，数据的流向
		* 加工：圆或圆框，对数据进行处理的单元接受输入数据，产生输出
		* 数据存储：信息的静态存储
		* 实体：矩形，分数据源（源头），数据潭（终点）
	* 数据字典
		* 是以准确的方式定义所有数据流和数据存储，含三类：数据流条目，数据存储条目，数据项条目
	* 加工逻辑描述
		* 也称 小说明，用来描述加工的，加工逻辑即 做什么
* **数据流图的设计原则**
	* 数据守恒原则：任何一个加工，其所有输出的数据都是从输入数据流中获得
	* 守恒加工原则：对同一个加工来说，输入输出的名字必须不同，即使组成成分是一样的
	* 每一个加工必须有输入流和输出流
	* 外部实体和数据存储之间，自身也是，！不能有数据流！
	* 父图与子图平衡原则：父图子图的输入输出流，必须一致，该原则不存在于一张图
	* 数据流必须和加工有关，必须经过加工
* 数据流图的顶层数据流图，描述了系统的输入和输出，只有一个加工表示系统

#### 【模块】
* **模块独立**：
	* 耦合：**模块之间**的紧密程度
	* 聚合：**模块内部**各元素之间联系的紧密程度

* **内聚类型**（由高到低）
	* 功能内聚：完成一个单一的功能，各个部分缺一不可
	* 顺序内聚：处理元素相同，而且必须顺序执行
	* 通信内聚：所有处理元素集中在一个数据结构的区域上
	* 过程内聚：与处理元素相关，而且必须按待定的次序执行
	* 瞬时内聚：所包含的任务必须在同一时间间隔内执行（初始化模块）
	* 逻辑内聚：完成逻辑上相关的一组任务
	* 偶然内聚：完成一组没有关系或松散的任务

* **耦合类型**（由低到高）
	* 无直接耦合：两个模块**没有任何关系**
	* 数据耦合：两个模块间只是**参数传递**简单数据
	* 标记耦合：两个模块都只和一个**数据结构**有关
	* 控制耦合：两个模块间传递的信息中有**控制信息**
	* 公共耦合：两个或多个模块，通过引用一个**公共区的数据**（数据结构和变量）而发生作用
	* 内容耦合：**最高的耦合度**
		* 当一个模块使用另一个模块内部的控制和控制信息等数据；
		* 一个模块直接转移到另一个模块；

****

#### 【测试方法】
* **白盒测试**：由低到高
	* 语句覆盖
		* 冒泡排序只要一个用例就可以达到语句覆盖
	* 判定覆盖
	* 条件覆盖
	* 判定/条件覆盖
	* 条件组合覆盖
	* 路径覆盖： 使用 McCabe度量法 计算路径复杂度，一个路径一个测试用例。
		* 但是折半查找最少两个，和流程图无关，因为结果是互斥的
		
* **黑盒测试**：
	* 等价类划分：将所有可能输入的数据划分为若干子集，然后从每一个子集中选取少数具有代表性的数据作为测试用例
	* 边界值分析
	* 错误猜测
	* 因果图
* **回归测试**：修改了旧代码后，重新测试，确认修改没有引入其他错误或导致原有代码错误
* **软件测试步骤**：。。。。。。
* **单元测试**，集成测试，确认测试，系统测试


****

* **软件维护**：
	* 改正性维护：修复错误 约占20%
	* 适应性维护：适应环境 约占25%
	* 完善性维护：增加功能，提高性能 约占50%
	* 预防性维护：为以后增加功能准备

**************************************************
## 【6.网络与多媒体基础知识】近几年没有考题
* **SO/OSI七层网络体系结构** 1979年建立
	* 应用层
	* 表示层
	* 会话层
	* 传输层
	* 网络层
	* 数据链路层
	* 物理层
	

* **TCP/IP协议**：
	* 应用层
	* 传输层
	* IP层
	* 网络接口层：包含了OSI模型中的数据链路层，物理层

* 【网络协议】：
	* **LAN模型**：IEEE802局域网标准，定义了物理层和数据链路层，数据链路层又分两个子层
	* **1. 物理层**
	* LLC ： 提供两种控制类型，面向连接，非连接
	* MAC ： 控制对传输介	* TCP/IP协议簇质的访问

	* **2. 网络接口层协议**：负责管理为物理网络准备数据
	* IP（网络层）：网络之间互联的协议
	* ARP/RARP（网络层）：硬件MAC到IP/IP到硬件MAC的转换协议
	* ICMP（网络层）：网际控制报文协议
	* TCP（传输层）：传输控制协议 ，可靠的面向连接的服务
	* UDP（传输层）：用户数据包协议 ，不可靠的面向无连接的
	* 应用层协议：NFS,Telnet,SMTP,DNS,SNMP,FTP

****
#### 【硬件设备】
* **物理层互联设备**
	* 中继器 Repeater ： 常用于两个网络节点之间物理信号的双向转发工作
	* 集线器 Hub ：对接收到的信号进行再生整形放大，以扩大网络传输距离（是相当于将各个主机直接联通，在逻辑上构成了一个共享的总线，所以就构成了一个广播域，一个冲突域）

* **数据链路层互联设备**
	* 网桥 Bridge ：扩展网络的距离和范围，提高网络性能，可靠性，安全性
	* 交换机 Switch ：基于mac地址的识别，有记录mac地址的地址表（为通信的两台主机建立专用的通道，所以是交换机的没一个接口都是自己的一个冲突域，所有接口和主机构成了一个广播域）

* **网络层互联设备**
	* 路由器 Router ：连接多个逻辑上分开的网络（） 

* **应用层互联设备**
	* 网关 GateWay ：当连接不同类型，并且协议差别大的网络时，要选用网关设备 功能：协议转换，数据分组。

****

* **DHCP** 客户端可以从DHCP服务器，获得DHCP服务器的IP地址，DNS服务器的IP地址，默认网关的IP地址，但是不能获得WEB服务器的IP地址。
* **NAT桥接**：内网主机发送数据时，NAT将源IP从内网转换成外网址。接受数据时将目的IP（外网）转换成内网网址

****

* **安全认证**：
	* PPP的NCP可以承载多种协议的三层数据包
	* PPP使用LCP控制多种链路的参数（建立，认证，压缩）
* **PPP中的安全认证类型**：
	* pap认证 是通过二次握手建立认证（明文不加密）
	* chap认证 是挑战握手认证，三次握手建立认证（密文采用MDS加密）
	* PPP的双向认证 采用的是chap的主验证风格
	* PPP的加固认证 采用的是两种 （pap chap）同时使用
* **无线接口标准** :国际电信联盟，在2000年5月 确定W-CDMA，CDMA2000，TDS-CDMA三大主流无线接口标准
	* 中国独自制定的3G标准是 TD-SCDMA

****

* IP地址
* IP地址全0是指任意网络，全1是指当前子网的广播地址

****

#### 【网络安全】
* **防火墙技术分类**
    * 包过滤型防火墙
    * 代理服务器型防火墙
    * 监测型防火墙
* **防火墙体系结构**
    * 包过滤路由器结构
    * 双穴主机结构
    * 屏蔽主机网关结构
    * 被屏蔽子网结构
* **防火墙的工作模式**
    * 透明模式
    * NAT模式
    * 路由模式
* **防火墙的安全策略**
    * 禁止外部网络ping内部网络
    * 禁止外部网络非法用户访问内部网络和DMZ区应用服务器
    * 禁止外部网络用户对内部网络HTTP、FTP、TELNET、TRACEROUTE、RLOGIN等端口访问
    * 禁止DMZ区的应用服务器访问内部网络
    * 允许外部网络用户使用DMZ区的应用服务：HTTP,HTTPS,POP3
    * 允许DMZ区内的工作站与应用服务器访问Internet
    * 允许内部企业用户访问DMZ区的应用服务：DNS,POP3,SMTP,HTTP,HTTPS,FTP等
    * 允许内部企业网络访问或通过代理访问外部网络

****

* **模拟和数字信号的转换**：A/D是模拟到数字和D/A 数字到模拟

* **声音数字化**：
    * 采样：把时间连续的模拟信号 转换成时间离散幅度连续的信号
    * 量化：把幅度上连续取值的每一个样本，转换成离散值表示，量化也称A/D转换
    * 编码：数据压缩和编码
* **图形和图像**
    * **色彩三要素**：亮度，色调，饱和度
    * **三基色原理**：红 绿 蓝 
    * **彩色空间**：
        * RGB彩色空间：
        * CMY彩色空间：
        * YUV彩色空间：
    * **图形数据的表示**：
        * 矢量：用指令描述构成一幅图像
        * 位图：使用像素点来描述
    * **图像的属性**：
        * 分辨率：像素数目
        * 图像深度（值域）：确定了图像的每个像素可能有的颜色数，或者确定灰度图像的每个像素可能有的灰度级数。 它决定了彩色图像中的可能出现的最多颜色数，或者灰度图像中的最大灰度等级
        * 真彩色和伪彩色：真彩色是像素值中存有RGB三个分量值，伪彩色是将像素值作为地址索引，在彩色查找表中查找这个像素实际的RGB值
        * 图像的压缩编码：有损（JPEG）和无损压缩
* **图像文件格式**：
    * BMP：windows采用的图像文件格式，采用位映射存储格式，不压缩
    * GIF：无损压缩算法，可以显示简单动画
    * TIFF：
    * PCX：
    * PNG：作为GIF的替代品而开发的，压缩采用的是LZ77无损压缩算法
    * JEPG：有损压缩算法，压缩比例大
    * Targe：
    * WMF：只在windows中使用，保存的是函数调用信息
    * EPS：
    * DIF：AutoCAD中常采用
* **图像的存储**
    * **例题**：使用150 DPI扫描一幅3×4英寸的图，原始24位的图像占用多少字节
        * 150DPI 表示每英寸150像素点 所以 150×150×3×4×24/8 得到占用字节数

#### 动画与视频
* **彩色电视的制式**：NTCS和PAL，前者用于日美加拿大，墨西哥等，后者用于中国，欧洲，中东
* **视频文件格式**：GIF,FLC/FLI,AVI,.MOV/QT
* **视频压缩标准**：H.261,JEPG,MPEG,DVI

#### 媒体类型：
* **感觉媒体**：使人感觉得到的媒体，音乐，图像等
* **表示媒体**：为加工处理传输感觉媒体而来的一种媒体，例如文本编码，图像编码，声音编码
* **表现媒体**：进行信息的输入输出的媒体：键盘，鼠标，扫描仪，话筒
* **存储媒体**：存储表示媒体的物理介质，硬盘，光盘
* **传输媒体**：电缆，光缆等
* 通常没有特殊说明的情况下，信息媒体就是指感觉媒体

**************************************************
## 【7.数据库技术，基础】

#### 关系模式（不是指表，但是是包含了表，在表的层次以上）
* **一个关系模式应该是五元组** R（U,D,DOM,F）
    * R 符号化的元组语义
    * U 一组属性
    * D 是属性组U中的属性所来自的域
    * DOM 为属性到域的映射
    * F 为属性组U上的一组数据依赖
* 一般使用三元组 R <U,F>
* 当且仅当 U 上的一个关系r满足F时，r称为关系模式R<U,F>的一个关系。


#### 【数据依赖】
* 数据依赖是一个关系内部属性与属性之间的一种约束关系
* 1.**函数依赖** FD
    * 若U的子集X,Y，X和Y形成唯一标识，X函数确定Y，Y函数依赖于X。记X -> Y
    * 非平凡的函数依赖：X->Y 但是Y不属于X
    * 平凡的函数依赖：X->Y Y属于X
    * X 称为该函数依赖的决定属性，决定因素
    * X->Y 并 Y->X 则 X<-->Y
* 2.**多值依赖** MVD
* 1.1 完全函数依赖：X->Y 并且X的真子集D 都存在子集 D不能->Y。
* 1.2 部分函数依赖：X->Y 但是Y不完全函数依赖于X 。
* 1.3 传递函数依赖：X->Y（Y不属于X），Y不能->X， Y->Z（Z不属于Y）则称Z对X传递函数依赖

#### 【码】
* 设 K是R<U,F>中的属性或属性组，K能完全函数依赖推出U，则K是R的候选码。
* 如果上面的K是部分函数依赖，则称K是超码，候选码是最小的超码
* 主属性：被包含在任一候选码中的属性
* 非主属性：主属性的补集
* 全码：所有属性一起构成了码
* 外码：关系模式R中属性或属性组 X 不是R的码，但是X是另一个关系模式的码，则X是外码

#### 【范式】 应用于关系模式R<U,F>
* **1NF**：每一个分量都是不可分的数据项
* **2NF**：R满足1NF，且每一个非主属性完全函数依赖任何一个候选码
* **3NF**：R满足1NF，R中不存在码X，属性组Y以及非主属性Z（Z不属于Y） 使得X->Y Y->Z Y不->X 则称R是满足3NF（取消了传递函数依赖）
* **BCNF**：满足1NF，若X->Y且Y不属于X时，X必含有码，则R是满足BCNF
    * 所有非主属性对每一个码都是完全函数依赖
    * 所有主属性对每一个不包含它的码也是完全函数依赖
    * 没有任何属性完全依赖于非码的任何一组属性

#### 闭包
* 在关系模式R<U,F>中为F所逻辑蕴含的函数依赖的全体叫做F的闭包
* 设F是属性集U上的一组函数依赖，X,Y属于U，![](http://i.imgur.com/pChaMD3.png)={A|X->A} 称为![](http://i.imgur.com/pChaMD3.png)属性集X关于函数依赖集F的闭包

#### 模式分解
* 具有无损连接性（粗略概述：不减少字段和改变元组）
* 要保持函数依赖（子模式里满足依赖关系）
* 既要保持函数依赖性，又要具有无损连接性
* 通过使用模式分解能提高关系模式能满足的范式等级

**************************************************
## 【8.算法与数据结构】
 
- 考点：
    - 排序算法，查找算法，常用算法，二叉树，图，模式匹配，线性结构，栈，队列，时间复杂度

---

- 串的模式匹配：
    - Brute-Force算法
    - KMP算法
 
- 堆串的问题
    - 字符串分串名，串值
        - 串名使用符号表存储
        - 串值使用堆串存储方法

- 循环队列求下标记得减去总长再对总长取余
- 二叉树的转换：
 
 
 
**************************************************

## 【9.面向对象技术】
* **面向对象** = 对象+分类+继承+用消息通信
* **对象**：对象名，属性，操作
    * 特性：清晰的边界，良好定义的行为，可扩展性
* **类**：对象的抽象
* **消息**：对象之间通信的一种构造（对象调用方法）

#### 三大特性
* **继承**：可分单重继承，多重继承
* **多态**：
    * 参数多态：指同一个对象，函数，过程能以一致的形式用于不同类型
    * 包含多态：子类型化，即一个类型是另一个类型的子类型
    * 过载多态：同一变量被用来表示不同的功能
    * 强制多态：通过语义操作，把一个变元的类型加以变换，以符合函数要求，不强转就会使得函数错误
* **封装**：目的是将定义和数据分离，保护数据不被对象使用者直接存取

****

* **重置**（覆盖）：指在子类中改变父类中既有函数行为的操作，通过一种动态绑定是的子类继承父类的前提下，用适合自己要求的实现去覆盖父类的实现
* **重载**：子类保留父类的函数名，但使用不同类型的参数
* **动态绑定**：以函数调用和函数本体的关联为基础，绑定动作在运行期才根据对象类型运行。也称后期绑定（应该就是根据参数来判断实例化什么对象或执行对应的方法）
* **静态绑定**：编译过程中，将函数调用与响应调用所需的代码结合的过程

****

### 关联关系：
* **泛化** ： 类和类之间的继承关系，接口之间的继承关系，类和接口的实现关系，泛化关系是从子类指向父类
* **关联** ： 当一个对象的实例和另一个对象的实例存在固定的对应关系时，关联体现的是两个类或者类和接口之间语义级别的一种强依赖关系，可以单或双向。
* **聚合** ： 体现的是整体与部分的关系，整体与部分之间是可分离的，他们各自有各自的声明周期，部分可以属于多个整体对象，也可以为多个整体对象共享
* **组合** ： 也称强聚合，整体和部分是不可分的，整体的生命周期结束也就意味着部分的生命周期结束
 
#### 面向对象分析（OOA）：
* 1.分析问题域，建立用例模型。
* 2.发现和定义对象和类
* 3.识别对象的内部特征
* 4.识别对象的外部联系
* 5.识别对象之间的交互

****

* OOA模型（面向对象分析）：
    * **5个层次**：
        * 主体层
        * 对象类层
        * 结构层
        * 属性层
        * 服务层
    * **5个活动**：
        * 标识对象类
        * 标识结构
        * 定义主题
        * 定义属性
        * 定义服务
* **OOD模型**（对象建模技术）：
    * OOA的五个层次和五个活动贯穿在OOD中
    * 四个活动构成：
        * 设计问题域部件：OOA的结果就是OOD的问题域部件
        * 设计人机交互部件
        * 设计任务管理部件：识别事件驱动任务
        * 设计数据管理部件：目的是隔离数据管理方案对其他部件的影响

* 【OMT】
    * **OMT模型**
        * 对象模型
        * 动态模型
        * 功能模型
        * 模型关系
    * **OMT步骤**
        * **分析**：
        * **系统设计**：
            * 将系统分解成子系统
            * 标识问题中固有的并发性
            * 将子系统分配到处理器和任务
            * 选择数据存储管理的手段
            * 处理对全局资源的访问
            * 选择软件中控制的实现
            * 处理边界条件
            * 设置折中的优先级
        * **对象设计**：设计者必须履行一下步骤：
            * 综合考虑三个模型以获得类上的操作
            * 设计实现操作的算法
            * 优化数据访问路径
            * 实现与外部交互的控制
            * 调整类结构以增加继承
            * 设计关联
            * 确定对象表示
            * 将类和关联包装到模块中
        * **实现**：

****

* 【UML】
    * **事物**
        * **结构事物**：模型的静态部分，描述概念或物理元素，例如：类，接口，协作，用例，主动类，构件，节点
        * **行为事物**：UML模型的动态部分。例如：交互（消息，有向线段），状态机（对象或交互的状态，圆角矩形）
        * **分组事物**：模型分解组成的“盒子”，例如：包（概念性，仅存在开发阶段，文件夹图形）
        * **注释事物**：UML的解释部分，例如：注解
    * **视图**
        * 分为三个视图域：**结构分类**，**动态行为**，**模型管理**
        * 
        * **类图**（Class Diagram）:展现了一组对象，接口，协作以及之间的关系，作为静态视图，还可以包含依赖，关联，泛化，实现，注解，约束关系等
        * 
        * **用例图**（Use Case Diagram）：展现了一组用例，参与者以及两者的关系。对系统的静态用例视图建模时，可以分两种方法：对系统的语境建模，对系统的需求建模
        * 
        * **构件图**（Component Diagram）：展现了一组构建之间的组织和依赖，通常将构建映射一个或多个类、接口或协作
        * 
        * **部署图**（Deployment Diagram）：体系结构的静态实施视图，与构件图相关，通常一个节点包含一个或多个构件，类似包图
        * 
        * **状态图**（statechart Diagram）：展现了一个状态机，它由状态，转换，事件和活动组成，一般是分析一个对象,强调对象行为的事件顺序。
            * 状态图中的状态包括状态名、内部活动、内部转换、入口和出口动作等部分
        * **活动图**（activity Diagram）：特殊的状态图，展现了系统从一个活动到另一个活动的流程
        * 
        * **交互图** ：顺序图和协作图均被称为交互图
            * 顺序图强调消息时间序列
            * 系统的动态方面建模
        * 
        * **对象图** （Object Diagram）：静态的实例，一组对象以及它们之间的关系 一般包括对象和链
        
### 设计模式【主要分三类】

##### 1.创建型设计模式

* 抽象了实例化过程，它们帮助一个系统独立于如何创建，组合和表示它的那些对象。
* 一个类创建型模型使用继承改变被实例化的类，而一个对象创建型模型将实例化委托给另一个对象
* 将一组固定行为的硬编码转移为定义一个较小的基本行为集，这些行为可以被组合成任意数目的更复杂性的行为。这样创建有特定行为的对象要求的不仅仅是实例化一个类

```
    - 生成器 Builder，是一种对象构建模式，模式通常包含Builder，ConcreteBuilder。Director 和 Product四部分
    - 
```

##### 2.结构型设计模式
> 适配器(**Adapter**)模式，桥接(**Bridge**)模式，组合(**Compontent**)模式，代理(**Proxy**)模式，享元(**Flyweight**)模式，**Facade模式**，装饰(**Decorator**)模式，命令(**Command**)模式，状态(**State**)模式

* 结构型设计模式涉及如何组合类和对象以获得更大的结构
* 结构型模式采用继承机制来组合接口或实现。
* 结构型对象模式不是对接口和实现进行组合，而是描述了如何对一些对象进行组合，从而实现新功能
 
****
 
* **Composite模式**
它将对象组合成树形结构以表示“部分-整体”
* **Flyweight模式**
该模式为共享对象定义了一个结构，强调对象的空间效率，自由共享
* **Facade模式**（外观模式）
描述了如何用单个对象表示整个子系统（外部与其内部通信必须通过一个统一的对象进行交互），模式中的facade用来表示一组对象，
外观设计模式提供一个高层次的接口是的子系统易于使用。
**适用情况:**
>  1.为复杂的子系统提供一个简单的接口
>  2.客户程序与抽象类的实现部分有很大依赖性
>  3.构建一个层次结构的子系统时，适用外观模式定义子系统每层的入口

* **Bridge模式** 将对象的抽象和实现分离，从而可以独立的改变他们。
* **Decorator模式**
描述如何动态地为对象添加职责，模式采用递归方式组合对象，从而允许添加任意多的对象职责。

##### 3.行为设计模式
* 行为设计模式涉及算法和对象间职责的分配，行为模式描述对象和类的模式以及其通信模式
* 行为模式使用继承机制在类间派发行为

-------------------------------------------------------------------------------
## 【常见设计模式】：

- **适配器 模式**（Adapter）：适配器是的一个接口与其他接口兼容，从而给出了多个不同接口的同一抽象。一般分类结构和对象结构两种：
- *类适配器*：适配器类继承被适配类，实现某个接口，在客户端类中可以根据需求来建立子类
- *对象适配器*：适配器不是继承，是使用直接关联，或称委托方式
![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/Adapter.png)
- **中介者 模式**：包装了一系列对象相互作用的方式，使得对象间的相互作用是独立变化，但是与中介者紧密联系
- **观察者 模式 Observer**：一个目标物件管理相依于它的管理物件，并且在它本身的状态发生改变时发出通知，这种模式常用来实现事件处理系统。（也称发布-订阅，模型-视图，源-收听者模式）
    - 观察者（接口）：更新信息，展示信息，给 **被观察者（形参）** 注册上观察者
    - 被观察者（接口）：发出更新通知（遍历观察者集合并注册），当自身发生改动时发出通知消息

![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/Observer.png)

- **单例模式 Singleton** 一个类只有一个实例易于外界访问
- **装饰器模式** 创建一个新类为某一个类动态添加新功能或增强原有的功能，避免代码重复或具体子类的数量增加

![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/Decorator.png)

- **策略模式** 优点：灵活添加同一问题的不同解决方案
- **状态模式** 允许对象在内部状态时变更其行为，并且修改其类：
    - 环境类（Context）：定义客户感兴趣的接口，维护一个子类的实例，这个实例就是当前状态
    - 抽象状态类（State）：定义一个接口以封装与Context的一个特定状态相关的行为
    - 具体状态类（concreteState）：每一子类实现与Context的一个状态相关的行为
    - **例题**：纸巾售卖机:有四个状态!
        - 【状态图】
        - ![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/State_zhijin.png)
        - 【类图】
        - ![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/State_zhijin2.png)
    - **例题**：TCP连接状态:![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/State_TCP.png)
- **命令模式 command**：
    - 行为请求者 与 请求实现者 之间 紧耦合 的关系
    - **将一个请求封装成一个对象**，从而可用不同的请求对客户进行参数化，支持可撤销的操作
    - 下例：使用了接口来实现多态，子类是多个的，方法同名并功能多样的
        - 代码复用好，代码结构清晰【参数类表最好不要出现标志变量，最好分离出另一个方法】

![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/Command.png)

- **桥接模式** ： 便于扩展，实现与抽象分离（解耦）对一个模块修改不影响别的模块

![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/Bridge.png)

- **抽象工厂模式** ： 提供一个创建一系列相关实例相互依赖的对象。
    - 当一个系统要独立于它的产品的创建，组合和表示时
    - 当一个系统要由多个产品系列中的一个来配置时
    - 当需强调一系列相关的产品对象的设计以便进行联合使用时
    - 想提供一组对象而不显示他们的实现过程，只显示他们的接口
    
![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/AbstractFactory.png)

- **原型模式** ： 对象创建模型： 允许一个对象创建另一个可定制的对象，封装实例化细节。
    - 实现Cloneable接口（Java自带接口），重写clone方法（在这里实例化对象，new或反射，按需求来修改）
    - 该例，组合关系，在对方使用clone来代替构造器来实例化对象，并做好了绑定操作，大量减少代码量
    
![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/Clone.png) 

- **生成器模式**：

![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/Model/Builder.png)

-------------------------------------------------------------------------

**************************************************

## 【10.标准化与知识产权】

#### 标准化
- 标准分类
    - 按适用范围：国际标准，国家标准，行业标准，企业标准，项目标准
    - 按性质分类：技术标准，管理标准，工作标准
    - 对象和作用：基础标准，产品标准，方法标准，安全标准，卫生标准，环境保护标准，服务标准
    - 法律约束力：强制性标准和推荐标准（一般是加上T）
- 知识产权：分两类
    - **工业产权**：
        - 专利，商标，厂商名称，服务标记，实用新型，工业品外观设计，原产地名称，制止不正当竞争等内容
    - **著作权**：指作者对其创作的作品享有的人身权和财产权。人身权包括发表权，署名权，修改权和保护作品完整权等；财产权包括作品的使用权和获得报酬权
    - 知识产权的特点：
        - 无形性，双重性，确认性，独占性，地域性，时间性
- 计算机软件著作权
    - 主体和客体：主体是指享有著作权的人，客体是计算机程序及其相关文档
    - 受保护的条件
        - 独立创作：开发者独立开发完成，复制和抄袭的作品不得获得著作权
        - 可被感知：作品应当是作者的创作思想在固定载体上的一种实际表达
        - 逻辑合理
    - 著作权的权利：
        - 计算机软件著作人身权：发表权和开发者身份权
        - 财产权：使用权，复制权，修改权，发行权，翻译权，注释权，信息网络传播权，出租权，使用许可权和获得报酬权，转让权
        - 软件**合法持有人**的权利：
            -  根据需要把软件装入计算机等储存设备中；根据需要进行必要的复制；为了防止复制品损坏，制作备份复制品；为了把该软件安装于计算机做的必要的修改
    - 计算机软件著作权的保护期：自开发完成之日计算 50年
**************************************************
## 【11.专业英语】
 
**************************************************
## 【12.数据流图】
 
- **主要 看细心，业务逻辑不能分析错误**
- 要看清楚所有出现的业务名词或 对存储的读写  不能有一个遗漏
- 确定数据流的起点和终点，一般存储都是叫做**表  子图里 存储必须要有读和写 缺一不可
- 注意实体是不能写错的，一般是人（某职位）


**************************************************
## 【13.UML设计与分析】
- 题目套路：
    - 第一题：读懂题目，搞定逻辑和业务流程，填补类图，填多重度等（类模型看**参数**及关联推断类名和关系（**特殊的：聚合，泛化**），切记不能随便填类名）
    - 第二题：填流程图，用例图（**突破口：特殊关系：泛化，组合**），等
    - 第三题：优化，分析，模式优化，添加功能，模式等（**概念题**）
- **注意 书写规范，看清题意**


- **候选类的选择** 使用了良性原则：
    - 不会在实际中造成危害的依赖关系，都是良性依赖
- **候选类的删除** 使用了接口隔离原则（ISP）：
    - 不应该强迫类实现依赖于他们不同的方法（不需要的方法不实现）

#### 图形元素讲解

* 用例图：
    * 消息传递：实线箭头
* 关系（类图）
    * 依赖：虚线箭头 （线上方可能注明：include-包含，extend-扩展，bind-绑定，friend-友元）
    * 关联：实线（双向）实线箭头（单向） 看成数据通道
        * 聚合：空心菱形实线： 对象做另一个对象的成员 菱形是整体方
        * 组合：实心菱形实线：
    * 泛化：实线空心箭头（可理解为继承）
    * 实现：虚线空心箭头
* 多重度：考虑时要从**对方的角度**考虑自己的数量应该是什么范围
    * 【0..1】 : 0或1
    * 【 1 】  ：只有一个
    * 【0..*】 ： 0或更多
    * 【 * 】  ： 0或更多
    * 【1..*】 ：1个或更多

![UML图](http://img4.ph.126.net/JrURAUSJexxjlxrSpnCsow==/2530178565669130094.png)
![元素说明](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E5%85%83%E7%B4%A0%E8%AF%B4%E6%98%8E.png)
![关系图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E5%85%B3%E7%B3%BB.png)
![关联图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E5%85%B3%E8%81%94.png)
![示例图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E7%A4%BA%E4%BE%8B.png)
![顺序图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E9%A1%BA%E5%BA%8F%E5%9B%BE.png)
![顺序图和用例图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E9%A1%BA%E5%BA%8F%E5%9B%BE%E5%92%8C%E7%94%A8%E4%BE%8B%E5%9B%BE%E5%85%B3%E7%B3%BB.png)
![状态图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E7%8A%B6%E6%80%81%E5%9B%BE.png)
![活动图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E6%B4%BB%E5%8A%A8%E5%9B%BE.png)
![活动图关系](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E6%B4%BB%E5%8A%A8%E5%9B%BE%E5%85%B3%E7%B3%BB.png)
![构件图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E6%9E%84%E4%BB%B6%E5%9B%BE.png)
![部署图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E9%83%A8%E7%BD%B2%E5%9B%BE.png)
![部署图关系](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/%E9%83%A8%E7%BD%B2%E5%9B%BE%E5%85%B3%E7%B3%BB.png)

****

**外链博客：**
- [一.用例图_1](http://www.cnblogs.com/silent2012/archive/2011/09/07/2169518.html) ||  [用例图_2](http://xhf123456789plain.blog.163.com/blog/static/172880482201192221826110/)
- [二.类图_1](http://www.cnblogs.com/silent2012/archive/2011/09/07/2169946.html) || [类图_2](http://blog.csdn.net/xhf55555/article/details/6896316/)
- [三.序列图](http://www.cnblogs.com/silent2012/archive/2011/09/14/2172219.html)
- [四.状态图](http://www.cnblogs.com/silent2012/archive/2011/11/01/2178278.html)
- [理解九种图](http://xhf123456789plain.blog.163.com/blog/static/172880482201192222144421/)

****

**状态图：**
![](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/UML/UML_10.jpg)

#### UML概念图
* 有点像ER图，也是描述了实体之间关系（有一对多等关系），有面向对象特有的关系


**************************************************

## 【14.数据库设计】
* 考试套路：
    * 1.补全ER图
    * 2.补全关系模式指明主外键
    * 3.添加一个实体，或修改关系模式。或者优化
* 考点：
    * ER图的补充，主外键的确定，业务关系的正确具体分析，模式优化（模式分解）
    * 注意：给出的ER图是不全的，可能还会少实体，关系
    * 一定要仔细检查大段的说明文字，不能遗漏关系，字段等
![ER图](https://raw.githubusercontent.com/Kuangcp/ImageRepos/master/Tech/ER.png)

**************************************************

## 【15.数据结构与算法】
 
**************************************************
## 【16.Java程序设计】

- 一般考的是**设计模式**直接应用于代码上，一年一个模式:要注意根据对应的设计模式的精神，来考虑代码的安排
- 特别注意**abstract**的使用，在方法，类的修饰上
- 写属性不要忘记**数据类型**，权限修饰符最好写上
- 由**子类**或**实现类**来推断出，上层**类/接口**的方法和具体实现

----------


## 大学生们，你们知道软考的意义吗？（转）
- 作者： 顾若赵
- 职称评定——关卡重重路艰难 
- 很早以前就听说计算机行业中，获得“系统分析员”(以下简称系分)称誉是从业人员的最高境界，但直到2004年年初，我才比较深入地了解了我国的系分和软考(计算机技术与软件专业技术资格(水平)考试)，并于同年以实际行动参加了该项考试，幸运地获得了国家颁发的“系统分析师”资格证书。 
- 我在IT界摸爬滚打近十年，其间开发过电脑主机板，调试过汇编程序，写过Fortran、C、Java代码，设计过方案，管理过项目，安装过网络主机，维护过网站，带领过团队，几乎所有IT岗位我都蹲过，但却没有参加过任何国家认证考试。 
- 2003年，我决定参加高级工程师职称评定，为此我在核心期刊上发表了3篇论文并通过了职称英语考试。9月份开始准备申报材料，却意外地得知我还要通过计算机应用能力考试才有资格参加社会化评审，原因仅仅因为我不是计算机专业科班出身！ 
- 当我参加了计算机应用能力考试之后，我的一位朋友告诉我：“可能今年你也评不了职称，因为计算机专业职称不评了，需要参加计算机考试。”我说：“我考了，WORD模块，刚拿的证。”他说：“两回事，你知道软考吗？” 
- 随后，我仔细研究了后来改变了我命运的那份文件——关于印发《计算机技术与软件专业技术资格(水平)考试暂行规定》和《计算机技术与软件专业技术资格(水平)考试实施办法》的通知(俗称人事部39号文)，其中第十条：通过考试并获得相应级别计算机专业技术资格(水平)证书的人员，表明其已具备从事相应专业岗位工作的水平和能力……取得高级资格，可聘任高级工程师职务。第十一条：计算机专业技术资格(水平)实施全国统一考试后，不再进行计算机技术与软件相应专业和级别的专业技术职务任职资格评审工作。果然，要想获得高级职称资格，就得真刀实枪地参加全国统考，而不用费尽心机地准备什么论文、评审材料，还要找关系与评委混个脸熟，还可能因为名额限制等原因，为此奋斗好几年。 
- 这真是太好了！我兴冲冲地在考试报名截止日期当天报了名。 
- 软考大纲——覆盖面广含金高 
- 等我开始静下心来阅读高级资格(系统分析员)考试大纲时，心差点凉了半截！这个系分的考试内容覆盖了在学校学过、报刊上看过、工作中实践过的几乎所有IT知识，而且还包括高等数学、线性代数、离散数学等早已遗忘的理论知识！不仅如此，考试还是个“体力”活儿，需要在一天内完成三场考试：第一场150分钟，考综合知识；第二场90分钟，考案例分析；第三场120分钟，考专业论文。 
- 看来，要想通过考试拿到职称资格，也并不轻松！ 
- 上网检索有关系分和软考的信息，了解到软考是国家人事部和信息产业部组织的国家级考试，目前每年举行两次。考试的级别包括：程序员、软件设计师、网络管理员、网络工程师、数据库工程师、软件评测师、信息系统监理师、信息系统项目管理师、系统分析员等20个资格。从1990年开始，软考就成为国家级考试。软考现已纳入全国专业技术人员职业资格证书制度的统一规划，从2004年1月1日开始，全国不再进行相应专业技术职务任职资格的评审工作。报考任何级别不需要学历、专业、资历条件，实现了“以考代评”，不拘一格选拔人才！ 
- 业界的一个共识是，经过十多年的发展，软考不仅为国家和社会选拔了大量的符合岗位需求的计算机软件人才，而且规范和引导了IT行业从业人员的知识结构。 
- 而网上热点话题包括软考含金量高、软考通过率低、中日软考互认等，印象最深的是某位网友经过统计得出“2002年前，获得系统分析员证书的不超过千人”的“恐怖”结论，甚至许多人把参加软考当作一种“人生挑战”。 
- 根据考试大纲内容，我找来了官方教程以及大量的相关书籍(离散数学、线性代数、计算机原理、网络原理、软件工程等等)，每天抽出时间阅读几个小时以上，有空就上网快速查找最新的计算机和软件知识。刚开始还感觉枯燥，几天后，却变得有些兴趣盎然，觉得有时间系统地看看书的感觉真好，那段时间就像一首歌唱的那样：痛，并快乐着！ 
- 考证虽是我的初衷，但是在软考大纲的指导下，有条理地理顺知识结构、总结并融会贯通理论知识与实际经验，找回因多年忙碌工作而产生的与新知识之间的落差，即使不能通过考试，也是非常有意义的收获。心态放平和了，轻装上阵。 
- 2004年5月23日，我踏入软考考场。考场秩序井井有条，感觉就像高考。后来，这日子印在了我的高级资格证书上，让我终身难忘。我认为：十年的工作积累非常重要，没有那些实践，这次通过高级资格考试简直是天方夜谭，也许这就是平时所谓的厚积薄发吧。 
- 软考作用——内涵丰富意义深 
- 细细体味，感慨颇多，软考决不只是单纯的职称考试。它的内涵非常丰富。 
- 计算机产业是个变化非常快的产业，新技术、新产品层出不穷，可谓“过尽千帆皆不是”、“大浪淘沙始见金”，但万变不离其宗。软考的诞生、快速发展，正是源于计算机产业的这个特点，同时又满足了资格评定、水平测试的社会与心理需求。 
- 在熟悉软考的日子里，我切实体会到，软考考试内容以计算机、软件专业的基本理论为“纲”，以新技术应用为“目”，命题灵活，不拘泥于具体产品和技术实现，其中又体现出优美的计算机文化和计算机“哲学”。 
- 软考的考试大纲是根据一般IT企业的岗位需求，经过科学分析、综合制定的，因此软考非常注重对实践技能的考核，使得用人单位可以据此合理配置其人力资源。 
- 软考各级证书(包括高级)获得者中，有一些还是正在苦读或刚刚毕业的大学生，这无疑大大增加了他们的就业竞争筹码，或者说，大学生可以将软考考试内容作为梳理其理论知识并弥补其实践经验不足的指南。 
- 软考能够很好地反映出工作多年的专业技术人员的知识、经验和积累，是对技术人员能力的一个很好鉴定，同时也为大家学习、更新知识提供了一个系统的参考。 
- 软考对我国IT业的贡献，是提供了一个公开、量化、中立、一致的全国统一标准的评估手段，比较科学地反映了专业技术人员的理论与应用水平。 
- 它不仅帮我圆了“高工”梦，客观上还规范、系统化了我的知识体系，让我对自己有了新的评价，新的起点！ 
- 许多考生对软考是又爱又恨，“梅花香自苦寒来”，想要通过软考以实现自我价值，确实需要花一定功夫，但功夫不会白费。套用电视剧中的一句话，颇能反映许多考生对软考的感情： 
- “如果你恨他，让他参加软考；如果你爱他，让他参加软考！” 