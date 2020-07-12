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
 - Number
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200712180901382.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhZHJ5MTIz,size_16,color_FFFFFF,t_70)
 - String
 - Boolean
 - Object
 - Null
 - Undefined
 - Symbol
还有一个
 - Biglnt

