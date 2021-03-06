# 内存分配、可变参数

==================================

* 一般Java在内存分配时会涉及到以下区域：
  * 寄存器：我们在程序中无法控制
  * 栈stack：存放基本类型的数据和对象的引用，但对象本身不存放在栈中，而是存放在堆中
  * 堆heap：存放用new产生的数据
  * 静态域：存放在对象中用static定义的静态成员
  * 常量池：存放常量
  * 非RAM存储：硬盘等永久存储空间
* 栈
  * 在函数中定义的一些基本类型的变量数据（8种基本类型）和对象的引用变量都在函数的栈内存中分配。
  * 该区域具有先进后出的特性.
  * 当在一段代码块定义一个变量时，Java就在栈中为这个变量分配内存空间，当该变量退出该作用域后，Java会自动释放掉为该变量所分配的内存空间，该内存空间可以立即被另作他用。
* 堆
  * 堆内存用来存放由new创建的对象和数组。 
  * 在堆中分配的内存，由Java虚拟机的自动垃圾回收器来管理。
* 静态存储区
  * 静态(static)，是指“在固定的位置”。静态存储里存放程序运行时一直存在的数据。
  * 内存在程序编译的时候就已经分配好，这块内存在程序的整个运行期间都存在。
  * 它主要存放静态数据、全局数据和常量。
  * 用关键字static来标识一个对象的特定元素是静态的
* 可变参数
  * 适用于参数个数不确定，类型确定的情况，java把可 变参数当做数组处理。
  * 可变参数必须位于最后一项。当可变参数个数多余一个时，必将有一个不是最后一项，所以只支持有一个可变参数。
  * ​

