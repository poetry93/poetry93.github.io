---
title: 年终技术分享总结
date: 2018-02-03 15:35:08
tags: 
  - 总结
  - 思考
categories: 分享总结
---

## 一、JS应用领域、ES6特性

### 1.1 JavaScript的应用领域

> 首先很遗憾的一点是，“PHP虽然是最好的语言”，但是它不是最流行的语言

- 我们先来看一下`2017`年`GitHub`上最流行的`15`种编程语言排行榜
- 这个数据是 `GitHub` 根据过去 `12` 月提交的`PR` 数量来排名的，虽然不完全准确，但是 `PR `起码代表了项目的热度与欢迎度

![2017 GitHub 上最受欢迎的前 15 门语言](http://7xq6al.com1.z0.glb.clouddn.com/rank.jpeg)

#### 1.1.1 数据可视化

- 以`Processing`作为可视化的语言——它起始于2001年，它最初是面向美术工作者和设计者创建的，后来变成了全面的设计和原型工具，可以用于创建复杂数据可视化领域
- `Processing`被带入了到`Web`领域产生了`Processing.js`，还出现了`D3.js`

<!--more-->

#### 1.1.2 移动端应用 Cordova

> 接着就是`PhoneGap`（今天的`Cordova`），将`WebView`带向了移动应用，也将`JavaScript`带向了移动应用

![Cordova](http://7xq6al.com1.z0.glb.clouddn.com/Cordova.png)
> 使用`Cordova`，可以让我们一次开发多平台发布。我们也顺便提一下`Ionic`，作为混合应用的翘楚

![ionic](http://7xq6al.com1.z0.glb.clouddn.com/ionic.jpg)


#### 1.1.3 移动端应用 React Native

> 既然我们已经提到了`Cordova`，那么我们也应该说说`React Native`。也是一次开发多次运行。虽然它的坑还有很多，但是还是值得期待的

![native](http://7xq6al.com1.z0.glb.clouddn.com/react-native.png)

#### 1.1.4 服务端 Node.js

> 正是`V8`的性能将`JavaScript`带到了一个新的高度，于是`Node.js`诞生了——前端、后台都可以用`JavaScript`，一个`JavaScript`的全栈时代

- `Mongodb`作为数据库，`Express`作为`Server`端`MVC`，他们可以提供一个`RESTful`服务

![mean](http://7xq6al.com1.z0.glb.clouddn.com/mean.png)

#### 1.1.5 桌面应用 NW.js 和 Electron

-  `NW.js` 是基于 `Chromium` 和 `Node.js` 运行的， 它们可以让我们用`HTML`和`JavaScript`来制作桌面应用。除了`NW.js`还有最近比较火的`Electron`，`Atom`编辑器的
- 与`Cordova`的多平台构建多版本不同的是，`Electron`可以在一个平台上构建多个平台的应用。即我们可以在`Mac OS`上打包出`Linux`和`Windows`上的应用，而不需要在`Windows`再编译一次。
- 带向了桌面端，让桌面和`Web`保持了一致。最成功的案例就是估值达30亿美元的`Slack`

![slack](http://7xq6al.com1.z0.glb.clouddn.com/slack.jpg)


#### 1.1.6 游戏

- 自从`WebGL`被带入浏览器的那一刻，就决定了这又是一个新的天地
- 让我们忘记编译、启动更新、外挂等等的问题，并且我们还可以一次开发直接运行

![html5-games](http://7xq6al.com1.z0.glb.clouddn.com/html5-games.jpg)

#### 1.1.7 VR

- 主要思想还是通过`WebView`来渲染`VR`视角
- 并且各浏览器产商各在推进`WebVR `为虚拟现实设备显示提供支持

![threejs-oculus](http://7xq6al.com1.z0.glb.clouddn.com/threejs-oculus.jpeg)


#### 1.1.8 AR

- 虽然大部分的`AR`应用可能离我们有点远，但是离我们最近的就是`Leap Motion`——它可以利用手掌和手指动作来进行输入，但无需手部接触或者触摸
- 同理于`VR`，读取传感器的数据，再将其手势交由浏览器端来处理

![ar](http://7xq6al.com1.z0.glb.clouddn.com/ar.jpg)

#### 1.1.9 硬件

> 早先看到了`Arduino`在编译的时候，以`DSL`的方式封装了`API`。而`NodeMCU`则内建了`Lua`语言的支持，可以让开始者使用`Lua`来开始。 而`Tessel` 原生就提供了`JavaScript`运行环境，我们写需要写好`JavaScript`就可以在上面运行

- `Tessel 2`属于配置比较高的硬件
- 三星设计了`JerryScript`引擎，它能够运行在小于`64KB`内存上，且全部代码能够存储在不足`200KB`的只读存储（`ROM`）上

![iotjs](http://7xq6al.com1.z0.glb.clouddn.com/iotjs.png)

#### 1.1.10 物联网

- 上面说到的只是`Node.js`在`Web`中的应用，而物联网和`Web`的很大不同之处在于，物联网可以使用各种不同的协议，而这些协议都需要`Node.js`对其的支持。
- 因此，如果我们需要开始`Web`版、移动应用，那么我们自然更需要其作为后台

![lot](http://7xq6al.com1.z0.glb.clouddn.com/lot.png)

#### 1.1.11 操作系统界面

- 虽然更好的机器带来了更好的性能，但是显然人们对于原生应用的需求并没有那么强烈。`Firefox OS`已经在移动操作系统败下阵来，但是这个操作被带到了物联网领域
- 这就意味着，我们可以使用`JavaScript`来开发操作系统的界面了

![firefox-os](http://7xq6al.com1.z0.glb.clouddn.com/firefox-os.jpg)

### 1.2 ES6的一些特性

![es](http://7xq6al.com1.z0.glb.clouddn.com/es.png)

> `ECMAScript 6（以下简称ES6）`是`JavaScript`语言的下一代标准。因为当前版本的`ES6`是在`2015`年发布的，所以又称`ECMAScript 2015`。也就是说，`ES6`就是`ES2015`

- 虽然目前并不是所有浏览器都能兼容`ES6`全部特性，但越来越多的程序员在实际项目当中已经开始使用`ES6`了
- 在我们正式讲解`ES6`语法之前，我们得先了解下`Babel`

> `Babel`是一个广泛使用的`ES6`转码器，可以将`ES6`代码转为`ES5`代码，从而在现有环境执行。大家可以选择自己习惯的工具来使用使用`Babel`，具体过程可直接在`Babel`[官网](https://babeljs.io/)查看

**最常用的`ES6`特性**


#### 1.2.1 let, const

> 这两个的用途与`var`类似，都是用来声明变量的，但在实际运用中他俩都有各自的特殊用途

```javascript
var name = 'b'

while (true) {
    var name = 'a'
    console.log(name)  //a
    break
}

console.log(name)  //a
```

> 使用`var` 两次输出都是`a`，这是因为`ES5`只有全局作用域和函数作用域，没有块级作用域，这带来很多不合理的场景。第一种场景就是你现在看到的内层变量覆盖外层变量。而`let`则实际上为`JavaScript`新增了块级作用域。用它所声明的变量，只在`let`命令所在的代码块内有效

```javascript
let name = 'b'

while (true) {
    let name = 'a'
    console.log(name)  //a
    break
}

console.log(name)  //b
```

- 另外一个var带来的不合理场景就是用来计数的循环变量泄露为全局变量，看下面的例子

```javascript
var a = [];
for (var i = 0; i < 10; i++) {
  a[i] = function () {
    console.log(i);
  };
}
a[6](); // 10
```

- 上面代码中，变量`i`是`var`声明的，在全局范围内都有效。所以每一次循环，新的i值都会覆盖旧值，导致最后输出的是最后一轮的i的值。而使用`let`则不会出现这个问题

```javascript
var a = [];
for (let i = 0; i < 10; i++) {
  a[i] = function () {
    console.log(i);
  };
}
a[6](); // 6
```

#### 1.2.2 class, extends, super

> - 这三个特性涉及了`ES5`中最令人头疼的的几个部分：原型、构造函数，继承...你还在为它们复杂难懂的语法而烦恼吗？你还在为指针到底指向哪里而纠结万分吗？有了`ES6`我们不再烦恼！
> - `ES6`提供了更接近传统语言的写法，引入了`Class`（类）这个概念。新的`class`写法让对象原型的写法更加清晰、更像面向对象编程的语法，也更加通俗易懂

```javascript
class Animal {
    constructor(){
        this.type = 'animal'
    }
    says(say){
        console.log(this.type + ' says ' + say)
    }
}

let animal = new Animal()
animal.says('hello') //animal says hello

class Cat extends Animal {
    constructor(){
        super()
        this.type = 'cat'
    }
}

let cat = new Cat()
cat.says('hello') //cat says hello
```

- 上面代码首先用`class`定义了一个“类”，可以看到里面有一个`constructor`方法，这就是构造方法，而`this`关键字则代表实例对象。简单地说，`constructor`内定义的方法和属性是实例对象自己的，而`constructor`外定义的方法和属性则是所有实例对象可以共享的
- `Class`之间可以通过`extends`关键字实现继承，这比`ES5`的通过修改原型链实现继承，要清晰和方便很多。上面定义了一个`Cat`类，该类通过`extends`关键字，继承了`Animal`类的所有属性和方法
- `super`关键字，它指代父类的实例（即父类的`this`对象）。子类必须在`constructor`方法中调用`super`方法，否则新建实例时会报错。这是因为子类没有自己的this对象，而是继承父类的`this`对象，然后对其进行加工。如果不调用super方法，子类就得不到`this`对象
- `ES6`的继承机制，实质是先创造父类的实例对象`this`（所以必须先调用`super`方法），然后再用子类的构造函数修改`this`
- 以上三个东西在最新版`React`中出现得很多。创建的每个`component`都是一个继承`React.Component`的类

#### 1.2.3 arrow function

> `ES6`最最常用的一个新特性了，用它来写`function比原来的写法要简洁清晰很多

```javascript
function(i){ return i + 1; } //ES5
(i) => i + 1 //ES6
```

> 如果方程比较复杂，则需要用`{}`把代码包起来

```javascript
function(x, y) { 
    x++;
    y--;
    return x + y;
}
(x, y) => {x++; y--; return x+y}
```

#### 1.2.4 template string

> 当我们要插入大段的`html`内容到文档中时，传统的写法非常麻烦

- 可以先看下面一段代码

```javascript
$("#result").append(
  "There are <b>" + basket.count + "</b> " +
  "items in your basket, " +
  "<em>" + basket.onSale +
  "</em> are on sale!"
);
```

- 我们要用一堆的`'+'`号来连接文本与变量，而使用`ES6`的新特性模板字符串``后，我们可以直接这么来写

```javascript
$("#result").append(`
  There are <b>${basket.count}</b> items
   in your basket, <em>${basket.onSale}</em>
  are on sale!
`);
```

> 用反引号来标识起始，用`${}`来引用变量，而且所有的空格和缩进都会被保留在输出之中

- `React Router`从第`1.0.3`版开始也使用`ES6`语法了，比如这个例子

```javascript
<Link to={`/taco/${taco.name}`}>{taco.name}</Link>
```

#### 1.2.5 destructuring

> `ES6`允许按照一定模式，从数组和对象中提取值，对变量进行赋值，这被称为解构（`Destructuring`）

```javascript
let cat = 'ken'
let dog = 'lili'
let zoo = {cat: cat, dog: dog}
console.log(zoo)  //Object {cat: "ken", dog: "lili"}
```

- 用ES6完全可以像下面这么写

```javascript
let cat = 'ken'
let dog = 'lili'
let zoo = {cat, dog}
console.log(zoo)  //Object {cat: "ken", dog: "lili"}
```

- 反过来可以这么写

```javascript
let dog = {type: 'animal', many: 2}
let { type, many} = dog
console.log(type, many)   //animal 2
```

#### 1.2.6 default, rest

> `default`很简单，意思就是默认值。大家可以看下面的例子，调用`animal()`方法时忘了传参数，传统的做法就是加上这一句`type = type || 'cat' `来指定默认值

```javascript
function animal(type){
    type = type || 'cat'  
    console.log(type)
}
animal()
```

- 如果用`ES6`我们而已直接这么写

```javascript
function animal(type = 'cat'){
    console.log(type)
}
animal()
```

- 最后一个`rest(展开运算符)`语法也很简单，直接看例子

```javascript
function animals(...types){
    console.log(types)
}
animals('cat', 'dog', 'fish') //["cat", "dog", "fish"]
```

## 二、前端工程化浅析

### 2.1 前端工程化的历史模式演变

#### 2.1.1  Web 1.0 时代

![](http://7xq6al.com1.z0.glb.clouddn.com/web1.png)

>`Web 1.0` 时代，页面由 `JSP`、`PHP` 等工程师在服务端生成，浏览器负责展现。基本上是服务端给什么浏览器就展现什么，展现的控制在 `Web Server `层

- 这种模式的好处是：简单明快，本地起一个 `Tomcat` 或 `Apache` 就能开发，调试什么的都还好，只要业务不太复杂
- 然而业务的复杂会让 `Service`越来越多，调用关系变复杂，前端搭建本地环境不再是一件简单的事

> 如何让前后端分工更合理高效，如何提高代码的可维护性，在 `Web` 开发中很重要。下面我们继续来看技术架构的演变如何解决这两个问题

#### 2.1.2  后端为主的 MVC 时代

> 为了降低复杂度，以后端为出发点，有了 `Web Server` 层的架构升级，比如  `Spring MVC`，这是后端的 `MVC` 时代

![](http://7xq6al.com1.z0.glb.clouddn.com/mvc.png)

> 代码可维护性得到明显好转，`MVC` 是个非常好的协作模式，从架构层面让开发者懂得什么代码应该写在什么地方

#### 2.1.3  Ajax 带来的 SPA 时代(web2.0)

> `2004` 年 `Gmail `像风一样的女子来到人间，很快 `2005` 年 `Ajax` 正式提出，加上` CDN `开始大量用于静态资源存储，于是出现了 `JavaScript` 王者归来的 `SPA` （Single Page Application 单页面应用）时代

![](http://7xq6al.com1.z0.glb.clouddn.com/web2.png)

> 这种模式下，前后端的分工非常清晰，前后端的关键协作点是 `Ajax `接口。看起来是如此美妙，但回过头来看看的话，这与 `JSP` 时代区别不大。复杂度从服务端的 `JSP` 里移到了浏览器的 `JavaScript`，浏览器端变得很复杂。类似 `Spring MVC`，这个时代开始出现浏览器端的分层架构

![](http://7xq6al.com1.z0.glb.clouddn.com/spa.png)

**对于 SPA 应用，有几个很重要的挑战**

- **前后端接口的约定**
  - 有了和后端一起沉淀的接口规则，还可以用来模拟数据，使得前后端可以在约定接口后实现高效并行开发
- **前端开发的复杂度控制**
  - `SPA` 应用大多以功能交互型为主，`JavaScript` 代码过十万行很正常。大量 `JS` 代码的组织，与 `View` 层的绑定等，都不是容易的事情

> `SPA` 让前端看到了一丝绿色，但依旧是在荒漠中行走

####  2.1.4  前端为主的 MV* 时代

> 为了降低前端开发复杂度，除了 `Backbone`，还有大量框架涌现，比如 `EmberJS`、`KnockoutJS`、`AngularJS` 等。这些框架总的原则是先按类型分层，比如 `Templates`、`Controllers`、`Models`，然后再在层内做切分，如下图：

![](http://7xq6al.com1.z0.glb.clouddn.com/mvvm.png)


**这样做的好处**

- 前后端职责很清晰
  -  前端工作在浏览器端，后端工作在服务端。清晰的分工，可以让开发并行，测试数据的模拟不难，前端可以本地开发。后端则可以专注于业务逻辑的处理，输出 `RESTful` 等接口
- 前端开发的复杂度可控
  - 前端代码很重，但合理的分层，让前端代码能各司其职
- 部署相对独立，产品体验可以快速改进

**但依旧有不足之处**

- 代码不能复用。比如后端依旧需要对数据做各种校验，校验逻辑无法复用浏览器端的代码。如果可以复用，那么后端的数据校验可以相对简单化
- 全异步，对 `SEO` 不利。往往还需要服务端做同步渲染的降级方案
- 性能并非最佳，特别是移动互联网环境下
- `SPA` 不能满足所有需求，依旧存在大量多页面应用。`URL Design` 需要后端配合，前端无法完全掌控

#### 2.1.5  Node 带来的全栈时代

> 前端为主的 `MV*` 模式解决了很多问题，但如上所述，依旧存在不少不足之处。随着 `Node.js` 的兴起，`JavaScript` 开始有能力运行在服务端。这意味着可以有一种新的研发模式：

![](http://7xq6al.com1.z0.glb.clouddn.com/node.png)

**在这种研发模式下，前后端的职责很清晰。对前端来说，两个 UI 层各司其职**

- `Front-end UI layer` 处理浏览器层的展现逻辑。通过 `CSS `渲染样式，通过 `JavaScript` 添加交互功能，`HTML` 的生成也可以放在这层，具体看应用场景
- `Back-end UI layer` 处理路由、模板、数据获取、`cookie` 等。通过路由，前端终于可以自主把控 `URL Design`，这样无论是单页面应用还是多页面应用，前端都可以自由调控。后端也终于可以摆脱对展现的强关注，转而可以专心于业务逻辑层的开发。
- 通过 `Node`，`Web Server `层也是 `JavaScript`代码，这意味着部分代码可前后复用，需要 `SEO` 的场景可以在服务端同步渲染，由于异步请求太多导致的性能问题也可以通过服务端来缓解。前一种模式的不足，通过这种模式几乎都能完美解决掉。

**基于 Node 的全栈模式，依旧面临很多挑战**

- 需要前端对服务端编程有更进一步的认识。比如 `network/tcp` 等知识的掌握
- `Node` 层与` Java `层的高效通信。`Node` 模式下，都在服务器端，`RESTful HTTP` 通信未必高效，通过` SOAP` 等方式通信更高效

#### 2.1.6 总结

- 模式没有好坏高下之分，只有合不合适
- `Ajax` 给前端开发带来了一次质的飞跃，`Node` 很可能是第二次
- 上面种种模式，都是让前后端的职责更清晰，分工更合理高效
- 还有个原则，让合适的人做合适的事。比如 `Web Server` 层的 `UI Layer` 开发，前端是更合适的人选

### 2.2 什么是前端工程化

> 大体的来说，前端工程化有两层含义

**广义的前端工程化**

> 前端工程是软件工程的一个子类，指的是将软件工程的方法和原理运用在前端开发中, 目的是实现 高效开发，有效协同，质量可控

**狭义的前端工程化**

> 前端工程是指将 开发阶段 的代码转变成 生产环境 的代码的 一系列步骤。主要包括 构建 , 分支管理 , 自动化测试, 部署 等

**简单总结一下就是**

- 广义的前端工程是一个系统工程，需要从软件生命周期的各个方面入手，本质上属于管理科学的方法论
- 狭义的前端工程是前端开发流程中的一部分，本质上属于软件技术的范畴和开发的最佳实践。我们平时提到的前端，如果特别说明，一般指的就是狭义上的前端工程
- 具体到前端工程化，面临的问题是如何提高编码->测试->维护阶段的生产效率

### 2.3 为什么要提前端工程化

> 简单来说，前端越来越复杂，设计的问题和环节也越来越多，不采用工程化管理，就无法很好的实现团队协同和降低复杂性。 具体的原因大概有以下几点

**前端范畴不断扩大**

> 早期的前端只需要适配桌面浏览器，而现在的前端，需要适配不同类型和尺寸的设备，包括移动端网页，`app`应用等

**前后端分离**

> 早期的前端只是后端 `MVC` 框架的一层模块， 而现在的前端普遍是从后端接口获取数据，编写处理逻辑，各种前端`mvc`前端框架也层出不穷

**模块化开发的出现**

> 现在的前端开发不再是从零写起，重复造轮子，而是会引用大量内部和外部的组件和模块，这也导致前端必须进行模块管理

**转码器的盛行**

> 为了提高效率，前端工程往往不会直接写`html`,`css`,和`js`代码，而是改用其他格式书写，再用工具编译为目标格式。比如用`Jade` 写`HTML`，用`less`／`sass`／`stylus`编写`CSS`,用`ES6`/`Typescript`/.. 编写`JavaScript`.

**开发流程和团队**

> 早期的前端团队往往只有几个人，而现在的前端团队可以扩展到几十人，甚至上百人。每个人只负责自己的一块内容。所以，如何协调多人多团队的工作，保证沟通顺畅，保证权限管理，越来越成为一大问题

### 2.4 前端工程化的具体内容

- **代码规范**: 保证团队所有成员以同样的规范开发代码
- **分支管理**: 不同的开发人员开发不同的功能或组件，按照统一的流程合并到主干
- **模块管理**: 一方面，团队引用的模块应该是规范的;另一方面，必须保证这些模块可以正确的加入到最终编译好的包文件中
- **自动化测试**：为了保证和并进主干的代码达到质量标准，必须有测试，而且测试应该是自动化的，可以回归的
- **构建**：主干更新以后，自动将代码编译为最终的目标格式，并且准备好各种静态资源
- **部署**:  将构建好的代码部署到生产环境

### 2.5 前端工程化面临的问题

> 要解决前端工程化的问题，从两个角度入手：**开发**和**部署**

**从开发角度，要解决的问题包括**

 - 提高开发生产效率
 - 降低维护难度

**这两个问题的解决方案有两点**

- 制定开发规范，提高团队协作能力；
- 模块化开发

**从部署角度，要解决的问题主要是资源管理，包括**

- 代码审查
- 压缩打包
- 增量更新
- 单元测试

> 要解决上述问题，需要引入构建/编译阶段

### 2.6 构建&编译

> - 自`Node.js`问世以来，前端圈子一直传播着一个词：颠覆。前端工程师要借助`Node.js`颠覆以往的`web`开发模式，简单说就是用`Node.js`取代`php`、`ruby`、`python`等语言搭建`web server`
> - 催生了大量前端工程化工具（`Grunt`、`Gulp`、`Browserify`、`Webpack`、`Rollup`、`Parcel`.....)，提高了前端开发效率并使大型`Web`前端项目的开发更为方便和规范

> 我们首先看一下在整个前端工程系统中，构建扮演什么角色？请看下图

![build](http://7xq6al.com1.z0.glb.clouddn.com/build.png)


> 大前端体系下，前端开发人员掌握着`Node.js`搭建的`web server`层。不论是大前端还是“小”前端，构建阶段在两种模式下的作用完全一致，构建的作用就是对静态资源以及模板进行处理，换句话说：构建的核心是资源管理。

### 2.7 总结

**一个完整的前端工程体系应该包括**

- 统一的开发规范
- 组件化开发
- 构建流程

> - 开发规范和组件化开发面向的开发阶段，宗旨是提高团队协作能力，提高开发效率并降低维护成本
> - 构建工具和平台解决了`web`产品一系列的工程问题，旨在提高`web`产品的性能表现，提高开发效率


## 三、React实践

> 随着近几年的发展，前端已经不单单是`html+css`编写样式静态页了，而是往着更深层次发展，越来越多的前端`js`框架：`angular`、`vue`、`react`纷纷研发出来了。该如何选择？

### 3.1 选型对比

#### 3.1.1 过去一年的Google趋势分析

> 下图是进行了过去一年中国区的比较，这个结果是网页搜索的结果，对应颜色可以看到相应的折线图，`React`整体很高，`vue`第二，`angularjs`依旧占据很大份额

![trend](http://7xq6al.com1.z0.glb.clouddn.com/trend.png)

#### 3.1.2 React、Vue、angular优缺点对比

##### 3.1.2.1 React

**优点**

- `React`速度很快：它并不直接对`DOM`进行操作，引入了一个叫做虚拟`DOM`的概念，安插在`javascript`逻辑和实际的`DOM`之间，性能好
- 跨浏览器兼容：虚拟`DOM`帮助我们解决了跨浏览器问题，它为我们提供了标准化的`API`，甚至在`IE8`中都是没问题的
- 一切都是`component`：代码更加模块化，重用代码更容易，可维护性高
- 单向数据流：`Flux`是一个用于在`JavaScript`应用中创建单向数据层的架构，它随着`React`视图库的开发而被`Facebook`概念化
- 同构、纯粹的`javascript`：因为搜索引擎的爬虫程序依赖的是服务端响应而不是`JavaScript`的执行，预渲染你的应用有助于搜索引擎优化
- 兼容性好：比如使用`RequireJS`来加载和打包，而`Browserify`和`Webpack`适用于构建大型应用。它们使得那些艰难的任务不再让人望而生畏

**缺点**

- `React`本身只是一个`V`而已，并不是一个完整的框架，所以如果是大型项目想要一套完整的框架的话，基本都需要加上`ReactRouter`和`Flux`才能写大型应用
- 大多数坑没踩出来，大概就是现在还太新了很难说将来有没有大的`API`变化

##### 3.1.2.2 Angular

> `AngularJS`最近很火，追随者也很多。完全使用`JavaScript`编写的客户端技术。同其他历史悠久的`Web`技术（`HTML`、`CSS`和`JavaScript`）配合使用，使`Web`应用开发比以往更简单、更快捷“。当你学习它的时候，我相信你会被它的很多新特效所吸引

**优点**

- 是一个比较完善的前端`MVW`框架，包含模板，数据双向绑定，路由，模块化，服务，依赖注入等所有功能，模板功能强大丰富，并且是声明式的，自带了丰富的 `Angular` 指令。
- `AngularJS`有`Google`来维护，有了一个强大的后台，社区也非常活泼，能够很好促进它的发展

**缺点**

- 学习起来有难度，比较难理解一些
- `AngularJS2.0`和`1.0`相比，会把之前的推翻重写，两个框架的改变很大，基本是两个框架了，等于是说等到`2.0`出来后又需要从头开始

##### 3.1.2.3 Vue

> `Vue.js` 专注于 `MVVM` 模型的 `ViewModel` 层。它通过双向数据绑定把 `View` 层和 `Model` 层连接了起来。实际的 `DOM` 封装和输出格式都被抽象为了`Directives `和 `Filters`。`Vue.js`和其他库相比是一个小而美的库

![viewModel](http://7xq6al.com1.z0.glb.clouddn.com/view.png)

**优点**

- 简单：官方文档很清晰，比 `Angular` 简单易学
- 快速：异步批处理方式更新 `DOM`
- 组合：用解耦的、可复用的组件组合你的应用程序
- 对模块友好：可以通过 `NPM`安装，使用场景更加灵活

**缺点**

- 新生儿：`Vue.js`是一个新的项目，没有`angular`那么成熟
- 影响度不是很大：生态不是很完善
- 不支持`IE8`：不过`AngularJS 1.3`也抛弃了对`IE8`的支持。这一点对于那些需要支持`IE8`的项目就不好了

|Decision point|Angular2|React|Vue|
|---|---|---|---|---|
|稳定|`YES`|`YES`|`YES`|
|社区生态|完善,`Google`维护|大型的技术生态系统,`Facebook`维护|个人维护|
|文档是否全面|`YES`|`YES`|`YES`|
|学习曲线|很陡|一般|平缓|
|`Small`|`566K`|`139K`|`58.8K`|
|`Coding Speed`|`Slow`|`Normal`|`Fast`|
|是否使用`virtual DOM `||`YES`|`YES`|


### 3.2 在结算报表中的应用

#### 3.2.1 React概况

##### 3.2.1.1 概况

- `React` 起源于 `Facebook` 的内部项目，因为该公司对市场上所有 `JavaScript MVC` 框架，都不满意，就决定自己写一套。
- `React`是一个帮助构建页面`UI`的库，相较于`MVC`框架，只能算是其中的`View`层。能够帮助我们把页面分割成各个单独独立的小模块，每个小模块就是一个组件，这些组件相互组合、嵌套，就构成了复杂庞大的页面
- `React`只是一个库，不是一个框架，它只提供`UI`层的解决方案，在实际使用中需要搭配其他库实现完整的解决方案

**解决前端开发的那些痛点**

- .隔离`DOM`操作，所有操作全部转换成对数据的操作，通过改变数据来改变页面显示
- 数据绑定，单项数据流
- 组件化，`React`天生组件化，每个模块都是一个单独的组件，可以单独使用，也可以和其他模块组合、嵌套使用
- 可维护行增强，每个组件单独维护，互相不受牵扯
- 运行效率，使用虚拟`DOM`，减少`DOM`操作

##### 3.2.1.2 核心概念

> `React` 的核心概念只有 `2` 点

- 声明式渲染(`Declarative`)
- 基于组件(`Component-Based`)

**声明式渲染**

> 和普通模板不同的是，`React` 模板写在 `JS` 文件中，而不是 `html` 的 `<script>` 标签中。能使用所有 `JS` 语法，而不只有模板语法，所以更加灵活

```javascript
const formatName = user => user.firstName + ' ' + user.lastName;

// 数据
const user = {
  firstName: 'poetry',
  lastName: 'xie'
};

// 模板
const element = (
  <h1>
    Hello, {formatName(user)}!
  </h1>
);

// 渲染
ReactDOM.render(
  element,
  document.getElementById('root')
);
```

- `React` 可局部渲染，且只渲染改变了的数据

##### 3.2.1.3 生命周期

![life](http://7xq6al.com1.z0.glb.clouddn.com/life1.png)

#### 3.2.2 CRM项目整体结构

![crm架构图](http://7xq6al.com1.z0.glb.clouddn.com/crm.png)


#### 3.2.3 性能优化

##### 3.2.3.1 PureRenderMixin 优化

> `React` 最基本的优化方式是使用`PureRenderMixin`，安装工具 `npm i react-addons-pure-render-mixin --save`，然后在组件中引用并使用

```javascript
import React from 'react'
import PureRenderMixin from 'react-addons-pure-render-mixin'

class List extends React.Component {
    constructor(props) {
        super(props);
        this.shouldComponentUpdate = PureRenderMixin.shouldComponentUpdate.bind(this);
    }
    //...省略其他内容...
}
```

- 这里使用`this.shouldComponentUpdate = PureRenderMixin.shouldComponentUpdate.bind(this);`的意思是重写组件的`shouldComponentUpdate`函数，在每次更新之前判断`props`和`state`，如果有变化则返回`true`，无变化则返回`false`
- 因此，我们在开发过程中，在每个 `React`组件中都尽量使用`PureRenderMixin`

#### 3.2.4 一些坑

- 升级最新版的`react-router`写法的变更
- 使用`mobile-ant-design`组件库在`iphone`下出现兼容性问题

## 四、Chrome开发者工具介绍

### 4.1 如何查看修改DOM

#### 4.1.1 Elements面板的使用

> 你可能经常会想能直接在浏览器里更改网页的文本内容。答案是肯定的，你可以只通过一行简单的指令把`Chrome`变成所见即所得的编辑器，直接在网页上随心所欲地删改文字

- 打开`Chrome`的开发者控制台，输入

```javascript
document.body.contentEditable=true
```

#### 4.1.2 查看DOM树

> 打开`Element`面板，可以查看所有`DOM`节点，包括`CSS`和`JavaScript`，如下图所示，左侧为`DOM`树，右侧为`CSS`样式。

![dom](http://7xq6al.com1.z0.glb.clouddn.com/dom.png)

- 点击“图标1”，可以在新窗口中打开开发者工具，再次点击回到当前网页；
- 点击“图标2”，可以调出控制台，可以在控制台里输入并执行`JavaScript`代码，查看当前网页的错误和日志等；
- 点击“图标3”，可以选取当前页面的`HTML`元素

#### 4.1.3 选取DOM节点

![select-dom](http://7xq6al.com1.z0.glb.clouddn.com/select-dom.png)

#### 4.1.4 增加、删除和修改DOM节点

> 在`Element`面板中，选择`DOM`节点，在文本处右击鼠标，会弹出一个菜单，如下图所示

![add-dom](http://7xq6al.com1.z0.glb.clouddn.com/add-dom.png)



### 4.2 performance性能分析工具

> 我们都知道浏览器从打开 `url` 到整个页面渲染完成，中间的过程，大致是 `DOM` 解析，`CSSOM` 解析，`JS` 解析，渲染。

**切换至Performance标签**

![performance](http://7xq6al.com1.z0.glb.clouddn.com/per.png)

> 先来看看在 `Chrome` 浏览器控制台中执行 `window.performance` 会出现什么

![d](http://7xq6al.com1.z0.glb.clouddn.com/dd-co.png)

- `performance` 有好几个属性，但是由于浏览器支持程度不同，我们主要用到的是支持最广泛，最常用的 `performance.timing` 这个属性

> `performance.timing` 主要属性如下： 

这些属性记录的都是时间戳

```javascript
navigationStart: 1500979373880,    // 地址栏输入 url 回车之后，或者用户点击链接开始打开 href 时
unloadEventStart: 0,    // 前一个页面触发 unload 时间时，和当前页面同源时才统计
unloadEventEnd: 0,      // 前一个页面 unload 事件处理函数结束时，和当前页面同源时才统计
redirectStart: 0,       // 重新向到当前页面时，同源才统计
redirectEnd: 0,         // 重定向结束时，同源才统计
fetchStart: 1500979373880,    // 开始请求页面
domainLookupStart: 1500979373880,    // 开始解析域名，如果是本地有 DNS 缓存，或者使用 http-alive 复用 TCP 连接，则此属性值和 fetchStart 相同
domainLookupEnd: 1500979373880,    // 域名解析结束时，如果是本地有 DNS 缓存，或者使用 http-alive 复用 TCP 连接 ，则此属性值和 fetchStart 相同
connectStart: 1500979373886,       // 开始向服务器请求建立连接
secureConnectionStart: 0,          // 开始进行 SSL 连接，不走 HTTPS 这个属性值为0
connectEnd: 1500979373887,         // 连接建立完毕
requestStart: 1500979373887,       // 开始向服务器发起请求
responseStart: 1500979374433,      // 服务器开始响应请求
responseEnd: 1500979374540,        // 服务器可能会采用流式响应，或者分片传输。这个属性表示浏览器接收到完整页面的时刻
domLoading: 1500979374442,        // 开始解析 DOM, 此时 document.readyState 变成 loading
domInteractive: 1500979375806,    // DOM 树解析完成，此时 document.readyState 变成 interactive，可以在 JS 里面访问 DOM 了，但此时 JS 未必解析执行完毕了
domContentLoadedEventStart: 1500979375806,    // JS 也解析执行完了(不包括 async 加载的 JS)，触发 DOMContentLoaded 事件
domContentLoadedEventEnd: 1500979375827,      // DOMContentLoaded 事件结束
domComplete: 1500979376043,                   // 页面内资源全部加载完毕（比如图片、音视频），JS 解析完毕，此时 document.readyState 变为 complete
loadEventStart: 1500979376043,    // 触发 onload 事件
loadEventEnd:1500979376049        // onload 事件结束
```

> 拿到这些节点的时间戳之后，各个阶段的耗时就能知道了 

**当采样至一定的时间段后，点击暂停，浏览器会生成如下的图表**

 
![performance](http://7xq6al.com1.z0.glb.clouddn.com/performance.png)

- 区域 1 是一个缩略图，可以看到除了时间轴以外被上下分成了四块，分别代表 `FPS`、`CPU` 时间、网络通信时间、堆栈占用。这个缩略图可以横向缩放，白色区域是下面可以看到的时间段
- 区域 2 可以看一些交互事件，例如你滚动了一下页面，那么这里会出现一个 `scroll` 的线段，线段覆盖的范围就是滚动经过的时间
- 区域 3 则是具体的事件列表了
- 区域 4 是概览

> - 一开始没有记录的时候，所有的区域都是空的。开始统计和结束统计都很简单，左上角那坨黑色的圆圈就是。它右边那个长得像“禁止通行”的按钮是用来清除现有记录的。当有数据的时候，我们把鼠标滚轮向上滚，可以看到区域被放大了
> - 短短的时间里，浏览器做了这么多事情。对于一般的屏幕，原则上来说一秒要往屏幕上绘制` 60` 帧，所以理论上讲我们一帧内的计算时间不能超过 `16` 毫秒

- 不同的颜色表示不同的事件
  - 蓝色：网络通信和`HTML`解析
  - 黄色：`JavaScript`执行
  - 紫色：样式计算和布局，即重排
  - 绿色：重绘
  
 > 哪种色块比较多，就说明性能耗费在那里。色块越长，问题越大

**查看页面的重绘过程**

![render](http://7xq6al.com1.z0.glb.clouddn.com/render.png)

**简单提一下什么是回流重绘**

- 回流
 
> 当`render Tree`中的一部分或全部元素的规模尺寸、布局、隐藏等改变而需要重新构建，这称为回流（`reflow`）

- 重绘

> 当`render Tree`中的一些元素需要更新属性，而这些属性这是影响元素的风格，而不会影响布局的，比如`background-color`，则称为重绘（`repaint`）

回流必定会引起重绘，重绘不一定引起回流。这也是我们在写页面的时候关注的一些细节点。



### 4.3 前端存储能力

#### 4.3.1 LocalStorage、SessionStorage

> 客户端出于不同的原因，我们会存储一些相应的用户数据，如

- 在页面间共享数据——适用于同一个网站，页面间使用不同的框架
- 存储用户的 `token`——缓存在内存或者 `localstorage` 用于登录，在重要的操作时再验证权限
- 缓存数据，加快下次打开速度
- 临时保存用户未完成的表单
- 存储 `JavaScript` 代码，以加快打开速度

> 数据存储并不是一件很难的事。只需要

- 选择一个合适的存储介质
- 决定要存储的数据内容及形式
- 创建存储和读取接口

我们只需要想一个 `key`，再想一个 `value` 就可以保存这个值了，如 `localStorge` 的`setItem` 和 `getItem` 就可以轻松达到这个要求了。而对于常用的数据格式来说，加上个 `JSON.stringify` 来转换对象为字符 串，从 `localStorage` 中读取数据时，再用 `JSON.parse` 去解析即可

![local](http://7xq6al.com1.z0.glb.clouddn.com/local.png)

#### 4.3.2 IndexDB

> 对于 `IndexedDB` 来说，我们就可以使用对象来存储了

![indexDB](http://7xq6al.com1.z0.glb.clouddn.com/indexDB.jpg)


#### 4.3.3 Cookies

**Cookie存储的限制**

- 作为浏览器存储，大小`4KB`左右
- 需要设置过期时间，`expire`
- `cookie`的存储能力被`localStorage`代替

> 非常重要的一点，`CDN`域名不要携带`cookie`，因为每次请求中都不需要用户信息，否则会浪费大量的流量

![cookie](http://7xq6al.com1.z0.glb.clouddn.com/cookie.png)


#### 4.3.4 Service worker-离线应用

> `service worker` 是一个脚本，独立于当前网页，将其在后台运行，为实现一些不依赖页面或者用户交互的特性打开了一扇大门。在未来这些特性讲包括推送消息，背景后台同步，但它讲推出的第一个首页特性，就是拦截和处理网络请求的能力，包括以编程方式来管理被缓存的响应。

**service worker的应用**

- 使用拦截和处理网络请求的能力，去实现一个离线应用
- 使用`Service worker`在后台运行同时能和页面通信的能力

**例子**

![service-worker](http://7xq6al.com1.z0.glb.clouddn.com/worker.png)

![server-worker](http://7xq6al.com1.z0.glb.clouddn.com/server-worker.png)

> 不同的情况下，我们可需要在不同的存储介质中保持他们了，这个时候只需要不同的适配器即可。我们可以使用不同的库来，如支持使用不同介质的` localForge`，`IndexedDB`、`WebSQL`、`localStorage`。又或者是支持不同浏览器的 `store.js`

- 在客户端上存储数据的时候，就那么几种情况
- 单条数据。主要用于存储一些简单的数据，如用户 `Token`、功能开关、临时数据等等。
- 一个模型的数据集合。
- 多个模型的数据集合。
- 复杂的地方就是处理这些数据模型

#### 4.3.5 总结对比

**Cookie**

- 因为`HTTP`请求无状态，所以需要`cookie`去维护客户端状态
- 过期时间`expire`
- `cookie`的生成方式
   - `http response header`中的`set-cookie`
   - js中可以通过`document.cookie`读写`cookie`
 - 仅仅作为浏览器存储（大小`4KB`左右）
 - `cookie`中在相关域名下面---`cdn`的流量损耗
 - `httpponly`

**LocalStorage**

- `HTML5`设计出来专门用于浏览器存储的
- 大小为`5M`左右
- 仅仅在客户端使用，不和服务端进行通信
- 浏览器本地缓存的方案

**SessionStorage**

- 会话级别的浏览器存储
- 大小为`5M`左右
- 仅仅在客户端使用，不和服务端进行通信
- 对表单信息的维护


## 五、JS中的异步处理方案

> - 在`JavaScript`的世界中，所有代码都是单线程执行的
> - 由于这个“缺陷”，导致`JavaScript`的所有网络操作，浏览器事件，都必须是异步执行。异步执行可以用回调函数实现
> - 异步操作会在将来的某个时间点触发一个函数调用

- 主流的异步处理方案主要有：回调函数(`CallBack`)、`Promise`、`Generator`函数、`async/await`

### 5.1 回调函数(CallBack)

- 这是异步编程最基本的方法
- 假设我们有一个`getData` 方法，用于异步获取数据，第一个参数为请求的 `url` 地址，第二个参数是回调函数，如下

```javascript
function getData (url, callBack) {
    // 模拟发送网络请求
    setTimeout(() => {
        // 假设 res 就是返回的数据
        var res = {
            url: url,
            data: Math.random()
        }
        // 执行回调，将数据作为参数传递
        callBack(res)
    }, 1000)
}
```

> 我们预先设定一个场景，假设我们要请求三次服务器，每一次的请求依赖上一次请求的结果，如下

```javascript
getData('/page/1?param=123', (res1) => {
    console.log(res1)
    getData(`/page/2?param=${res1.data}`, (res2) => {
        console.log(res2)
        getData(`/page/3?param=${res2.data}`, (res3) => {
            console.log(res3)
        })
    })
})
```

- 通过上面的代码可以看出，第一次请求的 `url` 地址为：`/page/1?param=123`，返回结果为 `res1`
- 第二个请求的 `url` 地址为：`/page/2?param=${res1.data}`，依赖第一次请求的`res1.data`，返回结果为`res2`。
- 第三次请求的 `url`地址为：`/page/3?param=${res2.data}`，依赖第二次请求的`res2.data`，返回结果为 `res3`
- 由于后续请求依赖前一个请求的结果，所以我们只能把下一次请求写到上一次请求的回调函数内部，这样就形成了常说的：**回调地狱**

### 5.2 Promise

- `Promise` 是异步编程的一种解决方案，比传统的解决方案——回调函数和事件——更合理和更强大
- 简单说，它的思想是，每一个异步任务返回一个`Promise`对象，该对象有一个`then`方法，允许指定回调函数
- 现在我们使用 `Promise` 重新实现上面的案例，首先，我们要把异步请求数据的方法封装成 `Promise`

```javascript
function getDataAsync (url) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            var res = {
                url: url,
                data: Math.random()
            }
            resolve(res)
        }, 1000)
    })
}
```

> 那么请求的代码应该这样写

```javascript
getDataAsync('/page/1?param=123')
    .then(res1 => {
        console.log(res1)
        return getDataAsync(`/page/2?param=${res1.data}`)
    })
    .then(res2 => {
        console.log(res2)
        return getDataAsync(`/page/3?param=${res2.data}`)
    })
    .then(res3 => {
        console.log(res3)
    })
```

- `then` 方法返回一个新的 `Promise` 对象，`then` 方法的链式调用避免了 `CallBack` 回调地狱
- 但也并不是完美，比如我们要添加很多 `then` 语句， 每一个 `then` 还是要写一个回调
- 如果场景再复杂一点，比如后边的每一个请求依赖前面所有请求的结果，而不仅仅依赖上一次请求的结果，那会更复杂。 为了做的更好，`async/await` 就应运而生了，来看看使用 `async/await` 要如何实现

### 5.3 Async/Await

> 这是异步的终极解决方案，我们看一下用这种方式写异步有什么变化

- `await`后面必须是一个`Promise`对象
- `getDataAsync` 方法不变，如下

```javascript
function getDataAsync (url) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            var res = {
                url: url,
                data: Math.random()
            }
            resolve(res)
        }, 1000)
    })
}
```

- 接着在调用的函数外层加上`async`

```javascript
async function getData () {
    var res1 = await getDataAsync('/page/1?param=123')
    console.log(res1)
    var res2 = await getDataAsync(`/page/2?param=${res1.data}`)
    console.log(res2)
    var res3 = await getDataAsync(`/page/2?param=${res2.data}`)
    console.log(res3)
}
```

- 可以看到使用`async\await`就像写同步代码一样
- 对比 `Promise` 是不是非常清晰，但是 `async/await` 是基于 `Promise` 的，因为使用 `async` 修饰的方法最终返回一个 `Promise`， 实际上，`async/await` 可以看做是使用 `Generator` 函数处理异步的语法糖




