#### 内容简介 ####
* [Part01](#Part01 "JavaScript 基础知识")
* [Part02](#Part02 "HTML5 热门特性")
* [Part03](#Part03 "Canvas")
* [Part04](#Part04 "JavaScript 后端开发功能 - Node.js")

### Part01 ###
` JavaScript 基础知识 `

#### 标准不过是为了竞争而存在的武器 ####
> 明白标准制定的目的。

#### 动态语言和静态语言 ####
* 静态类型语言，结构非常规范，便于调试，类型安全，效率高。比如：C、C++。
* 动态类型语言，不方便调试，要运行起来后才能发现一些错误。目前，主要的动态编程语言有 PHP、Visual Basic、Ruby、Python、JavaScript、Groovy 和 Perl 等。

#### 开发效率的高度取决于两大因素 —— 自身和外在 ####
* 自身因素包括开发者的逻辑思维能力、对开发语言和工具的熟悉程度。
* 外在因素通常包括工具的灵活度、代码复用率、语法复杂度等。

#### JavaScript = ECMAScript + DOM + BOM ####
* ECMAScript 定义了脚本语言的所有属性、方法和对象。它是 JavaScript 的一部分，也可以是其他语言的一部分，比如：Flash 中的 ActionScript。
* DOM - 文档对象模型( Document Object Model )，一个与系统平台和编程语言无关的、中立的应用程序编程接口( API )，允许程序通过接口访问并更改文档的内容、结构和样式。
* BOM - 浏览器对象模型( Browser Object Model )。

#### JavaScript 语法基本要素 ####
* 区分大小写。
* 常量不区分类型。
* 每条语句结尾可以省略分号。
* 注释与 C、C++、Java、PHP 相同。
* 代码段要封闭。

#### JavaScript 数据类型 ####
* 字符串 - String
* 数字 - Number
* 布尔值 - Boolean
* 数组 - Array
* 对象 - Object
* Null
* undefined
* NaN

#### JavaScript 内置对象 ####
* String
* Number
* Boolean
* Array
* Object
* 正则表达式对象 - RegExp
* 日期对象 - Date
* 函数对象 - Function
* 静态数学对象 - Math

##### 注意 - 20170514 #####
1. Null 和 undefined 没有对应的内置对象，只在赋值和对比时使用。
2. 除了 Math 对象，其他内置对象都可以用 new 关键字调用。
3. 常见的 window 对象和 document 对象不是 JavaScript 内置对象，而由浏览器 BOM 和 DOM 提供，在 Node.js 等非浏览器环境下是无法调用的。
4. 单双引号都可以用来定义字符串对象。
5. NaN - Not a Number，主要用于处理计算中出现的错误情况。
6. Boolean 对象初始化值为 0、-0、null、""、false、undefined、NaN 时，对象值就是 false，反之则为 true。
7. 对象通过中括号运算符能够创建任意名称的对象成员。

##### 疑问 - 20170514 #####
1. 取整同时转成数值型
> `"10.567890"|0 === 10`
2. 日期转数值
> `+new Date() === new Date().getTime()`
3. a, b 交换数值
> `var a = 1, b = 2; a = [b, b = a][0];`
***
> Part02 -
 HTML5 热门特性
***
> Part03 -
 Canvas
***
> Part04 -
 JavaScript 后端开发功能 - Node.js
