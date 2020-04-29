# 每周总结可以写在这里

## 编程语言通识

### 非形式语言
  * 中文、英文
### 形式语言（乔姆斯基普系）
  * 0型 无限制文法
    * ?::=?
  * 1型 上下文相关文法
    * ?<A>?::=?<B>?
  * 2型 上下文无关文法
    * <A>::=?
  * 3型 正则文法
    * <A>::=<A>?
    * <A>::=?<A>

### 产生式(BNF)
  * 尖括号括起来的名称来表示语法机构名
  * 语法结构分成基础结构和需要用其他语法结构定义的复合结构
  * 引号和中间的字符表示终结符
  * 可以有括号
  * *表示所有
  * |表示或
  * +表示至少一次
  ```
  <Program>:="a"+

<Number> = "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"

<DecimalNumber> = "0" | (("0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9")<Number>*)
// 正则方式定义
<DecimalNumber> = /0|[1-9][0-9]*/
// 乘除
<MultiplicativeExpression> = <DecimalNumber> |
    <MultiplicativeExpression> '*' <DecimalNumber> |
    <MultiplicativeExpression> '/' <DecimalNumber>
// 加减运算
<AdditiveExpression> = <MultiplicativeExpression> |
    <AdditiveExpression> "+" <MultiplicativeExpression> |
    <AdditiveExpression> "-" <MultiplicativeExpression>
// 逻辑运算
<LogicExpression> = <AdditiveExpression> |
    <LogicExpression> "||" <AdditiveExpression> |
    <LogicExpression> "&&" <AdditiveExpression>

<PrimaryExpression> = <DecimalNumber> |
    "(" <LogicExpression ")"
  ```

### 图灵完备性
  * 图灵完备性
    * 命令式--图灵机
      * goto
      * if和while 
  * 声明式--lambda
    * 递归

### 动态与静态
  * 动态
    * 在用户的设备、在线服务器上
    * 产品实际运行时
    * Runtime
  * 静态
    * 在程序员的设备上
    * 产品开发时
    * Compiletime

### 类型系统
  * 动态类型系统与静态类型系统
  * 强类型与弱类型（有隐式转换的式弱类型）
    * String + Number
    * String == Boolean
  * 复合类型
    * 结构体
    * 函数签名
  * 子类型
    * 逆变-凡是能用Function<Child>的地方，都能用Function<Parent>
    * 协变-凡是能用Array<Parent>的地方，都能用Array<Child>

### 一般命令式编程语言
  * Atom
    * Identifier
    * Literal
  * Expression
    * Atom
    * Operator
    * Punctuator
  * Statement
    * Expression
    * Keyword
    * Punctuator
  * Structure
    * Function
    * Class
    * Process
    * Namespace

  * Program
    * Program
    * Module
    * Package
    * Library

## 数据类型
### 基本数据类型
  * Number
  * String
  * Boolean
  * Null
  * Undefined
  * Object
  * Symbol

### 引用数据类型
  * Object
  * Array
  * Function

