## 语言的分类
**形式语言—用途**
 - 数据描述语言 （例 ：JSON ， HTML，XHTML，SQL）
 - 编程语言（例：C，C++， Java）
形式语言—表达方式
 - 声明式语言（只告诉你他的结果是怎么样的，例：JSON）
 - 命令型语言（会告诉你达成这个结果他的每个步骤是怎么样的，例C++、C、Java、C#、Python、Ruby、Perl、T-SQL、JavaScript）

## 语言按语法分类
 - 非形式语言 
 - 形式语言（乔姆斯基谱系）
 说明：0123属于包含关系
 
	 - 0型  无限制文法
	 - 1型 上下文相关文法
	 - 2型 上下文无关文法
	 - 3型  正则文法
	

## 产生式（BNF）
说明：巴科斯-诺尔范式 最经典最常用，简称BNF。

 - 用尖括号括起来的名称来表示语法结构名
 - 语法结构分成基础结构和需要用其他语法结构定义的复合结构
	 - 基础结构称终结符
	 - 复合结构称非终结符
 - 引号和中间的字符表示终结符
 - 可以有括号
 - *表示重复多次
 - | 表示或
 -  +表示至少一次

## 通过产生式理解乔姆斯基普系
 - 0型 无限制文法

```
  `？::=?
```

 - 1型 上下文无关文法
	

```
 "<A>::=?"
```

 - 2型 上下文无关文法

```
<A>::=?
```
3型 正则文法

```
<A>::=<A>?
<A>::=?<A> ❌
```

## 图灵完备性

 - 图形完备性
 - 命令式——图灵机
	- goto
 	- if和while
 - 声明式——lambda
	- 递归

## 动态与静态
**动态**

 - 在用户的设备/在线服务器上
 - 时机：产品实际运行时
 - 术语：Runtime
 
 **静态**
 - 在程序员的设备上
 - 时机：产品开发时
 - 术语：Compiletime

## 类型系统
 - 动态类型系统与静态类型系统
 - 强类型与弱类型
 - 复合类型
	 - 结构体
 	- 函数签名（参数类型，返回值类型）
 - 子类型
 - 泛型
	 - 逆变/协变

## 一般命令式编程语言

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200712173523871.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhZHJ5MTIz,size_16,color_FFFFFF,t_70)

## JavaScript类型
基本数据存储在栈（stack）中（String Numble Boolean Null Undefined Symbol（注：Symbol是ES6引入的一种新的原始数据类型，表示独一无二的值。）），引用数据类型是保存在堆（heap）中的对象（对象Object、数组Array 、函数Function、Date等）
 - ###  **Number**（重点 IEEE 754 float 表示方法）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200712180901382.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhZHJ5MTIz,size_16,color_FFFFFF,t_70)
指数位默认会有一位
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200714200716851.jpg)
0.1+0.2 ！= 0.3是因为会有精度损失，最大损失3e
 
 - ### **String**
	 - ASCll（ 127 字符，无法表示中文）
	 - Unicode（基于两个字节 0000~FFFF）
	 - USC（Unicode与别的标准化组织合并 ）
	 - GB（与Unicode字符集不一致）
		 - GB2312（国标，第一个版本）
		 - GBK
		 - GB18030
 	- ISO-8859
 	- BIG5
 

###### 编码方式
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200715150845630.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhZHJ5MTIz,size_16,color_FFFFFF,t_70)
反引号：javaScript引擎解析
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200714212752986.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhZHJ5MTIz,size_16,color_FFFFFF,t_70)
 - ### **Boolean**

 - ### **Object**
	 任何一个对象都是唯一的，这与他本身的状态无关，即使状态完全一致的两个对象也并不相等，我们用状态来描述对象，我们状态的改变即是行为。
	 
	 **核心三要素**
	 - state 对象具有唯一标识性：即使完全相同的两个对象，也并非同一个对象。
	 - identifier对象有状态：对象具有状态，同一对象可能处于不同状态之下。
	 - behavior 象具有行为：即对象的状态，可能因为它的行为产生变迁。
	 
	**类**
		类是一种常见的描述对象的方式
		主要流派分为： “归类” 和 “分类”
		对于“归类”方法而言，多继承是非常自然的事情。例：c++
		而采用分类分类思想的计算机语言，则是单继承结构，并且会有一个基类Object
		javaScript比较接近分类思想，但也不完全是分类的思想， javaScript其实是一个多范式的面向对象语言
		在设计对象的状态和行为时 我们总是遵循“行为改变状态”的原则
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20200715170718322.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhZHJ5MTIz,size_16,color_FFFFFF,t_70)
	##### **javaScript 的属性的值的部分的两种形态**，
	我们可以使用内置函数 Object.getOwnPropertyDescripter 来查看，如果我们要想改变属性的特征，或者定义访问器属性，我们可以使用 Object.defineProperty
	**数据属性 attribute**：
	 - value：可以是任何的javaScript值。
	 - writable: 是否可写，为false 仅仅点运算不可改变
	 - enumerable：是否可枚举
	 - configurable:是否可以被改变， 为false所有值不可改变

	**访问器属性**：
	 - get（读属性时调用）
 	- set（写属性时调用）
	 - enumerable（决定 for in 能否枚举该属性）
	 - configurable（决定该属性能否被删除或者改变特征值。）
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020071517140424.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhZHJ5MTIz,size_16,color_FFFFFF,t_70)
	#### JavaScript 中的对象分类

	 - 宿主对象（host Objects）：由 JavaScript 宿主环境提供的对象，它们的行为完全由宿主环境决定。

	 - 内置对象（Built-in Objects）：由 JavaScript 语言提供的对象。

		 - 固有对象（Intrinsic Objects ）：由标准规定，随着 JavaScript 运行时创建而自动创建的对象实例。

		 - 原生对象（Native Objects）：可以由用户通过 Array、RegExp 等内置构造器或者特殊语法创建的对象。

	 	- 普通对象（Ordinary Objects）：由{}语法、Object 构造器或者 class 关键字定义类创建的对象，它能够被原型继承。


		##### 语法和API
		![在这里插入图片描述](https://img-blog.csdnimg.cn/20200715180052588.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhZHJ5MTIz,size_16,color_FFFFFF,t_70)
		#### 特殊对象
		函数对象的定义是：具有 [[call]] 私有字段的对象，构造器对象的定义是：具有私有字段 [[construct]] 的对象
 	

 		- Array：Array 的 length 属性根据最大的下标自动发生变化。

 		- Object.prototype：作为所有正常对象的默认原型，不能再给它设置原型了。

 		- String：为了支持下标运算，String 的正整数属性访问会去字符串里查找。

		 - Arguments：arguments 的非负整数型下标属性跟对应的变量联动。

		 - 模块的 namespace 对象：特殊的地方非常多，跟一般对象完全不一样，尽量只用于 import 吧。
   类型数组和数组缓冲区：跟内存块相关联，下标运算比较特殊。

		 - bind 后的 function：跟原来的函数相关联。

 		
 		
 -  ### **Null**（已存在的值）
 - ### **Undefined**（未存在的值，不是关键字）
    语法上最简洁得到Undefined值的方法是 void 0
 	- **为什么f()中的undefined被当成变量重写后，后面能取到值。但在全局以undefined为变量重写值时，console.log(undefined)还是undefined？**
 全局 undefined 本质上是window.undefined, 如果用 Object.getOwePropertyDescriptor(window, ‘undefined’) 就会看到 undefined是window的第一类属性--数据属性，而且该属性不能能被赋值（writable=false），不能被for in枚举（enumerable=false），不能删除或改变特征值(configurable=false)。这也解释为什么给undefined重新赋值后其值却不改变：因为writable=false
 - ### **Symbol**
还有一个
 - ### **Biglnt**

