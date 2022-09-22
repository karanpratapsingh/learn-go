# 学习Go 

你好，欢迎来到本课程，很高兴你参与到Go学习。我希望本教学内容可以提供一个较好的学习体验。

_本课程还可以通过访问[网站](https://www.karanpratapsingh.com/courses/go) 或者 [Educative.io](https://www.educative.io/collection/5716974084816896/6319653488164864). 你的⭐是我的最大动力！_

# 目录

- **开始**

  - [什么是Go?](#什么是Go)
  - [为什么学习Go?](#为什么学习Go)
  - [安装和配置](#安装和配置)

- **第一章**

  - [你好世界](#你好世界)
  - [变量和数据类型](#变量和数据类型)
  - [字符串格式化](#字符串格式化)
  - [流程控制](#流程控制)
  - [函数](#函数)
  - [模块](#模块)
  - [包](#包)
  - [工作区](#工作区)
  - [实用命令](#实用命令)
  - [编译](#编译)

- **第二章**

  - [指针](#指针)
  - [结构](#结构)
  - [方法](#方法)
  - [数组和切片](#数组和切片)
  - [字典](#字典)

- **第三章**

  - [Interfaces](#interfaces)
  - [Errors](#errors)
  - [Panic and Recover](#panic-and-recover)
  - [Testing](#testing)
  - [Generics](#generics)

- **第四章**

  - [Concurrency](#concurrency)
  - [Goroutines](#goroutines)
  - [Channels](#channels)
  - [Select](#select)
  - [Sync Package](#sync-package)
  - [Advanced Concurrency Patterns](#advanced-concurrency-patterns)
  - [Context](#context)

- **附录**

  - [Next Steps](#next-steps)
  - [References](#references)

# 什么是Go?

Go (也常称为 _Golang_，注：Golang其实是因为当初go这个域名被抢注使用golang作为域名，所以其实它不是一个正确的称呼，现在还用了go.dev)是由Google于2007年开发并且在2009年开源的一门编程语言。

专注于设计一个简单，可读以及高效。组合了高效，快速及安全的一门静态编译型语言，同时具备动态语言的简单特性，使得编程更有趣了。

也就是说，它们想组合Python和C++最好的部分，以便构建一个可靠、高效利用多核处理器的系统。

# 为什么学习Go?

在开始该课程前，我们聊聊为什么要学习Go。

## 1. 容易学

Go非常简单学习，并且有一个非常活跃的社区支持。

作为一个多范式编程语言，你可以使用它来构建类似后端服务，云计算，甚至是最近流行的数据科学。

## 2. 快速及可靠

非常适合构建分布式系统。流行的Kubernetes和Docker也都是Go实现的。

## 3. 简单但强大

Go仅包含25个关键字，容易阅读，编写及维护。语言自身也想当简洁。

但其实Go又不简单，后面我会学习Go几个强大的特性。

## 4. 就业机会大

Go发展迅猛，被越来越多的公司采用，同时诞生了许多高收入工作机会。

希望这能让你对Go产生浓厚的兴趣，让我们来开始课程。

# 安装和配置

本教程我们开始安装Go以及配置代码编辑器。

## 下载

我们可以从[下载](https://go.dev/dl)区域安装Go。

![下载](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/getting-started/installation-and-setup/download.png)

## 安装

_以下指令摘至[官网](https://go.dev/doc/install)_

### MacOS

1. 打开下载的安装包，根据对话框来进行Go安装。
   安装包将Go分发在`/usr/local/go`. 安装包还将`/usr/local/go/bin` 目录放置在 `PATH` 环境变量。
   你可能需要重新打开终端会话使其生效。

2. 通过打开命令提示符敲入如下指令来确保Go成功安装：

```
$ go version
```

3. 确认正确输出了Go安装的版本号。

### Linux

1. 移除之前已安装Go目录`/usr/local/go`(如果存在)，
   然后将归档文件解压到目录`/usr/local`, 创建一个全新的Go目录 `/usr/local/go`:

```
$ rm -rf /usr/local/go && tar -C /usr/local -xzf go1.19.1.linux-amd64.tar.gz
```

_(你可以需要使用root用户来执行，或者使用sudo)_

**不要untar** 归档目录至已经存在的`/usr/local/go` 目录下. 这样会导致安装失败。

1. 添加 `/usr/local/go/bin` 到**PATH**环境变量.
   可以通过添加如下行到 `$HOME/.profile` 或者 `/etc/profile` (对系统全局安装):

```
export PATH=$PATH:/usr/local/go/bin
```

_注意: 以上改变如果在未重启系统情况下可能不会立即生效。要立即生效，只需在shell命令行下执行 source `$HOME/.profile`._

1. 通过打开命令对话框敲入如下命令来确保Go安装成功：

```
$ go version
```

4. 确认命令正确输出了Go安装的版本号。

### Windows

1. 打开下载的MSI文件，根据提示框来安装Go。

默认，安装器会将Go安装至Program Files 或 Program Files (x86)目录。
你可以根据需要进行修改。安装完后，你需要关闭并重新打开命令对话框以便安装器对环境变量的变更生效。

2. 确保Go正确安装.
   1. 系统中单机开始菜单。
   2. 在菜单搜索框输入cmd，按回车。
   3. 在命令对话框中输入如下命令：

```
$ go version
```

3. 确认命令正确输出了Go安装的版本号。

## VS Code

本教程，我将使用[VS Code](https://code.visualstudio.com) 你可以从[这里](https://code.visualstudio.com/download)下载。

![vscode](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/getting-started/installation-and-setup/vscode.png)

_你可以选用你青睐的其它代码编辑器。_

### 扩展

确保VS Code安装了 [Go 扩张](https://code.visualstudio.com/docs/languages/go)以便我们更佳的开发体验。

![extension](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/getting-started/installation-and-setup/extension.png)

这就是我们Go安装和配置内容，让我们开始编写我们第一个hello world！

# 你好世界

让我们编写第一个你好世界程序，我们从初始化一个module开始,使用`go mod`命令来操作。

```bash
$ mkdir example
$ go mod init example
```

等等...`module`是什么鬼？别急，后面我们再讨论！我们先暂定module就是Go包的一个

继续，让我们来创建一个`main.go`文件，编写一个简单输出世界你好的程序。

```go
package main

import "fmt"

func main() {
	fmt.Println("你好世界！")
}
```

_`fmt`是Go标准库_

## Go程序结构

现在，让我们快速分解这里的代码，熟悉一下Go程序结构。

首先，我们定义了`main`包名。

```go
package main
```

然后，我们导入包。

```go
import "fmt"
```

最后类似其它编程语言C, Java或者C#一样定义了`main`入口函数。

```go
func main() {
	...
}
```

这里先记个大概，后面课程我们会学习`functions`，`imports`和其它详情。

最后，我们通过使用`go run`命令来执行代码。

```bash
$ go run main.go
你好世界！
```

恭喜，你完成第一个Go程序的编写！

# 变量和数据类型

本章，我们将学习变量。我还会学习Go提供给我们的不同数据类型。

## 变量

让我们从定义一个变量开始。

以下定义了一个未初始化变量：

```go
var foo string
```

定义并且初始化：

```go
var foo string = "Go is awesome"
```

多个定义：

```go
var foo, bar string = "Hello", "World"
// 或者
var (
	foo string = "Hello"
	bar string  = "World"
)
```

虽然类型省略了，但是能被自动推断：

```go
var foo = "What's my type?"
```

短声明方式，这里忽略`var`关键字，类型是隐式申明。大部分我们会用这种方式来申明变量。
我们同时使用`:=`来声明和赋值变量。

```go
foo := "Shorthand!"
```

_注意: 短声明仅在 `函数` 体使用._

## 常量

我还可以使用`const`关键字来定义常量，正如其名，它值是固定不能更改。

```go
const constant = "This is a constant"
```

还有一个重要点是，只有常量可以赋值给其它常量。

```go
const a = 10
const b = a // ✅ 有效

var a = 10
const b = a // ❌ a (variable of type int) is not constant (InvalidConstInit)
```

## 数据类型

非常好！让我们看看Go里的一些基本数据类型。我们从字符串开始。

### 字符串

在Go，字符串是字节序列。它们使用双引号定义或者反引号来定义多行字符串。

```go
var name string = "My name is Go"

var bio string = `I am statically typed.
									I was designed at Google.`
```

### 布尔

接下来是用来定义布尔值的`bool`。他只有两种值 `true` or `false`。

```go
var value bool = false
var isItTrue bool = true
```

**操作符**

布尔类型还可以使用如下操作符

| Type     | Syntax    |
| -------- | --------- |
| Logical  | `&&` `!`  |
| Equality | `==` `!=` |

### 数值类型

现在，我们谈谈数值类型, 先从

**有符号和无符号整型**

Go内建几个不同大小的数值类型，用于存储有符号和无符号整型

通用的`int`和`uint`类型大小是平台依赖的，在32位系统位32位宽度，在64位系统即64位宽度


```go
var i int = 404                     // 平台依赖
var i8 int8 = 127                   // -128 to 127
var i16 int16 = 32767               // -2^15 to 2^15 - 1
var i32 int32 = -2147483647         // -2^31 to 2^31 - 1
var i64 int64 = 9223372036854775807 // -2^63 to 2^63 - 1
```

类似有符号整型，我们还有无符号整型。

```go
var ui uint = 404                     // 平台依赖
var ui8 uint8 = 255                   // 0 to 255
var ui16 uint16 = 65535               // 0 to 2^16
var ui32 uint32 = 2147483647          // 0 to 2^32
var ui64 uint64 = 9223372036854775807 // 0 to 2^64
var uiptr uintptr                     // Integer representation of a memory address
```

如你所看到的，这里还存在无符号整型`uintptr`类型，它一个整型用来保存内存地址。并不推荐使用它，所以我们大可不必担心它。

**该用哪个?**

推荐在使用整型时选用`int`，除非我们需要特性大小或者无符号的整型。

**整型别名**

接下来，我们来看看整型的别名。

**Byte and Rune**

Go有两个附加的整型称作`byte`和`rune`，它们分别使用`uint8`和`int32`作为原生类型。

```go
type byte = uint8
type rune = int32
```

_一个 `rune` 表示一个unicode码点。._

```go
var b byte = 'a'
var r rune = '🍕'
```

**浮点类型**

接下来，我们看看用来存储小数的浮点类型。

Go包含两种浮点类型`float32`和`float64`。两种类型遵从IEEE-754标准。

_默认浮点值使用的是float64_

```go
var f32 float32 = 1.7812 // IEEE-754 32位
var f64 float64 = 3.1415 // IEEE-754 64位
```

**操作符**

Go提供了一些对数值操作的操作符。

| Type                | Syntax                                                   |
| ------------------- | -------------------------------------------------------- |
| Arithmetic          | `+` `-` `*` `/` `%`                                      |
| Comparison          | `==` `!=` `<` `>` `<=` `>=`                              |
| Bitwise             | `&` `^` `<<` `>>`                                        |
| Increment/Decrement | `++` `--`                                                |
| Assignment          | `=` `+=` `-=` `*=` `/=` `%=` `<<=` `>>=` `&=` `\|=` `^=` |

**复数**

在Go有两种复数类型，`complex128`实部和虚部使用`float64`，`complex64`实部和虚部使用`float32`。

我们可以使用内建的complex函数或者使用字面值来定义复数。

```go
var c1 complex128 = complex(10, 1)
var c2 complex64 = 12 + 4i
```

## 零值

现在，我们来讨论一下零值。在Go，任何声明变量在没有显示声明其初始值时均会初始化为_零值_。例如，我们看定义如下变量：

```go
var i int
var f float64
var b bool
var s string

fmt.Printf("%v %v %v %q\n", i, f, b, s)
```

```bash
$ go run main.go
0 0 false ""
```

所以，正如我们所看到`int`和`float`为赋值为0，`bool`赋值为false，`string`被赋值为空字符串。这和其它编程语言有一些不一样。例如，但部分未显示赋值初始化的变量会被定义为null或者undefined。

很好，那`Printf`这些百分号是啥？正如你所猜到，它们是用来格式化用的，后面我们学习它们。

## 类型转换

继续，我们现在已经知道数据类型工作方式，那让我们看看如何做数据转换。

```go
i := 42
f := float64(i)
u := uint(f)

fmt.Printf("%T %T", f, u)
```

```bash
$ go run main.go
float64 uint
```

正如我们所看到的，这里打印了`float64`和`unit`。

_注意这里是一种不同的解析方式_

## 类型别名

类型别名首次在Go 1.9出现。它允许开发者提供一个现存类型其它名字。并且可以和底层类型交互使用。

```go
package main

import "fmt"

type MyAlias = string

func main() {
	var str MyAlias = "I am an alias"

	fmt.Printf("%T - %s", str, str) // 输出: string - I am an alias
}
```

## 自定类型

最后，还可以自定义类型，它不能像类型别名一样与原始类型相等性比较。

```go
package main

import "fmt"

type MyDefined string

func main() {
	var str MyDefined = "I am defined"

	fmt.Printf("%T - %s", str, str) // Output: main.MyDefined - I am defined
}
```

**有啥区别**

自定义类型比仅仅是给原始类型定义一个别名，它还完全是一个全新的类型。不能与原始类型互换使用。

这个可能会让你有点迷糊，我们来看看例子来更清晰一点。

```go
package main

import "fmt"

type MyAlias = string

type MyDefined string

func main() {
	var alias MyAlias
	var def MyDefined

	// ✅ 有效
	var copy1 string = alias

	// ❌ Cannot use def (variable of type MyDefined) as string value in variable
	var copy2 string = def

	fmt.Println(copy1, copy2)
}
```

正如我们所看到的，我们不能像类型别名那样用自定义类型来与原始类型互换使用。

# 字符串格式化

本教程中，我们将学习关于字符串格式化，有时也称之为模板化。

`fmt`包含许多函数。为节省篇幅，我们仅讨论常用的一些函数。我们先从`fmt.Print`开始。

```go
...

fmt.Print("What", "is", "your", "name?")
fmt.Print("My", "name", "is", "golang")
...
```

```bash
$ go run main.go
Whatisyourname?Mynameisgolang
```

如你所见，`Print`做任何格式操作，它仅简单接收字符串参数然后打印它。

接下来，还有一个类似`Print`的`Println`函数，但是它会在末尾增加换行符，并且在参数字符串之间增加空格。

```go
...

fmt.Println("What", "is", "your", "name?")
fmt.Println("My", "name", "is", "golang")
...
```

```bash
$ go run main.go
What is your name?
My name is golang
```

是不是好看多了！

接下来，有一个`Printf`，也叫做 _"Print Formatter"_ ，允许我们对数值，字符串，布尔等数据进行格式化。

我们来看看例子。

```go
...
name := "golang"

fmt.Println("What is your name?")
fmt.Printf("My name is %s", name)
...
```

```bash
$ go run main.go
What is your name?
My name is golang
```

这里`%s`被`name`变量值替换了。

这里`%s`是什么意思呢？

这些称为 _占位符_，它用来告诉函数如何格式化参数。我们控制宽度，类型和精度等等。可以参考[手册](https://pkg.go.dev/fmt)。

现在，让我们马不停蹄的了解更多例子。这里我们试着计算一个百分比然后将它打印到终端。

```go
...
percent := (3/5) * 100
fmt.Printf("%f", percent)
...
```

```bash
$ go run main.go
58.181818
```

如果我们指向打印出`58.18`仅包含两个精度的小数，我们可以使用`.2f`格式化占位符。

同时还想增加一个百分号，这里百分号需要 _转义_ 。

```go
...
percent := (3/5) * 100
fmt.Printf("%.2f %%", percent)
...
```

```bash
$ go run main.go
58.18 %
```

我们看一组对应的`Sprint`, `Sprintln`, 和 `Sprintf`。这些工作机制和之前print的函数一样，唯一的区别是它仅返回格式化字符串而不是打印它们。

让我们来看个例子。

```go
...
s := fmt.Sprintf("hex:%x bin:%b", 10 ,10)
fmt.Println(s)
...
```

```bash
$ go run main.go
hex:a bin:1010
```

这里`Sprintf`格式化我们的整型为16进制和2进制表示形式并返回为字符串数据格式。


最后我们看看多行字符串字面量。

```go
...
msg := `
Hello from
multiline
`

fmt.Println(msg)
...
```


真棒！但这只是冰山一角。请你查看go doc里的`fmt`包来了解更多信息。

如果你是具备C/C++背景的话，使用起来会感觉很自然，但是如果接触的是其它语言的话，如Python或者JavaScript，用法可能会有一些区别。但是它非常强大，你将看到它被广泛使用。


# 流程控制

让我们聊聊流程控制，从if/else开始。

## If/Else

它工作方式与你之前接触的其它编程语言基本一致，就是表达式不再使用`()`括号包起来。

```go
func main() {
	x := 10

	if x > 5 {
		fmt.Println("x is gt 5")
	} else if x > 10 {
		fmt.Println("x is gt 10")
	} else {
		fmt.Println("else case")
	}
}
```

```bash
$ go run main.go
x is gt 5
```

### 紧凑型 if

我们还可以使用紧凑型if语句。

```go
func main() {
	if x := 10; x > 5 {
		fmt.Println("x is gt 5")
	}
}
```

_注意：该模式很常用_

## Switch

接下来，我们学习`switch`语句，它使得条件逻辑变得短小。

在Go中，switch仅运行匹配case子句表达式，它不需要手动添加`break`语句到每个case子句中。

也就是说它从上到下执行，当匹配case子句后将停止执行其它case子句。

让我们看看例子：

```go
func main() {
	day := "monday"

	switch day {
	case "monday":
		fmt.Println("time to work!")
	case "friday":
		fmt.Println("let's party")
	default:
		fmt.Println("browse memes")
	}
}
```

```bash
$ go run main.go
time to work!
```

switch同样也支持短声明方式：

```go
	switch day := "monday"; day {
	case "monday":
		fmt.Println("time to work!")
	case "friday":
		fmt.Println("let's party")
	default:
		fmt.Println("browse memes")
	}
```

我们可以通过显示使用`fallthrough`关键字让go继续执行后面的case子句（无论条件是否匹配）。

```go
	switch day := "monday"; day {
	case "monday":
		fmt.Println("time to work!")
		fallthrough
	case "friday":
		fmt.Println("let's party")
	default:
		fmt.Println("browse memes")
	}
```


执行该代码，我们看到当第一个case子句匹配后，switch语句遇到`fallthrough`关键字后继续执行了后面的case子句。

```bash
$ go run main.go
time to work!
let's party
```

我们还可以在switch中不带任何表达式，相当于`switch true`。

```go
x := 10

switch {
	case x > 5:
		fmt.Println("x is greater")
	default:
		fmt.Println("x is not greater")
}
```

## 循环

现在，让我们将注意转移到循环。

在Go中，我们只有一个循环类型语句即`for`。

但是它用途非常广泛。和if语句一样，我们不需要像其它语句一样使用括号`()`包起来。

### For 循环

我们从基础`for`循环开始。

```go
func main() {
	for i := 0; i < 10; i++ {
		fmt.Println(i)
	}
}
```

基础`for`循环使用冒号分隔了三部分：

- **_初始语句_**: 在首次循环执行前执行。
- **_条件表达式_**: 在每次循环都会进行判断。
- **_后置语句_**: 每次循环结束后执行。

**Break 和 continue**

正如预期，Go在for语句中也支持`break`和`continue`控制语句。让我们来看个例子：

```go
func main() {
	for i := 0; i < 10; i++ {
		if i < 2 {
			continue
		}

		fmt.Println(i)

		if i > 5 {
			break
		}
	}

	fmt.Println("We broke out!")
}
```

所以，`continue`用来跳过本次循环语句，`break`用来结束循环语句。

同样，初始语句和后置语句是可选的，这样`for`可以表现为while同样的形式。

```go
func main() {
	i := 0

	for ;i < 10; {
		i += 1
	}
}
```

_注意：我们还可以移除多余的分号使其更简洁。_

### 无线循环

最后，如果我们条件表达式部分的话，它就成为了一个无限循环语句了。
```go
func main() {
	for {
		// do stuff here
	}
}
```

# 函数

本章，我们讨论Go中使用函数，先看看如何定义一个简单的函数。

## 定义函数

```go
func myFunction() {}
```

我们如下 _执行_：

```go
...
myFunction()
...
```

我们来传递一参数

```go
func main() {
	myFunction("Hello")
}

func myFunction(p1 string) {
	fmt.Println(p1)
}
```

```bash
$ go run main.go
```

我们看出打印出了输入参数。如果多个参数数据类型一致的话还可以使用短申明方式：

```go
func myNextFunction(p1, p2 string) {}
```

## 返回值

现在让我们来返回一个值。

```go
func main() {
	s := myFunction("Hello")
	fmt.Println(s)
}

func myFunction(p1 string) string {
	msg := fmt.Sprintf("%s function", p1)
	return msg
}
```

### 多返回值

Go语言支持多返回值！

```go
func main() {
	s, i := myFunction("Hello")
	fmt.Println(s, i)
}

func myFunction(p1 string) (string, int) {
	msg := fmt.Sprintf("%s function", p1)
	return msg, 10
}
```

### 具名返回值

另一个特性是[具名返回值](https://go.dev/tour/basics/7)，返回值可以在申明时指定其具体的名字，这样类似是函数体当中变量一样。

```go
func myFunction(p1 string) (s string, i int) {
	s = fmt.Sprintf("%s function", p1)
	i = 10

	return
}
```

注意我们使用`return`语句时并没有带任何值，这也称为 _裸返回_。

虽然这个特性很有趣，但是请谨慎使用，因为这在大型函数减少可读性。

## 函数作为值

接下来，让我们谈谈函数作为值，Go函数作为一等公民（first class），我们可以将它们作为值来使用。我们来试试！

```go
func myFunction() {
	fn := func() {
		fmt.Println("inside fn")
	}

	fn()
}
```

这里的`fn`我们还可以使用 _匿名函数_ 的方式处理。

```go
func myFunction() {
	func() {
		fmt.Println("inside fn")
	}()
}
```

*注意我们我们通过再末尾使用括号来执行它*

## 闭包

我们继续来在返回函数中使用闭包。简单来讲就是函数体内引用外部变量。

闭包是此法作用域的，也就是说函数内可以访问定义时作用域值。


```go
func myFunction() func(int) int {
	sum := 0

	return func(v int) int {
		sum += v

		return sum
	}
}
```

```go
...
add := myFunction()

add(5)
fmt.Println(add(10))
...
```

这里我们将得到15结果，因为`sum`变量 _绑定_ 到函数中。我们应该掌握这个强大特性。

## 可变参数

现在让我们来看看函数可变参数，也即函数通过使用`...`操作符来可以接收零个或者多个参数。

以下是一个可接收多个参数的函数例子。

```go
func main() {
	sum := add(1, 2, 3, 5)
	fmt.Println(sum)
}

func add(values ...int) int {
	sum := 0

	for _, v := range values {
		sum += v
	}

	return sum
}
```

很酷对吧？别担心`range`关键字，后面课程我们会再讨论。

_**事实上**: `fmt.Println` 就是个可变参数函数，所以我们才可以传递多个值_

## Init

在Go中，`init`是一个特别的生命周期函数，它执行于`main`函数之前。

类似`main`函数，`init`函数不接收任何参数也不返回任何值。我们来看看例子：

```go
package main

import "fmt"

func init() {
	fmt.Println("Before main!")
}

func main() {
	fmt.Println("Running main")
}
```

正如预期，`init`函数执行于`main`函数之前。

```bash
$ go run main.go
Before main!
Running main
```

不像`main`函数，可以在单个或者多个文件定义任意多个`init`函数。

在单个文件中定义多个`init`函数，执行顺序为定义顺序，当`init`函数定义在多个文件时，它的执行顺序依赖名字排序。

```go
package main

import "fmt"

func init() {
	fmt.Println("Before main!")
}

func init() {
	fmt.Println("Hello again?")
}

func main() {
	fmt.Println("Running main")
}
```

如果我们执行该代码，我们将会看到`init`函数会根据定义的顺序执行。

```bash
$ go run main.go
Before main!
Hello again?
Running main
```

`init`函数是可选的，经常用来作为全局基础设置，例如数据库连接，获取配置文件，配置环境等。

## Defer

最后，我们来讨论`defer`关键字，它允许在函数结束后延迟执行代码。
```go
func main() {
	defer fmt.Println("I am finished")
	fmt.Println("Doing some work...")
}
```

我们是否可以拥有多个defer函数？当然，它会将多个函数置入 _defer栈_，例如：

```go
func main() {
	defer fmt.Println("I am finished")
	defer fmt.Println("Are you?")

	fmt.Println("Doing some work...")
}
```

```bash
$ go run main.go
Doing some work...
Are you?
I am finished
```

正如上面所见，defer语句是一个栈结构，以 _后进先出_ 的形式来执行。

所以，Defer非常有用，常用来做清理或者错误处理的工作。

函数还支持泛型，不过我们后面再讨论。

# 模块

本章，我们来学习模块。

## 什么是模块？

简单来说，一个模块就是在`$GOPATH/src`目录外，定义一个目录包含`go.mod`文件且包含[Go 包](https://go.dev/ref/spec#Packages)集合。

Go模块首次出现在 Go.11，带来了原生支持版本和模块。早期，我们需要配置`GO111MODULE=on`来打开试验性模块特性。不过在Go 1.13开始默认打开。

但是什么是`GOPATH`？

`GOPATH`是一个变量，用来定义根工作目录，它包含：

- **src**: 包含结构化的Go源码
- **pkg**: 包含编译的包代码
- **bin**: 包含编译的二进制可执行文件

![gopath](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-I/modules/gopath.png)


早期，我们就通过使用`go mod init`命令来创建模块，通过使用`go.mod`文件来配置。

```bash
$ go mod init example
```

_这里要提醒的是如果你打算将模块发布到Github中，你可以使用对应Github仓库地址。例如:_

```bash
$ go mod init github.com/golang/example
```

现在我们来看看`go.mod`，该文件模块路径和依赖关系。

```go
module <name>

go <version>

require (
	...
)
```

如果我们需要添加依赖，可以使用`go install`命令：

```bash
$ go install github.com/rs/zerolog
```

你还会在根目录下看到`go.sum`文件被创建。该文件包含已使用依赖模块的[哈希值](https://go.dev/cmd/go/#hdr-Module_downloading_and_verification)。

我可以使用`go list`命令列出所有的依赖：

```bash
$ go list -m all
```

如果依赖没被使用，我们还可以简单使用`go mod tidy`进行清理：

```bash
$ go mod tidy
```

结束模块的讨论，让我们来聊聊vendoring。

Vendoring是用来对项目使用的第三方包的完整拷贝。它会伴随项目一起进行贮存。

通过使用`go mod vendor`命令来实现。

我们就可以使用`go mod tidy`来重新安装模块了。

```go
package main

import "github.com/rs/zerolog/log"

func main() {
	log.Info().Msg("Hello")
}
```

```bash
$ go mod tidy
go: finding module for package github.com/rs/zerolog/log
go: found github.com/rs/zerolog/log in github.com/rs/zerolog v1.26.1
```

```bash
$ go mod vendor
```

```
├── go.mod
├── go.sum
├── go.work
├── main.go
└── vendor
    ├── github.com
    │   └── rs
    │       └── zerolog
    │           └── ...
    └── modules.txt
```

# 包

本章，我们聊聊包。

## 什么是包？

一个包仅就是一个目录来存放一个或者多个Go源文件，或者是其它包。

也就是说每个Go源代码文件都必须属于一个包，包定义在源文件开头处：

```go
package <package_name>
```

目前，我们已经在`package main`里完成基础工作。按照约定，可执行程序称为 _Commands_，其它称为 _Packages_。

`main`包应该包含一个`main()`函数，作为可执行程序入口。

让我们通过创建一个`custom`包，存放在`code.go`文件中。

```go
package custom
```

在继续前，我们来聊聊导入和导出。和其它语言一样，go同样有导入导出，不过它更佳优雅。

基本上，任何使用大写字母开头标识的值（例如变量和函数）都可以导出给其它包使用。

例如`custom`包

```go
package custom

var value int = 10 // 不被导出
var Value int = 20 // 被导出
```

小写字母标识的变量将没有被导出，属于`custom`包的私有变量。

那好，我们如何导入与访问呢？让我们在`main.go`文件中导入`custom`包。

我们可以使用我已经之前通过`go.mod`初始化的`模块`。


```go
---go.mod---
module example

go 1.18

---main.go--
package main

import "example/custom"

func main() {
	custom.Value
}
```

_注意包名为导入路径的最后部分。_

我们可以如下方式导入多个包：

```go
package main

import (
	"fmt"

	"example/custom"
)

func main() {
	fmt.Println(custom.Value)
}
```

我们还可以对于相同包名时使用别名来避免冲突：

```go
package main

import (
	"fmt"

	abcd "example/custom"
)

func main() {
	fmt.Println(abcd.Value)
}
```

## 外部依赖

Go不限于使用本地包，可以使用`go install`使用外部包，例如下载一个简单的日志包`github.com/rs/zerolog/log`.

```bash
$ go install github.com/rs/zerolog
```

```go
package main

import (
	"github.com/rs/zerolog/log"

	abcd "example/custom"
)

func main() {
	log.Print(abcd.Value)
}
```

_同时，确保使用go doc查看安装包的说明文档_

最后，我要指出的是Go没有强制 _"目录结构"_ 约束，请尽量按照简单易于理解的方式来组织你的包。

# 工作区

本章，我们学习首次在Go 1.18出现的多模块工作区。

工作区允许我们无需修改`go.mod`文件同时拥有多个模块。工作区各个模块各自以根模块方式来解决依赖。

为更好理解，我们创建一个`hello`模块：

```bash
$ mkdir workspaces && cd workspaces
$ mkdir hello && cd hello
$ go mod init hello
```

为演示目的，我们简单实现`main.go`，并安装示例包。

```go
package main

import (
	"fmt"

	"golang.org/x/example/stringutil"
)

func main() {
	result := stringutil.Reverse("Hello Workspace")
	fmt.Println(result)
}
```

```bash
$ go install golang.org/x/example
go: downloading golang.org/x/example v0.0.0-20220412213650-2e68773dfca0
go: added golang.org/x/example v0.0.0-20220412213650-2e68773dfca0
```

运行后，我们可以看到反转的字符串。

```bash
$ go run main.go
ecapskroW olleH
```

这也没什么，但是如果我们想要修改所依赖的`stringutil`模块呢？

之前，我们需要使用在`go.mod`文件使用`replace`指令来实现，但是现在我们可以使用工作区来实现。

让我们在`workspaces`目录来创建工作区。

```bash
$ go work init
```

该命令会创建 `go.work` 文件。

```bash
$ cat go.work
go 1.18
```

我们将添加`hello`模块到工作区。

```bash
$ go work use ./hello
```

它将更新`go.work`文件引用我们的`hello`模块。

```go
go 1.18

use ./hello
```

现在让我们下载`stringutil`，修改`Reverse`函数的实现。

```bash
$ git clone https://go.googlesource.com/example
Cloning into 'example'...
remote: Total 204 (delta 39), reused 204 (delta 39)
Receiving objects: 100% (204/204), 467.53 KiB | 363.00 KiB/s, done.
Resolving deltas: 100% (39/39), done.
```

`example/stringutil/reverse.go`

```go
func Reverse(s string) string {
	return fmt.Sprintf("I can do whatever!! %s", s)
}
```

最后，我们添加`example`包到工作区。

```bash
$ go work use ./example
$ cat go.work
go 1.18

use (
	./example
	./hello
)
```

完美，现在让我们执行`hello`模块，注意`Revese`函数的变更。

```bash
$ go run hello
I can do whatever!! Hello Workspace
```

_这时1.18被低估的特性，但是在某些场景下非常有用._

# 实用命令

在讲解模块时，我们谈及了模块相关的go命令，让我们继续讨论其它重要的命令。

我们从`go fmt`开始，用来格式化代码，强制规则让我们不用去过多烦恼代码格式。

```bash
$ go fmt
```

如果你是来自JavaScript或者Python背景的话可能会觉得很奇怪，不过不用去担心代码格式相当的好。

接下来，还有`go vet`用来检测包中错误。

```bash
$ go vet
```

还有`go env`打印所有的go环境信息，我们后面还会学习这些构建参数信息。

最后，`go doc`用来查看包里的文档，这是查看`fmt`包文档示例：

```bash
$ go doc -src fmt Printf
```

让我们使用`go help`命令来查看其它可用命令。
```bash
$ go help
```

列出的有:

`go fix` 找出一些过时的API并且重新为新式API

`go generate` 用来生成代码

`go install` 编译安装包和依赖

`go clean` 清理编译器生成的文件

一些其它的命令如`go build`和`go test`我们将会在后面课程学习到。

# 编译

Go提供一种极佳特性，使用二进制静态编译高效代码传递代码。

我们可以使用`go build`命令来实现编译。

```go
package main

import "fmt"

func main() {
	fmt.Println("I am a binary!")
}
```

```bash
$ go build
```

这将生成模块的二进制文件。例如，这里是`example`。

我们还可以指定输出的名字：

```bash
$ go build -o app
```

我们现在来执行它。

```bash
$ ./app
I am a binary!
```

_太简单了_


现在我们来聊聊一些编译时参数：

- `GOOS` 和 `GOARCH`

这些环境变量用来帮助我们构建不同[操作系统](https://en.wikipedia.org/wiki/Operating_system)
和[CPU架构](https://en.wikipedia.org/wiki/Microarchitecture)。

我们可以使用`go tool`命令来列出支持的CPU架构。

```bash
$ go tool dist list
android/amd64
ios/amd64
js/wasm
linux/amd64
windows/arm64
.
.
.
```

这里是从macOS编译Wwndows可执行文件的例子：

```bash
$ GOOS=windows GOARCH=amd64 go build -o app.exe
```

- `CGO_ENABLED`

该变量允许配置[CGO](https://go.dev/blog/cgo), Go用来执行C代码。

它帮助我们生成 [静态链接](https://en.wikipedia.org/wiki/Static_build) 二进制程序而不需要外部依赖。

它非常有用，比如我们像将我们go二进制程序使用最小化外部依赖方式执行。

我们这样使用：

```bash
$ CGO_ENABLED=0 go build -o app
```

# 指针

本章，我们来讨论指针。那么什么是指针？

简单来说，指针旧是用一个变量来存储另一个变量的内存地址。

![指针](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-II/pointers/pointers.png)

它可以这样使用：

```go
var x *T
```

`T`是类似`int`，`string`，`float`等类型。

我们来看看实际的例子：

```go
package main

import "fmt"

func main() {
	var p *int

	fmt.Println(p)
}
```

```bash
$ go run main.go
nil
```

这里打印出了`nil`，`nil`又是什么？

nil是一个预定义的标识符，用来表示指针，接口，通道，map和切片的零值。

就类似我们在变量和数据类型章节所提及，未初始化`int`零值为0,`bool`为false等。

好，现在我们来为指针赋值。

```go
package main

import "fmt"

func main() {
	a := 10

	var p *int = &a

	fmt.Println("address:", p)
}
```

我们使用`&`符号来引用变量的内存地址。

```bash
$ go run main.go
0xc0000b8000
```

这里即`a`变量的内存地址。

## 解引用

我还可以使用`*`符号来指针所指向存储的值。称为**解引用**。

例如，我们通过对`p`指针使用`*`操作符来取得`a`的变量的值。


```go
package main

import "fmt"

func main() {
	a := 10

	var p *int = &a

	fmt.Println("address:", p)
	fmt.Println("value:", *p)
}
```

```bash
$ go run main.go
address: 0xc000018030
value: 10
```

我们不但能通过指针访问，还可以修改。

```go
package main

import "fmt"

func main() {
	a := 10

	var p *int = &a

	fmt.Println("before", a)
	fmt.Println("address:", p)

	*p = 20
	fmt.Println("after:", a)
}
```

```bash
$ go run main.go
before 10
address: 0xc000192000
after: 20
```

我认为还是想当简洁的！

## 使用指针作为参数

指针可以用来实现引用传递函数参数。

下面是例子：

```go
myFunction(&a)
...

func myFunction(ptr *int) {}
```

## new函数

还有另外一种初始化指针的方式，使用`new`函数，并传递类型作为参数。它分配对应容纳该类型指针并返回。

看看例子：

```go
package main

import "fmt"

func main() {
	p := new(int)
	*p = 100

	fmt.Println("value", *p)
	fmt.Println("address", p)
}
```

```bash
$ go run main.go
value 100
address 0xc000018030
```

## 指针的指针

有个奇思妙想就是指针能否指向指针？答案是：可以。

```go
package main

import "fmt"

func main() {
	p := new(int)
	*p = 100

	p1 := &p

	fmt.Println("P value", *p, " address", p)
	fmt.Println("P1 value", *p1, " address", p)

	fmt.Println("Dereferenced value", **p1)
}
```

```bash
$ go run main.go
P value 100  address 0xc0000be000
P1 value 0xc0000be000  address 0xc0000be000
Dereferenced value 100
```

_注意`p1`存储为`p`的地址._

Go不支持同C/C++的指针运算。

```go
	p1 := p * 2 // Compiler Error: invalid operation
```

但是，我们可以使用`==`来匹配两个指针是否相等。

```go
p := &a
p1 := &a

fmt.Println(p == p1)
```

## 为什么

为什么需要指针？

没有绝对的答案，指针给我们一个有用特性是可以不需要通过拷贝数据的方式来高效传递数据。

而且被大量使用。

最后，如果你其它语言转过来没有接触过指针概念，先不着急，先尝试构建一个指针工作的心智模型。

# 结构

本章，我们来学习结构。

`struct`是通过包含一系列命名字段的自定义类型。通常用来将一组相关数据组合在一个单元里。

如果你具备面向对象背景，将结构想象成一个类，但是它仅支持组合，不支持继承。

## 定义

我们可以如下定义一个`struct`：

```go
type Person struct {}
```

我们使用`type`关键字来创建一个新类型，然后紧跟名字，接着是`struct`关键字用来指明为结构体。

现在，让我们增加一些字段：

```go
type Person struct {
	FirstName string
	LastName  string
	Age       int
}
```

同时，如果相同类型我们还可以联合申明。

```go
type Person struct {
	FirstName, LastName string
	Age                 int
}
```

## 声明和初始化


现在我们已经有结构了，我们可以类似其它数据类型方式来定义：

```go
func main() {
	var p1 Person

	fmt.Println("Person 1:", p1)
}
```

```bash
$ go run main.go
Person 1: {  0}
```

正如所见，所有的结构字段使用零值来初始化。所以`FirstName`和`LastName`设置为`""`空字符串且`Age`设置为0。

我们还可以使用 _"结构字面量"_ 来初始化。

```go
func main() {
	var p1 Person

	fmt.Println("Person 1:", p1)

	var p2 = Person{FirstName: "Karan", LastName: "Pratap Singh", Age: 22}

	fmt.Println("Person 2:", p2)
}
```

为提高可读性，我们通过换行隔开且最后也要声明逗号。x

```go
	var p2 = Person{
		FirstName: "Karan",
		LastName:  "Pratap Singh",
		Age:       22,
	}
```

```bash
$ go run main.go
Person 1: {  0}
Person 2: {Karan Pratap Singh 22}
```

还可以只指明部分字段初始化：

```go
func main() {
	var p1 Person

	fmt.Println("Person 1:", p1)

	var p2 = Person{
		FirstName: "Karan",
		LastName:  "Pratap Singh",
		Age:       22,
	}

	fmt.Println("Person 2:", p2)

	var p3 = Person{
		FirstName: "Tony",
		LastName:  "Stark",
	}

	fmt.Println("Person 3:", p3)
}
```

```bash
$ go run main.go
Person 1: {  0}
Person 2: {Karan Pratap Singh 22}
Person 3: {Tony Stark 0}
```

Person 3的Age字段同样使用了默认零值。

## 不带字段名

Go结构还支持不带字段名的初始化方式。

```go
func main() {
	var p1 Person

	fmt.Println("Person 1:", p1)

	var p2 = Person{
		FirstName: "Karan",
		LastName:  "Pratap Singh",
		Age:       22,
	}

	fmt.Println("Person 2:", p2)

	var p3 = Person{
		FirstName: "Tony",
		LastName:  "Stark",
	}

	fmt.Println("Person 3:", p3)

	var p4 = Person{"Bruce", "Wayne"}

	fmt.Println("Person 4:", p4)
}
```

不过要注意的是，这里需要初始化时提供所有的值否则会报错。

```bash
$ go run main.go
# command-line-arguments
./main.go:30:27: too few values in Person{...}
```

```go
	var p4 = Person{"Bruce", "Wayne", 40}

	fmt.Println("Person 4:", p4)
```

我们还可以定义一个匿名结构。

```go
func main() {
	var p1 Person

	fmt.Println("Person 1:", p1)

	var p2 = Person{
		FirstName: "Karan",
		LastName:  "Pratap Singh",
		Age:       22,
	}

	fmt.Println("Person 2:", p2)

	var p3 = Person{
		FirstName: "Tony",
		LastName:  "Stark",
	}

	fmt.Println("Person 3:", p3)

	var p4 = Person{"Bruce", "Wayne", 40}

	fmt.Println("Person 4:", p4)

	var a = struct {
		Name string
	}{"Golang"}

	fmt.Println("Anonymous:", a)
}
```

## 访问字段

让我们来看看如何访问单个字段。

```go
func main() {
	var p = Person{
		FirstName: "Karan",
		LastName:  "Pratap Singh",
		Age:       22,
	}

	fmt.Println("FirstName", p.FirstName)
}
```

我也创建一个指向结构的指针。

```go
func main() {
	var p = Person{
		FirstName: "Karan",
		LastName:  "Pratap Singh",
		Age:       22,
	}

	ptr := &p

	fmt.Println((*ptr).FirstName)
	fmt.Println(ptr.FirstName)
}
```

上面两个语句是相等，我们无需显示对指针进行解引用。我们也可以使用内建的`new`函数。

```go
func main() {
	p := new(Person)

	p.FirstName = "Karan"
	p.LastName = "Pratap Singh"
	p.Age = 22

	fmt.Println("Person", p)
}
```

```bash
$ go run main.go
Person &{Karan Pratap Singh 22}
```

当两个结构所有字段均相等，那么两个结构即相等。

```go
func main() {
	var p1 = Person{"a", "b", 20}
	var p2 = Person{"a", "b", 20}

	fmt.Println(p1 == p2)
}
```

```bash
$ go run main.go
true
```

## 导出字段

和变量函数一致，结构字段通过使用首字母标识是否导出。

```go
type Person struct {
	FirstName, LastName  string
	Age                  int
	zipCode              string
}
```

`zipCode`不会导出。`Person`结构也一样，如果我们改为`person`，它也不会被导出。

```go
type person struct {
	FirstName, LastName  string
	Age                  int
	zipCode              string
}
```

##嵌入和组合

之前我们提到，Go不支持继承，但是我们使用嵌入达到相同目的。

```go
type Person struct {
	FirstName, LastName  string
	Age                  int
}

type SuperHero struct {
	Person
	Alias string
}
```

新结构将包含原始结构所有属性。它的行为与原始结构一致。

```go
func main() {
	s := SuperHero{}

	s.FirstName = "Bruce"
	s.LastName = "Wayne"
	s.Age = 40
	s.Alias = "batman"

	fmt.Println(s)
}
```

```bash
$ go run main.go
{{Bruce Wayne 40} batman}
```

不过，大多情况下不建议这样使用。我们通常仅定义为一个普通字段而不是嵌入方式。

```go
type Person struct {
	FirstName, LastName  string
	Age                  int
}

type SuperHero struct {
	Person Person
	Alias  string
}
```

Hence, we can rewrite our example with composition as well.

```go
func main() {
	p := Person{"Bruce", "Wayne", 40}
	s := SuperHero{p, "batman"}

	fmt.Println(s)
}
```

```bash
$ go run main.go
{{Bruce Wayne 40} batman}
```

这里没有对错，有时用嵌入会带来便利。

## 结构标签

结构标签允许我们为字段添加元信息，可以方便使用`relect`包来自定义行为。

如下方式定义标签。

```go
type Animal struct {
	Name    string `key:"value1"`
	Age     int    `key:"value2"`
}
```

你将常在编码包中看见它们，例如XML, JSON, YAML, ORMS和配置管理。

以下是JSON编码器中的结构标签用例：

```go
type Animal struct {
	Name    string `json:"name"`
	Age     int    `json:"age"`
}
```

## 结构传递

最后，我们来讨论结构传递。

结构为值类型，当我赋值结构给另外一个变量时，将会生成一个全新的结构拷贝。

同样当然我们传递结构给函数时，函数同样会获得一个全新的拷贝。

```go
package main

import "fmt"

type Point struct {
	X, Y float64
}

func main() {
	p1 := Point{1, 2}
	p2 := p1 // Copy of p1 is assigned to p2

	p2.X = 2

	fmt.Println(p1) // Output: {1 2}
	fmt.Println(p2) // Output: {2 2}
}
```

空结构体占用0字节存储。

```go
package main

import (
	"fmt"
	"unsafe"
)

func main() {
	var s struct{}
	fmt.Println(unsafe.Sizeof(s)) // Output: 0
}
```

# 方法

让我们聊聊方法。有时也称为带有receiver的函数。

严格上来说，Go并不是一个面向对象编程语言。它没有类，对象和继承。

然而，Go有类型，而且你还可以给类型定义 **方法**。

方法相对函数来说，除了多一个 _receiver_ 参数外没有其它差别。让我们来看看如何定义方法。

```go
func (receiver) Name(params) (returnTypes) {}
```

_receiver_参数包含一个名字和类型。它们在出现在`func`关键字和方法名之间。

例如，让我们定义一个`Car`结构。

```go
type Car struct {
	Name string
	Year int
}
```

现在，我们定义个方法`IsLatest`用来返回该车是否生产与五年内。

```go
func (c Car) IsLatest() bool {
	return c.Year >= 2017
}
```

正如你所见，我们可以使用receiver变量`c`来访问`Car`实例。我习惯将它对应面向对象里的`this`关键字。

现在我们可以在初始化结构体后来访问该方法了，和其它语言中类访问方法类似：

```go
func main() {
	c := Car{"Tesla", 2021}

	fmt.Println("IsLatest", c.IsLatest())
}
```

## 使用指针receiver

上面所有例子我都使用值receiver。

使用值receiver时，传递的是值拷贝。因此，任何在方法内的修改并不会影响到调用方。

例如，我们创建一个`UpdateName`来尝试更新`Car`的名字。

```go
func (c Car) UpdateName(name string) {
	c.Name = name
}
```

现在，让我们来执行。

```go
func main() {
	c := Car{"Tesla", 2021}

	c.UpdateName("Toyota")
	fmt.Println("Car:", c)
}
```

```bash
$ go run main.go
Car: {Tesla 2021}
```

貌似名字并没有被修改，现在我们试着用指针receiver看看。

```go
func (c *Car) UpdateName(name string) {
	c.Name = name
}
```

```bash
$ go run main.go
Car: {Toyota 2021}
```

如预期，使用指针receiver将会修改原始调用方的值。

## 特性

让我们看一些方法特性！

- Go足够聪明使用正确的方式来调用方法，指针receiver只是Go提供方便的语法糖。

```go
(&c).UpdateName(...)
```

- 如果我们方法中没有使用receiver我们还可以忽略调用名字。

```go
func (Car) UpdateName(...) {}
```

- 方法不但可以定义在结构中，非结构类型也同样可以。

```go
package main

import "fmt"

type MyInt int

func (i MyInt) isGreater(value int) bool {
	return i > MyInt(value)
}

func main() {
	i := MyInt(10)

	fmt.Println(i.isGreater(5))
}
```

## 有函数为什么还要方法?

为什么使用方法来替代函数呢？

没有确切的答案一种方式比另一种好。它们在适合不同场景。

其中一个我能想到的是方法可以避免命名冲突。

因为方法绑定给了具体类型，所以对于多个receiver可以拥有相同名字。

当然还有是因为个人喜好，例如 _"方法调用比函数调用更容易阅读和理解"_。

# 数组和切片

本章，我们来学习Go里的数组和切片。


## 数组

### 什么是数组？

数组包含是包含相同类型固定大小的元素集合。它们使用顺序存储可以用`下标`访问。

![array](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-II/arrays-and-slices/array.png)

### 申明

我可以如下方式申明：

```go
var a [n]T
```

这里`n`是长度,`T`可以是任意类型，如整型，字符串或者自定义结构。

现在我们来申明一个长度为4的整型数组，然后打印它。

```go
func main() {
	var arr [4]int

	fmt.Println(arr)
}
```

```bash
$ go run main.go
[0 0 0 0]
```

默认，所有数组元素会初始化为相应元素的数组类型。

### 初始化

我们还可以使用数组字面量来初始化数组。


```go
var a [n]T = [n]T{V1, V2, ... Vn}
```

```go
func main() {
	var arr = [4]int{1, 2, 3, 4}

	fmt.Println(arr)
}
```

```bash
$ go run main.go
[1 2 3 4]
```

同样可以使用短申明方式。

```go
...
arr := [4]int{1, 2, 3, 4}
```

### 访问

和其它语言一样，我们可以使用根据存储顺序的`下标`来访问元素。

```go
func main() {
	arr := [4]int{1, 2, 3, 4}

	fmt.Println(arr[0])
}
```

```bash
$ go run main.go
1
```

### 遍历

现在，我们来谈谈遍历。

有多种遍历数组的方式。

第一种是使用`len`函数来获取到数组长度使用for循环遍历。

```go
func main() {
	arr := [4]int{1, 2, 3, 4}

	for i := 0; i < len(arr); i++ {
		fmt.Printf("Index: %d, Element: %d\n", i, arr[i])
	}
}
```

```bash
$ go run main.go
Index: 0, Element: 1
Index: 1, Element: 2
Index: 2, Element: 3
Index: 3, Element: 4
```

另一种是使用`range`关键字来使用`for`循环来遍历。

```go
func main() {
	arr := [4]int{1, 2, 3, 4}

	for i, e := range arr {
		fmt.Printf("Index: %d, Element: %d\n", i, e)
	}
}
```

```bash
$ go run main.go
Index: 0, Element: 1
Index: 1, Element: 2
Index: 2, Element: 3
Index: 3, Element: 4
```

正如我们所看到的，和之前的输出结果一致。

range是多用途的，可以用在很多场景。

```go
for i, e := range arr {} // 基本使用方式

for _, e := range arr {} // 使用 _ 忽略下标

for i := range arr {} // 只获取下标

for range arr {} // 仅循环数组不获取值和小标
```

### 多维数组

Go也可以创建多维数组。

我们看看例子。

```go
func main() {
	arr := [2][4]int{
		{1, 2, 3, 4},
		{5, 6, 7, 8},
	}

	for i, e := range arr {
		fmt.Printf("Index: %d, Element: %d\n", i, e)
	}
}
```

```bash
$ go run main.go
Index: 0, Element: [1 2 3 4]
Index: 1, Element: [5 6 7 8]
```

我们还是用`...`符号让编译器自动推断数组长度。

```go
func main() {
	arr := [...][4]int{
		{1, 2, 3, 4},
		{5, 6, 7, 8},
	}

	for i, e := range arr {
		fmt.Printf("Index: %d, Element: %d\n", i, e)
	}
}
```

```bash
$ go run main.go
Index: 0, Element: [1 2 3 4]
Index: 1, Element: [5 6 7 8]
```

### 特性

现在我们聊聊数组特性。

数组的长度是其类型的一部分，数组`a`和`b`是完全不同的类型，不能相互赋值。

也就是我们不能改变数组大小，因为改变大小也就意味着改变其类型了。

```go
package main

func main() {
	var a = [4]int{1, 2, 3, 4}
	var b [2]int = a // Error, cannot use a (type [4]int) as type [2]int in assignment
}
```

Go里的数组不像其它类似C,C++和Java那样是引用类型。

也就是说将数组赋给一个新变量或者传递给函数时，将会对数组完全拷贝。

所以，如果我们对拷贝的数组做任何修改，原数组不会受影响。

```go
package main

import "fmt"

func main() {
	var a = [7]string{"Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"}
	var b = a // Copy of a is assigned to b

	b[0] = "Monday"

	fmt.Println(a) // Output: [Mon Tue Wed Thu Fri Sat Sun]
	fmt.Println(b) // Output: [Monday Tue Wed Thu Fri Sat Sun]
}
```

## 切片

我知道不会想，数组非常有用，但是又受限于它的固定大小。

这样旧引入的切片，那么切片是什么？

切片是数组的片段，切片构建于数组之上，提供了更多功能，可扩展性和更佳方便。

![slice](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-II/arrays-and-slices/slice.png)

切片由以下三部分组成：

- 指针指向数组下标
- 切片包含数组的长度
- 可以容纳元素的最大容量


和`len`函数一样，我们也可以使用内建`cap`函数来获取切片容量，例如：

```go
package main

import "fmt"

func main() {
	a := [5]int{20, 15, 5, 30, 25}

	s := a[1:4]

	// 输出: Array: [20 15 5 30 25], Length: 5, Capacity: 5
	fmt.Printf("Array: %v, Length: %d, Capacity: %d\n", a, len(a), cap(a))

	// 输出: Slice [15 5 30], Length: 3, Capacity: 4
	fmt.Printf("Slice: %v, Length: %d, Capacity: %d", s, len(s), cap(s))
}
```

别担心，我们会详细讲解这里所有的东西。

### 申明

我们来看看如何申明切片。

```go
var s []T
```

我们不需要给切片提供长度，试试看字符串切片

```go
func main() {
	var s []string

	fmt.Println(s)
	fmt.Println(s == nil)
}
```

```bash
$ go run main.go
[]
true
```

不同于数组，切片的零值为`nil`。

### 初始化

也有多种初始化切片的方式。一种是使用内建的`make`函数。

```go
make([]T, len, cap) []T
```

```go
func main() {
	var s = make([]string, 0, 0)

	fmt.Println(s)
}
```

```bash
$ go run main.go
[]
```

和数组一样，也可以使用切片字面量来初始化切片。

```go
func main() {
	var s = []string{"Go", "TypeScript"}

	fmt.Println(s)
}
```

```bash
$ go run main.go
[Go TypeScript]
```

另一种方式是从数组创建切片。由于切片是数组的片段。我们可以使用`low(上标)`和`high(下标)`来创建数组。

```go
a[low:high]
```

```go
func main() {
	var a = [4]string{
		"C++",
		"Go",
		"Java",
		"TypeScript",
	}

	s1 := a[0:2] // 从0到2
	s2 := a[:3]  // 开头到第三个
	s3 := a[2:]  // 从第二个到最后

	fmt.Println("Array:", a)
	fmt.Println("Slice 1:", s1)
	fmt.Println("Slice 2:", s2)
	fmt.Println("Slice 3:", s3)
}
```

```bash
$ go run main.go
Array: [C++ Go Java TypeScript]
Slice 1: [C++ Go]
Slice 2: [C++ Go Java]
Slice 3: [Java TypeScript]
```

_不指定上标即从0开始，不指定下标即数组长度 (`len(a)`)._


除了可以从数组构建切片，同样也可以切片上构建切片。

```go
var a = []string{
	"C++",
	"Go",
	"Java",
	"TypeScript",
}
var b = a[:]
fmt.Println("Slice a: ", a)
fmt.Println("Slice b: ", b)
```

### 遍历

我们可以使用遍历数组相同的方式来遍历切片，使用结合`len`函数或者`range`关键字使用for循环遍历。

### 函数


我们来看看Go提供的切片函数。

**copy**

`copy()`函数从一切切片拷贝元素到另一个切片中，它接收两个切片参数，一个是目标切片，一个是圆切片。它会返回拷贝元素的长度。

```go
func copy(dst, src []T) int
```

我们看看如何使用它。

```go
func main() {
	s1 := []string{"a", "b", "c", "d"}
	s2 := make([]string, len(s1))

	e := copy(s2, s1)

	fmt.Println("Src:", s1)
	fmt.Println("Dst:", s2)
	fmt.Println("Elements:", e)
}
```

```bash
$ go run main.go
Src: [a b c d]
Dst: [a b c d]
Elements: 4
```

成功将源切片4个元素拷贝到目标切片。

**append**

`append`函数用来给切片追加元素。

它接收一个切片参数和要追加的元素。它返回包含其所有元素的新切片。

```go
append(slice []T, elems ...T) []T
```

让我们来尝试给切片追加元素。

```go
func main() {
	s1 := []string{"a", "b", "c", "d"}

	s2 := append(s1, "e", "f")

	fmt.Println("s1:", s1)
	fmt.Println("s2:", s2)
}
```

```bash
$ go run main.go
s1: [a b c d]
s2: [a b c d e f]
```

执行`append`后包含新元素的切片被返回。

如果切片不够容量来存放追加元素情况下，切片会申请一个更大容量的底层数组。

所有原数会拷贝至新数组，然后添加追加元素。

### 特性

最后我们来讨论切片的特性。

所有的切片均是引用类型，和数组不一样。

也就是改变切片数组其实是改变所引用的底层数组元素。

```go
package main

import "fmt"

func main() {
	a := [7]string{"Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"}

	s := a[0:2]

	s[0] = "Sun"

	fmt.Println(a) // Output: [Sun Tue Wed Thu Fri Sat Sun]
	fmt.Println(s) // Output: [Sun Tue]
}
```

切片也可以作为可变参数。

```go
package main

import "fmt"

func main() {
	values := []int{1, 2, 3}
	sum := add(values...)
	fmt.Println(sum)
}

func add(values ...int) int {
	sum := 0
	for _, v := range values {
		sum += v
	}

	return sum
}
```

这里`values...`符号为对切片进行解包操作。

# 字典

Go提供了内建字典类型，我们来学习如何使用它。

字典是什么呢？又为什么我们需要它呢？

![maps](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-II/maps/maps.png)

字典是一个无序的键值对集合。由键对应到值。键必须唯一，值可以相同。

它用于基于键快速查找，获取及删除数据。最常用的数据结构之一。

## 申明

我们从申明开始。

字典使用如下语法申明：

```go
var m map[K]V
```

`K`是key类型，`V`是值类型。

例如下面申明了`string`为key对应`int`值的字典。

```go
func main() {
	var m map[string]int

	fmt.Println(m)
}
```

```bash
$ go run main.go
nil
```

如果我们所见，map默认零值为`nil`。

`nil`字典没有键，任何尝试通过对`nil`字典使用键操作均会发生运行时错误(panic)。


## 初始化

也有好几种初始化字典的方式。

**make 函数**

我使用内建的`make`函数通过提供对应字典键值对类型来开辟内存作为底层数据结构。

```go
func main() {
	var m = make(map[string]int)

	fmt.Println(m)
}
```

```bash
$ go run main.go
map[]
```

**map 字面量**

另一种方式是使用字典字面量。

```go
func main() {
	var m = map[string]int{
		"a": 0,
    	"b": 1,
	}

	fmt.Println(m)
}
```

_Note that the last trailing comma is necessary_

```bash
$ go run main.go
map[a:0 b:1]
```

As always, we can use our custom types as well.

```go
type User struct {
	Name string
}

func main() {
	var m = map[string]User{
		"a": User{"Peter"},
		"b": User{"Seth"},
	}

	fmt.Println(m)
}
```

We can even remove the value type and Go will figure it out!

```go
var m = map[string]User{
	"a": {"Peter"},
	"b": {"Seth"},
}
```

```bash
$ go run main.go
map[a:{Peter} b:{Seth}]
```

## Add

Now, let's see how we can add a value to our map.

```go
func main() {
	var m = map[string]User{
		"a": {"Peter"},
		"b": {"Seth"},
	}

	m["c"] = User{"Steve"}

	fmt.Println(m)
}
```

```bash
$ go run main.go
map[a:{Peter} b:{Seth} c:{Steve}]
```

### Retrieve

We can also retrieve our values from the map using the key.

```go
...
c := m["c"]
fmt.Println("Key c:", c)
```

```bash
$ go run main.go
key c: {Steve}
```

**What if we use a key that is not present in the map?**

```go
...
d := m["d"]
fmt.Println("Key d:", d)
```

Yes, you guessed it! we will get the zero value of the map's value type.

```bash
$ go run main.go
Key c: {Steve}
Key d: {}
```

### Exists

When you retrieve the value assigned to a given key, it returns an additional boolean value as well. The boolean variable will be `true` if the key exists, and `false` otherwise.

Let's try this in an example:

```go
...
c, ok := m["c"]
fmt.Println("Key c:", c, ok)

d, ok := m["d"]
fmt.Println("Key d:", d, ok)
```

```bash
$ go run main.go
Key c: {Steve} Present: true
Key d: {} Present: false
```

### Updating

We can also update the value for a key by simply re-assigning a key.

```go
...
m["a"] = "Roger"
```

```bash
$ go run main.go
map[a:{Roger} b:{Seth} c:{Steve}]
```

### Deleting

Or, we can delete the key using the built-in `delete` function.

Here's how the syntax looks:

```go
...
delete(m, "a")
```

The first argument is the map, and the second is the key we want to delete.

The `delete()` function doesn't return any value. Also, it doesn't do anything if the key doesn't exist in the map.

```bash
$ go run main.go
map[a:{Roger} c:{Steve}]
```

### Iteration

Similar to arrays or slices, we can iterate over maps with the `range` keyword.

```go
package main

import "fmt"

func main() {
	var m = map[string]User{
		"a": {"Peter"},
		"b": {"Seth"},
	}

	m["c"] = User{"Steve"}

	for key, value := range m {
		fmt.Println("Key: %s, Value: %v", key, value)
	}
}
```

```bash
$ go run main.go
Key: c, Value: {Steve}
Key: a, Value: {Peter}
Key: b, Value: {Seth}
```

Note that a map is an unordered collection, and therefore the iteration order of a map is not guaranteed to be the same every time we iterate over it.

### Properties

Lastly, let's talk about map properties.

Maps are reference types, which means when we assign a map to a new variable, they both refer to the same underlying data structure.

Therefore, changes done by one variable will be visible to the other.

```go
package main

import "fmt"

type User struct {
	Name string
}

func main() {
	var m1 = map[string]User{
		"a": {"Peter"},
		"b": {"Seth"},
	}

	m2 := m1
	m2["c"] = User{"Steve"}

	fmt.Println(m1) // Output: map[a:{Peter} b:{Seth} c:{Steve}]
	fmt.Println(m2) // Output: map[a:{Peter} b:{Seth} c:{Steve}]
}
```

# Interfaces

In this section, let's talk about the interfaces.

## What is an interface?

So, an interface in Go is an **abstract type** that is defined using a set of method signatures. The interface defines the **behavior** for similar types of objects.

_Here, **behavior** is a key term that we will discuss shortly._

Let's take a look at an example to understand this better.

One of the best real-world examples of interfaces is the power socket. Imagine that we need to connect different devices to the power socket.

![no-interface](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-III/interfaces/no-interface.png)

Let's try to implement this. Here are the device types we will be using.

```go
type mobile struct {
	brand string
}

type laptop struct {
	cpu string
}

type toaster struct {
	amount int
}

type kettle struct {
	quantity string
}

type socket struct{}
```

Now, let's define a `Draw` method on a type, let's say `mobile`. Here we will simply print the properties of the type.

```go
func (m mobile) Draw(power int) {
	fmt.Printf("%T -> brand: %s, power: %d", m, m.brand, power)
}
```

Great, now we will define the `Plug` method on the `socket` type which accepts our `mobile` type as an argument.

```go
func (socket) Plug(device mobile, power int) {
	device.Draw(power)
}
```

Let's try to _"connect"_ or _"plug in"_ the `mobile` type to our `socket` type in the `main` function.

```go
package main

import "fmt"

func main() {
	m := mobile{"Apple"}

	s := socket{}
	s.Plug(m, 10)
}
```

And if we run this we'll see the following.

```bash
$ go run main.go
main.mobile -> brand: Apple, power: 10
```

This is interesting, but let's say now we want to connect our `laptop` type.

```go
package main

import "fmt"

func main() {
	m := mobile{"Apple"}
	l := laptop{"Intel i9"}

	s := socket{}

	s.Plug(m, 10)
	s.Plug(l, 50) // Error: cannot use l as mobile value in argument
}
```

As we can see, this will throw an error.

**What should we do now? Define another method? Such as `PlugLaptop`?**

Sure, but then every time we add a new device type we will need to add a new method to the socket type as well and that's not ideal.

This is where the `interface` comes in. Essentially, we want to define a **contract** that, in the future, must be implemented.

We can simply define an interface such as `PowerDrawer` and use it in our `Plug` function to allow any device that satisfies the criteria, which is that the type must have a `Draw` method matching the signature that the interface requires.

And anyways, the socket doesn't need to know anything about our device and can simply call the `Draw` method.

![interface](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-III/interfaces/interface.png)

Now let's try to implement our `PowerDrawer` interface. Here's how it will look.

The convention is to use **"-er"** as a suffix in the name. And as we discussed earlier, an interface should only describe the **expected behavior**. Which in our case is the `Draw` method.

![interface-implementation](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-III/interfaces/interface-implementation.png)

```go
type PowerDrawer interface {
	Draw(power int)
}
```

Now, we need to update our `Plug` method to accept a device that implements the `PowerDrawer` interface as an argument.

```go
func (socket) Plug(device PowerDrawer, power int) {
	device.Draw(power)
}
```

And to satisfy the interface, we can simply add `Draw` methods to all the device types.

```go
type mobile struct {
	brand string
}

func (m mobile) Draw(power int) {
	fmt.Printf("%T -> brand: %s, power: %d\n", m, m.brand, power)
}

type laptop struct {
	cpu string
}

func (l laptop) Draw(power int) {
	fmt.Printf("%T -> cpu: %s, power: %d\n", l, l.cpu, power)
}

type toaster struct {
	amount int
}

func (t toaster) Draw(power int) {
	fmt.Printf("%T -> amount: %d, power: %d\n", t, t.amount, power)
}

type kettle struct {
	quantity string
}

func (k kettle) Draw(power int) {
	fmt.Printf("%T -> quantity: %s, power: %d\n", k, k.quantity, power)
}
```

Now, we can connect all our devices to the socket with the help of our interface!

```go
func main() {
	m := mobile{"Apple"}
	l := laptop{"Intel i9"}
	t := toaster{4}
	k := kettle{"50%"}

	s := socket{}

	s.Plug(m, 10)
	s.Plug(l, 50)
	s.Plug(t, 30)
	s.Plug(k, 25)
}
```

And just as we expected, it works.

```bash
$ go run main.go
main.mobile -> brand: Apple, power: 10
main.laptop -> cpu: Intel i9, power: 50
main.toaster -> amount: 4, power: 30
main.kettle -> quantity: Half Empty, power: 25
```

**But why is this considered such a powerful concept?**

Well, an interface can help us decouple our types. For example, because we have the interface, we don't need to update our `socket` implementation. We can just define a new device type with a `Draw` method.

Unlike other languages, Go Interfaces are implemented **implicitly**, so we don't need something like an `implements` keyword. This means that a type satisfies an interface automatically when it has _"all the methods"_ of the interface.

## Empty Interface

Next, let's talk about the empty interface. An empty interface can take on a value of any type.

Here's how we declare it.

```go
var x interface{}
```

**But why do we need it?**

Empty interfaces can be used to handle values of unknown types.

Some examples are:

- Reading heterogeneous data from an API.
- Variables of an unknown type, like in the `fmt.Println` function.

To use a value of type empty `interface{}`, we can use _type assertion_ or a _type switch_ to determine the type of the value.

## Type Assertion

A _type assertion_ provides access to an interface value's underlying concrete value.

For example:

```go
func main() {
	var i interface{} = "hello"

	s := i.(string)
	fmt.Println(s)
}
```

This statement asserts that the interface value holds a concrete type and assigns the underlying type value to the variable.

We can also test whether an interface value holds a specific type.

A type assertion can return two values:

- The first one is the underlying value.
- The second is a boolean value that reports whether the assertion succeeded.

```go
s, ok := i.(string)
fmt.Println(s, ok)
```

This can help us test whether an interface value holds a specific type or not.

In a way, this is similar to how we read values from a map.

And If this is not the case then, `ok` will be false and the value will be the zero value of the type, and no panic will occur.

```go
f, ok := i.(float64)
fmt.Println(f, ok)
```

But if the interface does not hold the type, the statement will trigger a panic.

```go
f = i.(float64)
fmt.Println(f) // Panic!
```

```bash
$ go run main.go
hello
hello true
0 false
panic: interface conversion: interface {} is string, not float64
```

### Type Switch

Here, a `switch` statement can be used to determine the type of a variable of type empty `interface{}`.

```go
var t interface{}
t = "hello"

switch t := t.(type) {
case string:
	fmt.Printf("string: %s\n", t)
case bool:
	fmt.Printf("boolean: %v\n", t)
case int:
	fmt.Printf("integer: %d\n", t)
default:
	fmt.Printf("unexpected: %T\n", t)
}
```

And if we run this, we can verify that we have a `string` type.

```bash
$ go run main.go
string: hello
```

### Properties

Let's discuss some properties of interfaces.

**Zero value**

The zero value of an interface is `nil`.

```go
package main

import "fmt"

type MyInterface interface {
	Method()
}

func main() {
	var i MyInterface

	fmt.Println(i) // Output: <nil>
}
```

**Embedding**

We can embed interfaces like structs.

_For example_

```go
type interface1 interface {
    Method1()
}

type interface2 interface {
    Method2()
}

type interface3 interface {
    interface1
    interface2
}
```

**Values**

Interface values are comparable.

```go
package main

import "fmt"

type MyInterface interface {
	Method()
}

type MyType struct{}

func (MyType) Method() {}

func main() {
	t := MyType{}
	var i MyInterface = MyType{}

	fmt.Println(t == i)
}
```

**Interface Values**

Under the hood, an interface value can be thought of as a tuple consisting of a value and a concrete type.

```go
package main

import "fmt"

type MyInterface interface {
	Method()
}

type MyType struct {
	property int
}

func (MyType) Method() {}

func main() {
	var i MyInterface

	i = MyType{10}

	fmt.Printf("(%v, %T)\n", i, i) // Output: ({10}, main.MyType)
}
```

With that, we covered interfaces in Go.

It's a really powerful feature, but remember, _"Bigger the interface, the weaker the abstraction"_ - Rob Pike.

# Errors

In this tutorial, let's talk about error handling.

Notice I said errors and not exceptions as there is no exception handling in Go.

Instead, we can just return a built-in `error` type which is an interface type.

```go
type error interface {
    Error() string
}
```

We will circle back to this shortly. First, let's try to understand the basics.

So, let's declare a simple `Divide` function which, as the name suggests, will divide integer `a` by `b`.

```go
func Divide(a, b int) int {
	return a/b
}
```

Great. Now, we want to return an error, let's say, to prevent the division by zero. This brings us to error construction.

## Constructing Errors

There are multiple ways to do this, but we will look at the two most common ones.

### `errors` package

The first is by using the `New` function provided by the `errors` package.

```go
package main

import "errors"

func main() {}

func Divide(a, b int) (int, error) {
	if b == 0 {
		return 0, errors.New("cannot divide by zero")
	}

	return a/b, nil
}
```

Notice, how we return an `error` with the result. And if there is no error we simply return `nil` as it is the zero value of an error because after all, it's an interface.

But how do we handle it? So, for that, let's call the `Divide` function in our `main` function.

```go
package main

import (
	"errors"
	"fmt"
)

func main() {
	result, err := Divide(4, 0)

	if err != nil {
		fmt.Println(err)
		// Do something with the error
		return
	}

	fmt.Println(result)
	// Use the result
}

func Divide(a, b int) (int, error) {...}
```

```bash
$ go run main.go
cannot divide by zero
```

As you can see, we simply check if the error is `nil` and build our logic accordingly. This is considered quite idiomatic in Go and you will see this being used a lot.

Another way to construct our errors is by using the `fmt.Errorf` function.

This function is similar to `fmt.Sprintf` and it lets us format our error. But instead of returning a string, it returns an error.

It is often used to add some context or detail to our errors.

```go
...
func Divide(a, b int) (int, error) {
	if b == 0 {
		return 0, fmt.Errorf("cannot divide %d by zero", a)
	}

	return a/b, nil
}
```

And it should work similarly.

```bash
$ go run main.go
cannot divide 4 by zero
```

### Sentinel Errors

Another important technique in Go is defining expected Errors so they can be checked explicitly in other parts of the code. These are sometimes referred to as sentinel errors.

```go
package main

import (
	"errors"
	"fmt"
)

var ErrDivideByZero = errors.New("cannot divide by zero")

func main() {...}

func Divide(a, b int) (int, error) {
	if b == 0 {
		return 0, ErrDivideByZero
	}

	return a/b, nil
}
```

In Go, it is considered conventional to prefix the variable with `Err`. For example, `ErrNotFound`.

**But what's the point?**

So, this becomes useful when we need to execute a different branch of code if a certain kind of error is encountered.

For example, now we can check explicitly which error occurred using the `errors.Is` function.

```go
package main

import (
	"errors"
	"fmt"
)

func main() {
	result, err := Divide(4, 0)

	if err != nil {
		switch {
    case errors.Is(err, ErrDivideByZero):
        fmt.Println(err)
				// Do something with the error
    default:
        fmt.Println("no idea!")
    }

		return
	}

	fmt.Println(result)
	// Use the result
}

func Divide(a, b int) (int, error) {...}
```

```bash
$ go run main.go
cannot divide by zero
```

## Custom Errors

This strategy covers most of the error handling use cases. But sometimes we need additional functionalities such as dynamic values inside of our errors.

Earlier, we saw that `error` is just an interface. So basically, anything can be an `error` as long as it implements the `Error()` method which returns an error message as a string.

So, let's define our custom `DivisionError` struct which will contain an error code and a message.

```go
package main

import (
	"errors"
	"fmt"
)

type DivisionError struct {
	Code int
	Msg  string
}

func (d DivisionError) Error() string {
	return fmt.Sprintf("code %d: %s", d.Code, d.Msg)
}

func main() {...}

func Divide(a, b int) (int, error) {
	if b == 0 {
		return 0, DivisionError{
			Code: 2000,
			Msg:  "cannot divide by zero",
		}
	}

	return a/b, nil
}
```

Here, we will use `errors.As` instead of `errors.Is` function to convert the error to the correct type.

```go
func main() {
	result, err := Divide(4, 0)

	if err != nil {
		var divErr DivisionError

		switch {
		case errors.As(err, &divErr):
			fmt.Println(divErr)
			// Do something with the error
		default:
			fmt.Println("no idea!")
		}

		return
	}

	fmt.Println(result)
	// Use the result
}

func Divide(a, b int) (int, error) {...}
```

```bash
$ go run man.go
code 2000: cannot divide by zero
```

**But what's the difference between `errors.Is` and `errors.As`?**

The difference is that this function checks whether the error has a specific type, unlike the [`Is`](https://pkg.go.dev/errors#Is) function, which examines if it is a particular error object.

We can also use type assertions but it's not preferred.

```go
func main() {
	result, err := Divide(4, 0)

	if e, ok := err.(DivisionError); ok {
		fmt.Println(e.Code, e.Msg) // Output: 2000 cannot divide by zero
		return
	}

	fmt.Println(result)
}
```

Lastly, I will say that error handling in Go is quite different compared to the traditional `try/catch` idiom in other languages. But it is very powerful as it encourages the developer to actually handle the error in an explicit way, which improves readability as well.

# Panic and Recover

So earlier, we learned that the idiomatic way of handling abnormal conditions in a Go program is using errors. While errors are sufficient for most cases, there are some situations where the program cannot continue.

In those cases, we can use the built-in `panic` function.

## Panic

```go
func panic(interface{})
```

The panic is a built-in function that stops the normal execution of the current `goroutine`. When a function calls `panic`, the normal execution of the function stops immediately and the control is returned to the caller. This is repeated until the program exits with the panic message and stack trace.

_Note: We will discuss `goroutines` later in the course._

So, let's see how we can use the `panic` function.

```go
package main

func main() {
	WillPanic()
}

func WillPanic() {
	panic("Woah")
}
```

And if we run this, we can see `panic` in action.

```bash
$ go run main.go
panic: Woah

goroutine 1 [running]:
main.WillPanic(...)
        .../main.go:8
main.main()
        .../main.go:4 +0x38
exit status 2
```

As expected, our program printed the panic message, followed by the stack trace, and then it was terminated.

So, the question is, what to do when an unexpected panic happens?

## Recover

Well, it is possible to regain control of a panicking program using the built-in `recover` function, along with the `defer` keyword.

```go
func recover() interface{}
```

Let's try an example by creating a `handlePanic` function. And then, we can call it using `defer`.

```go
package main

import "fmt"

func main() {
	WillPanic()
}

func handlePanic() {
	data := recover()
	fmt.Println("Recovered:", data)
}

func WillPanic() {
	defer handlePanic()

	panic("Woah")
}
```

```bash
$ go run main.go
Recovered: Woah
```

As we can see, our panic was recovered and now our program can continue execution.

Lastly, I will mention that `panic` and `recover` can be considered similar to the `try/catch` idiom in other languages. But one important factor is that we should avoid panic and recover and use [errors](https://karanpratapsingh.com/courses/go/errors) when possible.

If so, then this brings us to the question, when should we use `panic`?

## Use Cases

There are two valid use cases for `panic`:

- **An unrecoverable error**

Which can be a situation where the program cannot simply continue its execution.

For example, reading a configuration file which is important to start the program, as there is nothing else to do if the file read itself fails.

- **Developer error**

This is the most common situation. For example, dereferencing a pointer when the value is `nil` will cause a panic.

# Testing

In this tutorial, we will talk about testing in Go. So, let's start using a simple example.

We have created a `math` package that contains an `Add` function Which as the name suggests, adds two integers.

```go
package math

func Add(a, b int) int {
	return a + b
}
```

It's being used in our `main` package like this.

```go
package main

import (
	"example/math"
	"fmt"
)

func main() {
	result := math.Add(2, 2)
	fmt.Println(result)
}

```

And, if we run this, we should see the result.

```bash
$ go run main.go
4
```

Now, we want to test our `Add` function. So, in Go, we declare test files with `_test` suffix in the file name. So for our `add.go`, we will create a test as `add_test.go`. Our project structure should look like this.

```bash
.
├── go.mod
├── main.go
└── math
    ├── add.go
    └── add_test.go
```

We will start by using a `math_test` package, and importing the `testing` package from the standard library. That's right! Testing is built into Go, unlike many other languages.

But wait...why do we need to use `math_test` as our package, can't we just use the same `math` package?

Well yes, we can write our test in the same package if we wanted, but I personally think doing this in a separate package helps us write tests in a more decoupled way.

Now, we can create our `TestAdd` function. It will take an argument of type `testing.T` which will provide us with helpful methods.

```go
package math_test

import "testing"

func TestAdd(t *testing.T) {}
```

Before we add any testing logic, let's try to run it. But this time, we cannot use `go run` command, instead, we will use the `go test` command.

```bash
$ go test ./math
ok      example/math 0.429s
```

Here, we will have our package name which is `math`, but we can also use the relative path `./...` to test all packages.

```bash
$ go test ./...
?       example [no test files]
ok      example/math 0.348s
```

And if Go doesn't find any test in a package, it will let us know.

Perfect, let's write some test code. To do this, we will check our result with an expected value and if they do not match, we can use the `t.Fail` method to fail the test.

```go
package math_test

import "testing"

func TestAdd(t *testing.T) {
	got := math.Add(1, 1)
	expected := 2

	if got != expected {
		t.Fail()
	}
}
```

Great! Our test seems to have passed.

```bash
$ go test math
ok      example/math    0.412s
```

Let's also see what happens if we fail the test, for that, we can simply change our expected result.

```go
package math_test

import "testing"

func TestAdd(t *testing.T) {
	got := math.Add(1, 1)
	expected := 3

	if got != expected {
		t.Fail()
	}
}
```

```bash
$ go test ./math
ok      example/math    (cached)
```

If you see this, don't worry. For optimization, our tests are cached. We can use the `go clean` command to clear our cache and then re-run the test.

```bash
$ go clean -testcache
$ go test ./math
--- FAIL: TestAdd (0.00s)
FAIL
FAIL    example/math    0.354s
FAIL
```

So, this is what a test failure will look like.

## Table driven tests

This brings us to table-driven tests. But what exactly are they?

So earlier, we had function arguments and expected variables which we compared to determine if our tests passed or fail. But what if we defined all that in a slice and iterate over that? This will make our tests a little bit more flexible and help us run multiple cases easily.

Don't worry, we will learn this by example. So we will start by defining our `addTestCase` struct.

```go
package math_test

import (
	"example/math"
	"testing"
)

type addTestCase struct {
	a, b, expected int
}

var testCases = []addTestCase{
	{1, 1, 3},
	{25, 25, 50},
	{2, 1, 3},
	{1, 10, 11},
}

func TestAdd(t *testing.T) {

	for _, tc := range testCases {
		got := math.Add(tc.a, tc.b)

		if got != tc.expected {
			t.Errorf("Expected %d but got %d", tc.expected, got)
		}
	}
}
```

Notice, how we declared `addTestCase` with a lower case. That's right we don't want to export it as it's not useful outside our testing logic. Let's run our test.

```bash
$ go run main.go
--- FAIL: TestAdd (0.00s)
    add_test.go:25: Expected 3 but got 2
FAIL
FAIL    example/math    0.334s
FAIL
```

Seems like our tests broke, let's fix them by updating our test cases.

```go
var testCases = []addTestCase{
	{1, 1, 2},
	{25, 25, 50},
	{2, 1, 3},
	{1, 10, 11},
}
```

Perfect, it's working!

```bash
$ go run main.go
ok      example/math    0.589s
```

## Code coverage

Finally, let's talk about code coverage. When writing tests, it is often important to know how much of your actual code the tests cover. This is generally referred to as code coverage.

To calculate and export the coverage for our test, we can simply use the `-coverprofile` argument with the `go test` command.

```bash
$ go test ./math -coverprofile=coverage.out
ok      example/math    0.385s  coverage: 100.0% of statements
```

Seems like we have great coverage. Let's also check the report using the `go tool cover` command which gives us a detailed report.

```bash
$ go tool cover -html=coverage.out
```

![coverage](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-III/testing/coverage.png)

As we can see, this is a much more readable format. And best of all, it is built right into standard tooling.

## Fuzz testing

Lastly, let's look at fuzz testing which was introduced in Go version 1.18.

Fuzzing is a type of automated testing that continuously manipulates inputs to a program to find bugs.

Go fuzzing uses coverage guidance to intelligently walk through the code being fuzzed to find and report failures to the user.

Since it can reach edge cases that humans often miss, fuzz testing can be particularly valuable for finding bugs and security exploits.

Let's try an example:

```go
func FuzzTestAdd(f *testing.F) {
	f.Fuzz(func(t *testing.T, a, b int) {
		math.Add(a , b)
	})
}
```

If we run this, we'll see that it'll automatically create test cases. Because our `Add` function is quite simple, tests will pass.

```bash
$ go test -fuzz FuzzTestAdd example/math
fuzz: elapsed: 0s, gathering baseline coverage: 0/192 completed
fuzz: elapsed: 0s, gathering baseline coverage: 192/192 completed, now fuzzing with 8 workers
fuzz: elapsed: 3s, execs: 325017 (108336/sec), new interesting: 11 (total: 202)
fuzz: elapsed: 6s, execs: 680218 (118402/sec), new interesting: 12 (total: 203)
fuzz: elapsed: 9s, execs: 1039901 (119895/sec), new interesting: 19 (total: 210)
fuzz: elapsed: 12s, execs: 1386684 (115594/sec), new interesting: 21 (total: 212)
PASS
ok      foo 12.692s
```

But if we update our `Add` function with a random edge case such that the program will panic if `b + 10` is greater than `a`.

```go
func Add(a, b int) int {
	if a > b + 10 {
		panic("B must be greater than A")
	}

	return a + b
}
```

And if we re-run the test, this edge case will be caught by fuzz testing.

```bash
$ go test -fuzz FuzzTestAdd example/math
warning: starting with empty corpus
fuzz: elapsed: 0s, execs: 0 (0/sec), new interesting: 0 (total: 0)
fuzz: elapsed: 0s, execs: 1 (25/sec), new interesting: 0 (total: 0)
--- FAIL: FuzzTestAdd (0.04s)
    --- FAIL: FuzzTestAdd (0.00s)
        testing.go:1349: panic: B is greater than A
```

I think this is a really cool feature of Go 1.18. You can learn more about fuzz testing from the [official Go blog](https://go.dev/doc/fuzz/).

# Generics

In this section, we will learn about Generics which is a much awaited feature that was released with Go version 1.18.

## What are Generics?

Generics means parameterized types. Put simply, generics allow programmers to write code where the type can be specified later because the type isn't immediately relevant.

Let's take a look at an example to understand this better.

For our example, we have simple sum functions for different types such as `int`, `float64`, and `string`. Since method overriding is not allowed in Go we usually have to create new functions.

```go
package main

import "fmt"

func sumInt(a, b int) int {
	return a + b
}

func sumFloat(a, b float64) float64 {
	return a + b
}

func sumString(a, b string) string {
	return a + b
}

func main() {
	fmt.Println(sumInt(1, 2))
	fmt.Println(sumFloat(4.0, 2.0))
	fmt.Println(sumString("a", "b"))
}
```

As we can see, apart from the types, these functions are pretty similar.

Let's see how we can define a generic function.

```go
func fnName[T constraint]() {
	...
}
```

Here, `T` is our type parameter and `constraint` will be the interface that allows any type implementing the interface.

I know, I know, this is confusing. So, let's start building our generic `sum` function.

Here, we will use `T` as our type parameter with an empty `interface{}` as our constraint.

```go
func sum[T interface{}](a, b T) T {
	fmt.Println(a, b)
}
```

Also, starting with Go 1.18 we can use `any`, which is pretty much equivalent to the empty interface.

```go
func sum[T any](a, b T) T {
	fmt.Println(a, b)
}
```

With type parameters, comes the need to pass type arguments, which can make our code verbose.

```go
sum[int](1, 2) // explicit type argument
sum[float64](4.0, 2.0)
sum[string]("a", "b")
```

Luckily, Go 1.18 comes with **type inference** which helps us to write code that calls generic functions without explicit types.

```go
sum(1, 2)
sum(4.0, 2.0)
sum("a", "b")
```

Let's run this and see if it works.

```bash
$ go run main.go
1 2
4 2
a b
```

Now, let's update the `sum` function to add our variables.

```go
func sum[T any](a, b T) T {
	return a + b
}
```

```go
fmt.Println(sum(1, 2))
fmt.Println(sum(4.0, 2.0))
fmt.Println(sum("a", "b"))
```

But now if we run this, we will get an error that operator `+` is not defined in the constraint.

```bash
$ go run main.go
./main.go:6:9: invalid operation: operator + not defined on a (variable of type T constrained by any)
```

While constraint of type `any` generally works it does not support operators.

So let's define our own custom constraint using an interface. Our interface should define a type set containing `int`, `float`, and `string`.

![typeset](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-III/generics/typeset.png)

Here's how our `SumConstraint` interface looks.

```go
type SumConstraint interface {
	int | float64 | string
}

func sum[T SumConstraint](a, b T) T {
	return a + b
}

func main() {
	fmt.Println(sum(1, 2))
	fmt.Println(sum(4.0, 2.0))
	fmt.Println(sum("a", "b"))
}
```

And this should work as expected

```bash
$ go run main.go
3
6
ab
```

We can also use the `constraints` package which defines a set of useful constraints to be used with type parameters.

```go
type Signed interface {
	~int | ~int8 | ~int16 | ~int32 | ~int64
}

type Unsigned interface {
	~uint | ~uint8 | ~uint16 | ~uint32 | ~uint64 | ~uintptr
}

type Integer interface {
	Signed | Unsigned
}

type Float interface {
	~float32 | ~float64
}

type Complex interface {
	~complex64 | ~complex128
}

type Ordered interface {
	Integer | Float | ~string
}
```

For that, we will need to install the `constraints` package.

```bash
$ go get golang.org/x/exp/constraints
go: added golang.org/x/exp v0.0.0-20220414153411-bcd21879b8fd
```

```go
import (
	"fmt"

	"golang.org/x/exp/constraints"
)

func sum[T constraints.Ordered](a, b T) T {
	return a + b
}

func main() {
	fmt.Println(sum(1, 2))
	fmt.Println(sum(4.0, 2.0))
	fmt.Println(sum("a", "b"))
}
```

Here we are using the `Ordered` constraint.

```go
type Ordered interface {
	Integer | Float | ~string
}
```

`~` is a new token added to Go and the expression `~string` means the set of all types whose underlying type is `string`.

And it still works as expected.

```bash
$ go run main.go
3
6
ab
```

Generics is an amazing feature because it permits writing abstract functions that can drastically reduce code duplication in certain cases.

## When to use generics

So, when to use generics? We can take the following use cases as an example:

- Functions that operate on arrays, slices, maps, and channels.
- General purpose data structures like stack or linked list.
- To reduce code duplication.

Lastly, I will add that while generics are a great addition to the language, they should be used sparingly.

And, it is advised to start simple and only write generic code once we have written very similar code at least 2 or 3 times.

# Concurrency

In this lesson, we will learn about concurrency which is one of the most powerful features of Go.

So, let's start by asking What is _"concurrency"_?

## What is Concurrency

Concurrency, by definition, is the ability to break down a computer program or algorithm into individual parts, which can be executed independently.

The final outcome of a concurrent program is the same as that of a program that has been executed sequentially.

Using concurrency, we can achieve the same results in lesser time, thus increasing the overall performance and efficiency of our programs.

## Concurrency vs Parallelism

![concurrency-vs-parallelism](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/concurrency/concurrency-vs-parallelism.png)

A lot of people confuse concurrency with parallelism because they both somewhat imply executing code simultaneously, but they are two completely different concepts.

Concurrency is the task of running and managing multiple computations at the same time, while parallelism is the task of running multiple computations simultaneously.

A simple quote from Rob Pike pretty much sums it up.

_"Concurrency is about dealing with lots of things at once. Parallelism is about doing lots of things at once"_

But concurrency in Go is more than just syntax. In order to harness the power of Go, we need to first understand how Go approaches concurrent execution of code. Go relies on a concurrency model called CSP (Communicating Sequential Processes).

## Communicating Sequential Processes (CSP)

[Communicating Sequential Processes](https://dl.acm.org/doi/10.1145/359576.359585) (CSP) is a model put forth by [Tony Hoare](https://en.wikipedia.org/wiki/Tony_Hoare) in 1978 which describes interactions between concurrent processes. It made a breakthrough in Computer Science, especially in the field of concurrency.

Languages like Go and Erlang have been highly inspired by the concept of communicating sequential processes (CSP).

Concurrency is hard, but CSP allows us to give a better structure to our concurrent code and provides a model for thinking about concurrency in a way that makes it a little easier. Here, processes are independent and they communicate by sharing channels between them.

![csp](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/concurrency/csp.png)

_We'll learn how Golang implements it using goroutines and channels later in the course._

## Basic Concepts

Now, let's get familiar with some basic concurrency concepts

### Data Race

A data race occurs when processes have to access the same resource concurrently.

_For example, one process reads while another simultaneously writes to the exact same resource._

### Race Conditions

A race condition occurs when the timing or order of events affects the correctness of a piece of code.

### Deadlocks

A deadlock occurs when all processes are blocked while waiting for each other and the program cannot proceed further.

**Coffman Conditions**

There are four conditions, known as the Coffman conditions, all of them must be satisfied for a deadlock to occur.

- **Mutual Exclusion**

A concurrent process holds at least one resource at any one time making it non-sharable.

_In the diagram below, there is a single instance of Resource 1 and it is held by Process 1 only._

![mutual-exclusion](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/concurrency/mutual-exclusion.png)

- **Hold and wait**

A concurrent process holds a resource and is waiting for an additional resource.

_In the diagram given below, Process 2 holds Resource 2 and Resource 3 and is requesting the Resource 1 which is held by Process 1._

![hold-and-wait](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/concurrency/hold-and-wait.png)

- **No preemption**

A resource held by a concurrent process cannot be taken away by the system. It can only be freed by the process holding it.

_In the diagram below, Process 2 cannot preempt Resource 1 from Process 1. It will only be released when Process 1 relinquishes it voluntarily after its execution is complete._

![no-preemption](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/concurrency/no-preemption.png)

- **Circular wait**

A process is waiting for the resource held by the second process, which is waiting for the resource held by the third process, and so on, till the last process is waiting for a resource held by the first process. Hence, forming a circular chain.

_In the diagram below, Process 1 is allocated Resource2 and it is requesting Resource 1. Similarly, Process 2 is allocated Resource 1 and it is requesting Resource 2. This forms a circular wait loop._

![circular-wait](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/concurrency/circular-wait.png)

### Livelocks

Livelocks are processes that are actively performing concurrent operations, but these operations do nothing to move the state of the program forward.

### Starvation

Starvation happens when a process is deprived of necessary resources and is unable to complete its function.

Starvation can happen because of deadlocks or inefficient scheduling algorithms for processes. In order to solve starvation, we need to employ better resource-allotment algorithms that make sure that every process gets its fair share of resources.

# Goroutines

In this lesson, we will learn about Goroutines.

But before we start our discussion, I wanted to share an important Go proverb.

_"Don't communicate by sharing memory, share memory by communicating."_ - Rob Pike

## What is a goroutine?

A _goroutine_ is a lightweight thread of execution that is managed by the Go runtime and essentially let us write asynchronous code in a synchronous manner.

It is important to know that they are not actual OS threads and the main function itself runs as a goroutine.

A single thread may run thousands of goroutines in them by using the Go runtime scheduler which uses cooperative scheduling. This implies that if the current goroutine is blocked or has been completed, the scheduler will move the other goroutines to another OS thread. Hence, we achieve efficiency in scheduling where no routine is blocked forever.

We can turn any function into a goroutine by simply using the `go` keyword.

```go
go fn(x, y, z)
```

Before we write any code, it is important to briefly discuss the fork-join model.

## Fork-Join Model

Go uses the idea of the fork-join model of concurrency behind goroutines. The fork-join model essentially implies that a child process splits from its parent process to run concurrently with the parent process. After completing its execution, the child process merges back into the parent process. The point where it joins back is called the **join point**.

![fork-join](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/goroutines/fork-join.png)

Now, let's write some code and create our own goroutine.

```go
package main

import "fmt"

func speak(arg string) {
	fmt.Println(arg)
}

func main() {
	go speak("Hello World")
}
```

Here the `speak` function call is prefixed with the `go` keyword. This will allow it to run as a separate goroutine. And that's it, we just created our first goroutine. It's that simple!

Great, let's run this:

```bash
$ go run main.go

```

Interesting, it seems like our program did not run completely as it's missing some output. This is because our main goroutine exited and did not wait for the goroutine that we created.

What if we make our program wait using the `time.Sleep` function?

```go
func main() {
	...
	time.Sleep(1 * time.Second)
}
```

And now, if we run this.

```bash
$ go run main.go
Hello World
```

There we go, we can see our complete output now.

**Okay, so this works but it's not ideal. So how do we improve this?**

Well, the most tricky part about using goroutines is knowing when they will stop. It is important to know that goroutines run in the same address space, so access to shared memory must be synchronized.

# Channels

In this lesson, we will learn about Channels.

## So what are channels?

Well, simply defined a channel is a communications pipe between goroutines. Things go in one end and come out another in the same order until the channel is closed.

![channel](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/channels/channel.png)

As we learned earlier, channels in Go are based on Communicating Sequential Processes (CSP).

## Creating a channel

Now that we understand what channels are, let's see how we can declare them.

```go
var ch chan T
```

Here, we prefix our type `T` which is the data type of the value we want to send and receive with the keyword `chan` which stands for a channel.

Let's try printing the value of our channel `c` of type `string`.

```go
func main() {
	var ch chan string

	fmt.Println(c)
}
```

```bash
$ go run main.go
<nil>
```

As we can see, the zero value of a channel is `nil` and if we try to send data over the channel our program will panic.

So, similar to slices we can initialize our channel using the built-in `make` function.

```go
func main() {
	ch := make(chan string)

	fmt.Println(c)
}
```

And if we run this, we can see our channel was initialized.

```bash
$ go run main.go
0x1400010e060
```

## Sending and Receiving data

Now that we have a basic understanding of channels, let us implement our earlier example using channels to learn how we can use them to communicate between our goroutines.

```go
package main

import "fmt"

func speak(arg string, ch chan string) {
	ch <- arg // Send
}

func main() {
	ch := make(chan string)

	go speak("Hello World", ch)

	data := <-ch // Receive
	fmt.Println(data)
}
```

Notice how we can send data using the `channel<-data` and receive data using the `data := <-channel` syntax.

And if we run this

```bash
$ go run main.go
Hello World
```

Perfect, our program ran as we expected.

## Buffered Channels

We also have buffered channels that accept a limited number of values without a corresponding receiver for those values.

![buffered-channel](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/channels/buffered-channel.png)

This _buffer length_ or _capacity_ can be specified using the second argument to the `make` function.

```go
func main() {
	ch := make(chan string, 2)

	go speak("Hello World", ch)
	go speak("Hi again", ch)

	data1 := <-ch
	fmt.Println(data1)

	data2 := <-ch
	fmt.Println(data2)
}
```

Because this channel is buffered, we can send these values into the channel without a corresponding concurrent receive. This means _sends_ to a buffered channel block only when the buffer is full and _receives_ block when the buffer is empty.

By default, a channel is unbuffered and has a capacity of 0, hence, we omit the second argument to the `make` function.

Next, we have directional channels.

## Directional channels

When using channels as function parameters, we can specify if a channel is meant to only send or receive values. This increases the type-safety of our program as by default a channel can both send and receive values.

![directional-channels](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/channels/directional-channels.png)

In our example, we can update our `speak` function's second argument such that it can only send a value.

```go
func speak(arg string, ch chan<- string) {
	ch <- arg // Send Only
}
```

Here, `chan<-` can only be used for sending values and will panic if we try to receive values.

## Closing channels

Also, just like any other resource, once we're done with our channel, we need to close it. This can be achieved using the built-in `close` function.

Here, we can just pass our channel to the `close` function.

```go
func main() {
	ch := make(chan string, 2)

	go speak("Hello World", ch)
	go speak("Hi again", ch)

	data1 := <-ch
	fmt.Println(data1)

	data2 := <-ch
	fmt.Println(data2)

	close(ch)
}
```

Optionally, receivers can test whether a channel has been closed by assigning a second parameter to the receive expression.

```go
func main() {
	ch := make(chan string, 2)

	go speak("Hello World", ch)
	go speak("Hi again", ch)

	data1 := <-ch
	fmt.Println(data1)

	data2, ok := <-ch
	fmt.Println(data2, ok)

	close(ch)
}
```

if `ok` is `false` then there are no more values to receive and the channel is closed.

_In a way, this is similar to how we check if a key exists or not in a map._

## Properties

Lastly, let's discuss some properties of channels:

- A send to a nil channel blocks forever.

```go
var c chan string
c <- "Hello, World!" // Panic: all goroutines are asleep - deadlock!
```

- A receive from a nil channel blocks forever.

```go
var c chan string
fmt.Println(<-c) // Panic: all goroutines are asleep - deadlock!
```

- A send to a closed channel panics.

```go
var c = make(chan string, 1)
c <- "Hello, World!"
close(c)
c <- "Hello, Panic!" // Panic: send on closed channel
```

- A receive from a closed channel returns the zero value immediately.

```go
var c = make(chan int, 2)
c <- 5
c <- 4
close(c)
for i := 0; i < 4; i++ {
    fmt.Printf("%d ", <-c) // Output: 5 4 0 0
}
```

- Range over channels.

We can also use `for` and `range` to iterate over values received from a channel.

```go
package main

import "fmt"

func main() {
	ch := make(chan string, 2)

	ch <- "Hello"
	ch <- "World"

	close(ch)

	for data := range ch {
		fmt.Println(data)
	}
}
```

# Select

In this tutorial, we will learn about the `select` statement in Go.

The `select` statement blocks the code and waits for multiple channel operations simultaneously.

A `select` blocks until one of its cases can run, then it executes that case. It chooses one at random if multiple are ready.

```go
package main

import (
	"fmt"
	"time"
)

func main() {
	one := make(chan string)
	two := make(chan string)

	go func() {
		time.Sleep(time.Second * 2)
		one <- "One"
	}()

	go func() {
		time.Sleep(time.Second * 1)
		two <- "Two"
	}()

	select {
	case result := <-one:
		fmt.Println("Received:", result)
	case result := <-two:
		fmt.Println("Received:", result)
	}

	close(one)
	close(two)
}
```

Similar to `switch`, `select` also has a default case that runs if no other case is ready. This will help us send or receive without blocking.

```go
func main() {
	one := make(chan string)
	two := make(chan string)

	for x := 0; x < 10; x++ {
		go func() {
			time.Sleep(time.Second * 2)
			one <- "One"
		}()

		go func() {
			time.Sleep(time.Second * 1)
			two <- "Two"
		}()
	}

	for x := 0; x < 10; x++ {
		select {
		case result := <-one:
			fmt.Println("Received:", result)
		case result := <-two:
			fmt.Println("Received:", result)
		default:
			fmt.Println("Default...")
			time.Sleep(200 * time.Millisecond)
		}
	}

	close(one)
	close(two)
}
```

It's also important to know that an empty `select {}` blocks forever.

```go
func main() {
	...
	select {}

	close(one)
	close(two)
}
```

# Sync Package

As we learned earlier, goroutines run in the same address space, so access to shared memory must be synchronized. The [`sync`](https://go.dev/pkg/sync/) package provides useful primitives.

## WaitGroup

A WaitGroup waits for a collection of goroutines to finish. The main goroutine calls `Add` to set the number of goroutines to wait for. Then each of the goroutines runs and calls `Done` when finished. At the same time, `Wait` can be used to block until all goroutines have finished.

### Usage

We can use the `sync.WaitGroup` using the following methods:

- `Add(delta int)` takes in an integer value which is essentially the number of goroutines that the `WaitGroup` has to wait for. This must be called before we execute a goroutine.
- `Done()` is called within the goroutine to signal that the goroutine has successfully executed.
- `Wait()` blocks the program until all the goroutines specified by `Add()` have invoked `Done()` from within.

### Example

Let's take a look at an example.

```go
package main

import (
	"fmt"
	"sync"
)

func work() {
	fmt.Println("working...")
}

func main() {
	var wg sync.WaitGroup

	wg.Add(1)
	go func() {
		defer wg.Done()
		work()
	}()

	wg.Wait()
}
```

If we run this, we can see our program runs as expected.

```bash
$ go run main.go
working...
```

We can also pass the `WaitGroup` to the function directly.

```go
func work(wg *sync.WaitGroup) {
	defer wg.Done()
	fmt.Println("working...")
}

func main() {
	var wg sync.WaitGroup

	wg.Add(1)

	go work(&wg)

	wg.Wait()
}
```

But is important to know that a `WaitGroup` must **not be copied** after first use. And if it's explicitly passed into functions, it should be done by a _pointer._ This is because it can affect our counter which will disrupt the logic of our program.

Let's also increase the number of goroutines by calling the `Add` method to wait for 4 goroutines.

```go
func main() {
	var wg sync.WaitGroup

	wg.Add(4)

	go work(&wg)
	go work(&wg)
	go work(&wg)
	go work(&wg)

	wg.Wait()
}
```

And as expected, all our goroutines were executed.

```bash
$ go run main.go
working...
working...
working...
working...
```

## Mutex

A Mutex is a mutual exclusion lock that prevents other processes from entering a critical section of data while a process occupies it to prevent race conditions from happening.

### What's a critical section?

So, a critical section can be a piece of code that must not be run by multiple threads at once because the code contains shared resources.

### Usage

We can use `sync.Mutex` using the following methods:

- `Lock()` acquires or holds the lock.
- `Unlock()` releases the lock.
- `TryLock()` tries to lock and reports whether it succeeded.

### Example

Let's take a look at an example, we will create a `Counter` struct and add an `Update` method which will update the internal value.

```go
package main

import (
	"fmt"
	"sync"
)

type Counter struct {
	value int
}

func (c *Counter) Update(n int, wg *sync.WaitGroup) {
	defer wg.Done()
	fmt.Printf("Adding %d to %d\n", n, c.value)
	c.value += n
}

func main() {
	var wg sync.WaitGroup

	c := Counter{}

	wg.Add(4)

	go c.Update(10, &wg)
	go c.Update(-5, &wg)
	go c.Update(25, &wg)
	go c.Update(19, &wg)

	wg.Wait()
	fmt.Println(c.value)
}
```

Let's run this and see what happens.

```bash
$ go run main.go
Adding -5 to 0
Adding 10 to 0
Adding 19 to 0
Adding 25 to 0
Result is 49
```

That doesn't look accurate, seems like our value is always zero but we somehow got the correct answer.

Well, this is because, in our example, multiple goroutines are updating the `value` variable. And as you must have guessed, this is not ideal.

This is the perfect use case for Mutex. So, let's start by using `sync.Mutex` and wrap our critical section in between `Lock()` and `Unlock()` methods.

```go
package main

import (
	"fmt"
	"sync"
)

type Counter struct {
	m     sync.Mutex
	value int
}

func (c *Counter) Update(n int, wg *sync.WaitGroup) {
	c.m.Lock()
	defer wg.Done()
	fmt.Printf("Adding %d to %d\n", n, c.value)
	c.value += n
	c.m.Unlock()
}

func main() {
	var wg sync.WaitGroup

	c := Counter{}

	wg.Add(4)

	go c.Update(10, &wg)
	go c.Update(-5, &wg)
	go c.Update(25, &wg)
	go c.Update(19, &wg)

	wg.Wait()
}
```

```bash
$ go run main.go
Adding -5 to 0
Adding 19 to -5
Adding 25 to 14
Adding 10 to 39
Result is 49
```

Looks like we solved our issue and the output looks correct as well.

_Note: Similar to WaitGroup a Mutex must **not be copied** after first use._

## RWMutex

An RWMutex is a reader/writer mutual exclusion lock. The lock can be held by an arbitrary number of readers or a single writer.

In other words, readers don't have to wait for each other. They only have to wait for writers holding the lock.

`sync.RWMutex` is thus preferable for data that is mostly read, and the resource that is saved compared to a `sync.Mutex` is time.

### Usage

Similar to `sync.Mutex`, we can use `sync.RWMutex` using the following methods:

- `Lock()` acquires or holds the lock.
- `Unlock()` releases the lock.
- `RLock()` acquires or holds the read lock.
- `RUnlock()` releases the read lock.

_Notice how RWMutex has additional `RLock` and `RUnlock`_ methods _compared to Mutex._

### Example

Let's add a `GetValue` method which will read the counter value. We will also change `sync.Mutex` to `sync.RWMutex`.

Now, we can simply use the `RLock` and `RUnlock` methods so that readers don't have to wait for each other.

```go
package main

import (
	"fmt"
	"sync"
	"time"
)

type Counter struct {
	m     sync.RWMutex
	value int
}

func (c *Counter) Update(n int, wg *sync.WaitGroup) {
	defer wg.Done()

	c.m.Lock()
	fmt.Printf("Adding %d to %d\n", n, c.value)
	c.value += n
	c.m.Unlock()
}

func (c *Counter) GetValue(wg *sync.WaitGroup) {
	defer wg.Done()

	c.m.RLock()
	defer c.m.RUnlock()
	fmt.Println("Get value:", c.value)
	time.Sleep(400 * time.Millisecond)
}

func main() {
	var wg sync.WaitGroup

	c := Counter{}

	wg.Add(4)

	go c.Update(10, &wg)
	go c.GetValue(&wg)
	go c.GetValue(&wg)
	go c.GetValue(&wg)

	wg.Wait()
}
```

```bash
$ go run main.go
Get value: 0
Adding 10 to 0
Get value: 10
Get value: 10
```

_Note: Both `sync.Mutex` and `sync.RWMutex` implements the `sync.Locker` interface:_

```go
type Locker interface {
    Lock()
    Unlock()
}
```

## Cond

The `sync.Cond` condition variable can be used to coordinate those goroutines that want to share resources. When the state of shared resources changes, it can be used to notify goroutines blocked by a mutex.

Each Cond has an associated lock (often a `*Mutex` or `*RWMutex`), which must be held when changing the condition and when calling the Wait method.

### But why do we need it?

One scenario can be when one process is receiving data, and other processes must wait for this process to receive data before they can read the correct data.

If we simply use a [channel](https://karanpratapsingh.com/courses/go/channels) or mutex, only one process can wait and read the data. There is no way to notify other processes to read the data. Thus, we can `sync.Cond` to coordinate shared resources.

### Usage

`sync.Cond` comes with the following methods:

- `NewCond(l Locker)` returns a new Cond.
- `Broadcast()` wakes all goroutines waiting on the condition.
- `Signal()` wakes one goroutine waiting on the condition if there is any.
- `Wait()` atomically unlocks the underlying mutex lock.

### Example

Here is an example that demonstrates the interaction of different goroutines using the `Cond`.

```go
package main

import (
	"fmt"
	"sync"
	"time"
)

var done = false

func read(name string, c *sync.Cond) {
	c.L.Lock()
	for !done {
		c.Wait()
	}
	fmt.Println(name, "starts reading")
	c.L.Unlock()
}

func write(name string, c *sync.Cond) {
	fmt.Println(name, "starts writing")
	time.Sleep(time.Second)

	c.L.Lock()
	done = true
	c.L.Unlock()

	fmt.Println(name, "wakes all")
	c.Broadcast()
}

func main() {
	var m sync.Mutex
	cond := sync.NewCond(&m)

	go read("Reader 1", cond)
	go read("Reader 2", cond)
	go read("Reader 3", cond)
	write("Writer", cond)

	time.Sleep(4 * time.Second)
}
```

```bash
$ go run main.go
Writer starts writing
Writer wakes all
Reader 2 starts reading
Reader 3 starts reading
Reader 1 starts reading
```

As we can see, the readers were suspended using the `Wait` method until the writer used the `Broadcast` method to wake up the process.

## Once

Once ensures that only one execution will be carried out even among several goroutines.

### Usage

Unlike other primitives, `sync.Once` only has a single method:

- `Do(f func())` calls the function `f` **only once**. If `Do` is called multiple times, only the first call will invoke the function `f`.

### Example

This seems pretty straightforward, let's take an example:

```go
package main

import (
	"fmt"
	"sync"
)

func main() {
	var count int

	increment := func() {
		count++
	}

	var once sync.Once

	var increments sync.WaitGroup
	increments.Add(100)

	for i := 0; i < 100; i++ {
		go func() {
			defer increments.Done()
			once.Do(increment)
		}()
	}

	increments.Wait()
	fmt.Printf("Count is %d\n", count)
}
```

```bash
$ go run main.go
Count is 1
```

As we can see, even when we ran 100 goroutines, the count only got incremented once.

## Pool

Pool is s a scalable pool of temporary objects and is also concurrency safe. Any stored value in the pool can be deleted at any time without receiving notification. In addition, under high load, the object pool can be dynamically expanded, and when it is not used or the concurrency is not high, the object pool will shrink.

_The key idea is the reuse of objects to avoid repeated creation and destruction, which will affect the performance._

### But why do we need it?

Pool's purpose is to cache allocated but unused items for later reuse, relieving pressure on the garbage collector. That is, it makes it easy to build efficient, thread-safe free lists. However, it is not suitable for all free lists.

The appropriate use of a Pool is to manage a group of temporary items silently shared among and potentially reused by concurrent independent clients of a package. Pool provides a way to spread the cost of allocation overhead across many clients.

_It is important to note that Pool also has its performance cost. It is much slower to use `sync.Pool` than simple initialization. Also, a Pool must not be copied after first use._

### Usage

`sync.Pool` gives us the following methods:

- `Get()` selects an arbitrary item from the Pool, removes it from the Pool, and returns it to the caller.
- `Put(x any)` adds the item to the pool.

### Example

Now, let's look at an example.

First, we will create a new `sync.Pool`, where we can optionally specify a function to generate a value when we call, `Get`, otherwise it will return a `nil` value.

```go
package main

import (
	"fmt"
	"sync"
)

type Person struct {
	Name string
}

var pool = sync.Pool{
	New: func() any {
		fmt.Println("Creating a new person...")
		return &Person{}
	},
}

func main() {
	person := pool.Get().(*Person)
	fmt.Println("Get object from sync.Pool for the first time:", person)

	fmt.Println("Put the object back in the pool")
	pool.Put(person)

	person.Name = "Gopher"
	fmt.Println("Set object property name:", person.Name)

	fmt.Println("Get object from pool again (it's updated):", pool.Get().(*Person))
	fmt.Println("There is no object in the pool now (new one will be created):", pool.Get().(*Person))
}
```

And if we run this, we'll see an interesting output:

```bash
$ go run main.go
Creating a new person...
Get object from sync.Pool for the first time: &{}
Put the object back in the pool
Set object property name: Gopher
Get object from pool again (it's updated): &{Gopher}
Creating a new person...
There is no object in the pool now (new one will be created): &{}
```

_Notice how we did [type assertion](https://karanpratapsingh.com/courses/go/interfaces#type-assertion) when we call `Get`._

It can be seen that the `sync.Pool` is strictly a temporary object pool, which is suitable for storing some temporary objects that will be shared among goroutines.

## Map

Map is like the standard `map[any]any` but is safe for concurrent use by multiple goroutines without additional locking or coordination. Loads, stores, and deletes are spread over constant time.

### But why do we need it?

The Map type is _specialized_. Most code should use a plain Go map instead, with separate locking or coordination, for better type safety and to make it easier to maintain other invariants along with the map content.

The Map type is optimized for two common use cases:

- When the entry for a given key is only ever written once but read many times, as in caches that only grow.
- When multiple goroutines read, write, and overwrite entries for disjoint sets of keys. In these two cases, the use of a `sync.Map` may significantly reduce lock contention compared to a Go map paired with a separate `Mutex` or `RWMutex`.

_The zero Map is empty and ready for use. A Map must not be copied after first use._

## Usage

`sync.Map` gives us the following methods:

- `Delete()` deletes the value for a key.
- `Load(key any)` returns the value stored in the map for a key, or nil if no value is present.
- `LoadAndDelete(key any)` deletes the value for a key, returning the previous value if any. The loaded result reports whether the key was present.
- `LoadOrStore(key, value any)` returns the existing value for the key if present. Otherwise, it stores and returns the given value. The loaded result is true if the value was loaded, and false if stored.
- `Store(key, value any)` sets the value for a key.
- `Range(f func(key, value any) bool)` calls `f` sequentially for each key and value present in the map. If `f` returns false, the range stops the iteration.

_Note: Range does not necessarily correspond to any consistent snapshot of the Map's contents._

## Example

Let's look at an example. Here, we will launch a bunch of goroutines that will add and retrieve values from our map concurrently.

```go
package main

import (
	"fmt"
	"sync"
)

func main() {
	var wg sync.WaitGroup
	var m sync.Map

	wg.Add(10)
	for i := 0; i <= 4; i++ {
		go func(k int) {
			v := fmt.Sprintf("value %v", k)

			fmt.Println("Writing:", v)
			m.Store(k, v)
			wg.Done()
		}(i)
	}

	for i := 0; i <= 4; i++ {
		go func(k int) {
			v, _ := m.Load(k)
			fmt.Println("Reading: ", v)
			wg.Done()
		}(i)
	}

	wg.Wait()
}
```

As expected, our store and retrieve operation will be safe for concurrent use.

```bash
$ go run main.go
Reading: <nil>
Writing: value 0
Writing: value 1
Writing: value 2
Writing: value 3
Writing: value 4
Reading: value 0
Reading: value 1
Reading: value 2
Reading: value 3
```

## Atomic

Package atomic provides low-level atomic memory primitives for integers and pointers that are useful for implementing synchronization algorithms.

### Usage

`atomic` package provides [several functions](https://pkg.go.dev/sync/atomic#pkg-functions) which do the following 5 operations for `int`, `uint`, and `uintptr` types:

- Add
- Load
- Store
- Swap
- Compare and Swap

### Example

We won't be able to cover all of the functions here. So, let's take a look at the most commonly used function like `AddInt32` to get an idea.

```go
package main

import (
  "fmt"
	"sync"
	"sync/atomic"
)

func add(w *sync.WaitGroup, num *int32) {
	defer w.Done()
	atomic.AddInt32(num, 1)
}

func main() {
	var n int32 = 0
	var wg sync.WaitGroup

	wg.Add(1000)
	for i := 0; i < 1000; i = i + 1 {
		go add(&wg, &n)
	}

	wg.Wait()

	fmt.Println("Result:", n)
}
```

Here, `atomic.AddInt32` guarantees that the result of `n` will be 1000 as the instruction execution of atomic operations cannot be interrupted.

```bash
go run main.go
Result: 1000
```

# Advanced Concurrency Patterns

In this tutorial, we will discuss some advanced concurrency patterns in Go. Often, these patterns are used in combination in the real world.

## Generator

![generator](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/advanced-concurrency-patterns/generator.png)

Then generator Pattern is used to generate a sequence of values which is used to produce some output.

In our example, we have a `generator` function that simply returns a channel from which we can read the values.

This works on the fact that _sends_ and _receives_ block until both the sender and receiver are ready. This property allowed us to wait until the next value is requested.

```go
package main

import "fmt"

func main() {
	ch := generator()

	for i := 0; i < 5; i++ {
		value := <-ch
		fmt.Println("Value:", value)
	}
}

func generator() <-chan int {
	ch := make(chan int)

	go func() {
		for i := 0; ; i++ {
			ch <- i
		}
	}()

	return ch
}
```

If we run this, we'll notice that we can consume values that were produced on demand.

```bash
$ go run main.go
Value: 0
Value: 1
Value: 2
Value: 3
Value: 4
```

_This is a similar behavior as `yield` in JavaScript and Python._

## Fan-in

![fan-in](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/advanced-concurrency-patterns/fan-in.png)

The fan-in pattern combines multiple inputs into one single output channel. Basically, we multiplex our inputs.

In our example, we create the inputs `i1` and `i2` using the `generateWork` function. Then we use our [variadic function](https://karanpratapsingh.com/courses/go/functions#variadic-functions) `fanIn` to combine values from these inputs to a single output channel from which we can consume values.

_Note: order of input will not be guaranteed._

```go
package main

import (
	"fmt"
	"sync"
)

func main() {
	i1 := generateWork([]int{0, 2, 6, 8})
	i2 := generateWork([]int{1, 3, 5, 7})

	out := fanIn(i1, i2)

	for value := range out {
		fmt.Println("Value:", value)
	}
}

func fanIn(inputs ...<-chan int) <-chan int {
	var wg sync.WaitGroup
	out := make(chan int)

	wg.Add(len(inputs))

	for _, in := range inputs {
		go func(ch <-chan int) {
			for {
				value, ok := <-ch

				if !ok {
					wg.Done()
					break
				}

				out <- value
			}
		}(in)
	}

	go func() {
		wg.Wait()
		close(out)
	}()

	return out
}

func generateWork(work []int) <-chan int {
	ch := make(chan int)

	go func() {
		defer close(ch)

		for _, w := range work {
			ch <- w
		}
	}()

	return ch
}
```

```bash
$ go run main.go
Value: 0
Value: 1
Value: 2
Value: 6
Value: 8
Value: 3
Value: 5
Value: 7
```

## Fan-out

![fan-out](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/advanced-concurrency-patterns/fan-out.png)

Fan-out patterns allow us to essentially split our single input channel into multiple output channels. This is a useful pattern to distribute work items into multiple uniform actors.

In our example, we break the input channel into 4 different output channels. For a dynamic number of outputs, we can merge outputs into a shared _"aggregate"_ channel and use `select`.

_Note: fan-out pattern is different from pub/sub._

```go
package main

import "fmt"

func main() {
	work := []int{1, 2, 3, 4, 5, 6, 7, 8}
	in := generateWork(work)

	out1 := fanOut(in)
	out2 := fanOut(in)
	out3 := fanOut(in)
	out4 := fanOut(in)

	for range work {
		select {
		case value := <-out1:
			fmt.Println("Output 1 got:", value)
		case value := <-out2:
			fmt.Println("Output 2 got:", value)
		case value := <-out3:
			fmt.Println("Output 3 got:", value)
		case value := <-out4:
			fmt.Println("Output 4 got:", value)
		}
	}
}

func fanOut(in <-chan int) <-chan int {
	out := make(chan int)

	go func() {
		defer close(out)

		for data := range in {
			out <- data
		}
	}()

	return out
}

func generateWork(work []int) <-chan int {
	ch := make(chan int)

	go func() {
		defer close(ch)

		for _, w := range work {
			ch <- w
		}
	}()

	return ch
}
```

As we can see, our work has been split between multiple goroutines.

```bash
$ go run main.go
Output 1 got: 1
Output 2 got: 3
Output 4 got: 4
Output 1 got: 5
Output 3 got: 2
Output 3 got: 6
Output 3 got: 7
Output 1 got: 8
```

## Pipeline

![pipeline](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/advanced-concurrency-patterns/pipeline.png)

The pipeline pattern is a series of _stages_ connected by channels, where each stage is a group of goroutines running the same function.

In each stage, the goroutines:

- Receive values from _upstream_ via _inbound_ channels.
- Perform some function on that data, usually producing new values.
- Send values _downstream_ via _outbound_ channels.

Each stage has any number of inbound and outbound channels, except the first and last stages, which have only outbound or inbound channels, respectively. The first stage is sometimes called the _source_ or _producer_; the last stage is the _sink_ or _consumer_.

By using a pipeline, we separate the concerns of each stage, which provides numerous benefits such as:

- Modify stages independent of one another.
- Mix and match how stages are combined independently of modifying the stage.

In our example, we have defined three stages, `filter`, `square`, and `half`.

```go
package main

import (
	"fmt"
	"math"
)

func main() {
	in := generateWork([]int{0, 1, 2, 3, 4, 5, 6, 7, 8})

	out := filter(in) // Filter odd numbers
	out = square(out) // Square the input
	out = half(out)   // Half the input

	for value := range out {
		fmt.Println(value)
	}
}

func filter(in <-chan int) <-chan int {
	out := make(chan int)

	go func() {
		defer close(out)

		for i := range in {
			if i%2 == 0 {
				out <- i
			}
		}
	}()

	return out
}

func square(in <-chan int) <-chan int {
	out := make(chan int)

	go func() {
		defer close(out)

		for i := range in {
			value := math.Pow(float64(i), 2)
			out <- int(value)
		}
	}()

	return out
}

func half(in <-chan int) <-chan int {
	out := make(chan int)

	go func() {
		defer close(out)

		for i := range in {
			value := i / 2
			out <- value
		}
	}()

	return out
}

func generateWork(work []int) <-chan int {
	ch := make(chan int)

	go func() {
		defer close(ch)

		for _, w := range work {
			ch <- w
		}
	}()

	return ch
}
```

Seem like our input was processed correctly by the pipeline in a concurrent manner.

```bash
$ go run main.go
0
2
8
18
32
```

## Worker Pool

![worker-pool](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/advanced-concurrency-patterns/worker-pool.png)

The worker pool is a really powerful pattern that lets us distributes the work across multiple workers (goroutines) concurrently.

In our example, we have a `jobs` channel to which we will send our jobs and a `results` channel where our workers will send the results once they've finished doing the work.

After that, we can launch our workers concurrently and simply receive the results from the `results` channel.

_Ideally, `totalWorkers` should be set to `runtime.NumCPU()` which gives us the number of logical CPUs usable by the current process._

```go
package main

import (
	"fmt"
	"sync"
)

const totalJobs = 4
const totalWorkers = 2

func main() {
	jobs := make(chan int, totalJobs)
	results := make(chan int, totalJobs)

	for w := 1; w <= totalWorkers; w++ {
		go worker(w, jobs, results)
	}

	// Send jobs
	for j := 1; j <= totalJobs; j++ {
		jobs <- j
	}

	close(jobs)

	// Receive results
	for a := 1; a <= totalJobs; a++ {
		<-results
	}

	close(results)
}

func worker(id int, jobs <-chan int, results chan<- int) {
	var wg sync.WaitGroup

	for j := range jobs {
		wg.Add(1)

		go func(job int) {
			defer wg.Done()

			fmt.Printf("Worker %d started job %d\n", id, job)

			// Do work and send result
			result := job * 2
			results <- result

			fmt.Printf("Worker %d finished job %d\n", id, job)
		}(j)
	}

	wg.Wait()
}
```

As expected, our jobs were distributed among our workers.

```bash
$ go run main.go
Worker 2 started job 4
Worker 2 started job 1
Worker 1 started job 3
Worker 2 started job 2
Worker 2 finished job 1
Worker 1 finished job 3
Worker 2 finished job 2
Worker 2 finished job 4
```

## Queuing

![queuing](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/go/chapter-IV/advanced-concurrency-patterns/queuing.png)

Queuing pattern allows us to process `n` number of items at a time.

In our example, we use a buffered channel to simulate a queue behavior. We simply send an [empty struct](https://karanpratapsingh.com/courses/go/structs#properties) to our `queue` channel and wait for it to be released by the previous process so that we can continue.

This is because _sends_ to a buffered channel block only when the buffer is full and _receives_ block when the buffer is empty.

Here, we have total work of 10 items and we have a limit of 2. This means we can process 2 items at a time.

_Notice how our `queue` channel is of type `struct{}` as an empty struct occupies zero bytes of storage._

```go
package main

import (
	"fmt"
	"sync"
	"time"
)

const limit = 2
const work = 10

func main() {
	var wg sync.WaitGroup

	fmt.Println("Queue limit:", limit)
	queue := make(chan struct{}, limit)

	wg.Add(work)

	for w := 1; w <= work; w++ {
		process(w, queue, &wg)
	}

	wg.Wait()

	close(queue)
	fmt.Println("Work complete")
}

func process(work int, queue chan struct{}, wg *sync.WaitGroup) {
	queue <- struct{}{}

	go func() {
		defer wg.Done()

		time.Sleep(1 * time.Second)
		fmt.Println("Processed:", work)

		<-queue
	}()
}
```

If we run this, we will notice that it briefly pauses when every 2nd item (which is our limit) is processed as our queue waits to be dequeued.

```bash
$ go run main.go
Queue limit: 2
Processed: 1
Processed: 2
Processed: 4
Processed: 3
Processed: 5
Processed: 6
Processed: 8
Processed: 7
Processed: 9
Processed: 10
Work complete
```

## Additional patterns

Some additional patterns that might be useful to know:

- Tee channel
- Bridge channel
- Ring buffer channel
- Bounded parallelism

# Context

In concurrent programs, it's often necessary to preempt operations because of timeouts, cancellations, or failure of another portion of the system.

The `context` package makes it easy to pass request-scoped values, cancellation signals, and deadlines across API boundaries to all the goroutines involved in handling a request.

## Types

Let's discuss some core types of the `context` package.

### Context

The `Context` is an `interface` type that is defined as follows:

```go
type Context interface {
	Deadline() (deadline time.Time, ok bool)
	Done() <-chan struct{}
	Err() error
	Value(key any) any
}
```

The `Context` type has the following methods:

- `Done() <- chan struct{}` returns a channel that is closed when the context is canceled or times out. Done may return `nil` if the context can never be canceled.
- `Deadline() (deadline time.Time, ok bool)` returns the time when the context will be canceled or timed out. Deadline returns `ok` as `false` when no deadline is set.
- `Err() error` returns an error that explains why the Done channel was closed. If Done is not closed yet, it returns `nil`.
- `Value(key any) any` returns the value associated with the key or `nil` if none.

### CancelFunc

A `CancelFunc` tells an operation to abandon its work and it does not wait for the work to stop. If it is called by multiple goroutines simultaneously, after the first call, subsequent calls to a `CancelFunc` do nothing.

```go
type CancelFunc func()
```

## Usage

Let's discuss functions that are exposed by the `context` package:

### Background

Background returns a non-nil, empty `Context`. It is never canceled, has no values, and has no deadline.

_It is typically used by the main function, initialization, and tests, and as the top-level Context for incoming requests._

```go
func Background() Context
```

### TODO

Similar to the `Background` function `TODO` function also returns a non-nil, empty `Context`.

However, it should only be used when we are not sure what context to use or if the function has not been updated to receive a context. This means we plan to add context to the function in the future.

```go
func TODO() Context
```

### WithValue

This function takes in a context and returns a derived context where the value `val` is associated with `key` and flows through the context tree with the context.

This means that once you get a context with value, any context that derives from this gets this value.

_It is not recommended to pass in critical parameters using context values, instead, functions should accept those values in the signature making it explicit._

```go
func WithValue(parent Context, key, val any) Context
```

**Example**

Let's take a simple example to see how we can add a key-value pair to the context.

```go
package main

import (
	"context"
	"fmt"
)

func main() {
	processID := "abc-xyz"

	ctx := context.Background()
	ctx = context.WithValue(ctx, "processID", processID)

	ProcessRequest(ctx)
}

func ProcessRequest(ctx context.Context) {
	value := ctx.Value("processID")
	fmt.Printf("Processing ID: %v", value)
}
```

And if we run this, we'll see the `processID` being passed via our context.

```bash
$ go run main.go
Processing ID: abc-xyz
```

### WithCancel

This function creates a new context from the parent context and derived context and the cancel function. The parent can be a `context.Background` or a context that was passed into the function.

Canceling this context releases resources associated with it, so the code should call cancel as soon as the operations running in this context is completed.

_Passing around the `cancel` function is not recommended as it may lead to unexpected behavior._

```go
func WithCancel(parent Context) (ctx Context, cancel CancelFunc)
```

### WithDeadline

This function returns a derived context from its parent that gets canceled when the deadline exceeds or the cancel function is called.

For example, we can create a context that will automatically get canceled at a certain time in the future and pass that around in child functions. When that context gets canceled because of the deadline running out, all the functions that got the context gets notified to stop work and return.

```go
func WithDeadline(parent Context, d time.Time) (Context, CancelFunc)
```

### WithTimeout

This function is just a wrapper around the `WithDeadline` function with the added timeout.

```go
func WithTimeout(parent Context, timeout time.Duration) (Context, CancelFunc) {
	return WithDeadline(parent, time.Now().Add(timeout))
}
```

## Example

Let's look at an example to solidify our understanding of the context.

In the example below, we have a simple HTTP server that handles a request.

```go
package main

import (
	"fmt"
	"net/http"
	"time"
)

func handleRequest(w http.ResponseWriter, req *http.Request) {
	fmt.Println("Handler started")
	context := req.Context()

	select {
	// Simulating some work by the server, waits 5 seconds and then responds.
	case <-time.After(5 * time.Second):
		fmt.Fprintf(w, "Response from the server")

	// Handling request cancellation
	case <-context.Done():
		err := context.Err()
		fmt.Println("Error:", err)
	}

	fmt.Println("Handler complete")
}

func main() {
	http.HandleFunc("/request", handleRequest)

	fmt.Println("Server is running...")
	http.ListenAndServe(":4000", nil)
}
```

Let's open two terminals. In terminal one we'll run our example.

```bash
$ go run main.go
Server is running...
Handler started
Handler complete
```

In the second terminal, we will simply make a request to our server. And if we wait for 5 seconds, we get a response back.

```bash
$ curl localhost:4000/request
Response from the server
```

Now, let's see what happens if we cancel the request before it completes.

_Note: we can use `ctrl + c` to cancel the request midway._

```bash
$ curl localhost:4000/request
^C
```

And as we can see, we're able to detect the cancellation of the request because of the request context.

```bash
$ go run main.go
Server is running...
Handler started
Error: context canceled
Handler complete
```

I'm sure you can already see how this can be immensely useful.

For example, we can use this to cancel any resource-intensive work if it's no longer needed or has exceeded the deadline or a timeout.

# Next Steps

Congratulations, you've finished the course!

Now that you know the fundamentals of Go, here are some additional things for you to try:

- [Build a REST API with Go - For Beginners](https://www.youtube.com/watch?v=bFYZrEuEDLE)
- [Connecting to PostgreSQL using GORM](https://www.youtube.com/watch?v=Yk5ZjKq4qDQ)
- [Web Scraping with Go](https://www.youtube.com/watch?v=sU_BwzOxl54)
- [Dockerize your Go app](https://www.youtube.com/watch?v=zUc2LihXjlw)
- [DevOps Roadmap](https://www.youtube.com/watch?v=np_seazJL3Q)

I hope this course was a great learning experience. I would love to hear feedback from you.

Wishing you all the best for further learning!

# References

Here are the resources that were referenced while creating this course.

- [The Go Programming Language](https://www.gopl.io)
- [Official Go documentation](https://go.dev/doc)
- [Official Go blog](https://go.dev/blog)
- [A Tour of Go](https://go.dev/tour)
- [Learn Go with Tests](https://quii.gitbook.io/learn-go-with-tests)
