# 1 简介
## 1.1产品介绍
mxGraph是一系列以不同技术开发的工具库，旨在提供显示交互式的 图表和图形的应用程序的功能。 请注意，对于图形，我们是指数学图形， 不一定单单指图表 （虽然有些图形是图表）。参见后面的章节：“什么是图形？”的细节描述。

作为一个开发库，mxGraph没有专门提供了一个现成的可以使用的应用程序， 尽管其中的许多例子都接近可以直接使用。 mxGraph提供mxGraph样式的 所有通常所需的绘画功能，互动及关联的图表显示环境。 mxGraph自带有许多例子， 它们有助于解释每种技术是如何被放在一起组成一个基本的应用程序，并展示这个 工具库的各项功能。

每本用户手册是针对某种特定的技术，都具有通用的部分，如简介和布局。开发人员会发现，对于 在不同的技术实现，在产品范围内的每个工具库都共享相同的架构和API。对于特定的技术领域， 事件处理和渲染的实现略有不同，但是从一个技术平台整体移植到另一个平台，mxGraph提供了 尽可能多的通用的接口。

开发人员在集成此工具库到他们自己的应用程序前，需要应该阅读的使用技术的先决条件。 参见下面的“先决条件”一节。鉴于mxGraph是您的应用程序的组成部分，你必须了解应用程序 使用的技术，以及如何使用该技术进行编程。

mxGraph主要包含一个JavaScript文件，mxGraph的全部函数都在这个文件中。它需要被加载到一个浏览器的Web页面的Javascript中并执行在HTML容器中。它结构简单，只要一个web服务器来提供html页面和一个支持JavaScript的浏览器就可以了。

它的优点如下：
-  不需要第三方插件。也就少了对厂商的依赖。
-  涉及到的技术都是开源的并且有很多开放的实现。这就意味着一个厂商删除它的一个产品或者技术不会导致你的程序无法工作。
-  标准化的技术，意味着你的应用可以部署在最大数量的浏览器上，用户不需要在客户端机器上添加额外的配置或进行安装。大型企业的环境通常不允许个人安装浏览器插件，也不允许改变所有机器的标准配置。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_architecture.png)

*mxGraph组件关系*

## 1.2 mxGraph可以被用在什么样的产品上？

图形可视化库的应用实例包括：过程图、工作流和BPM的可视化图表、流程图、交通或水流量、 数据库和WWW的可视化、网络和电信显示、映射应用和地理信息系统、UML图、电子线路、金融、 超大规模集成电路和社会网络、数据挖掘、生化、生态循环、实体和因果关系和组织图表。

## 1.3 怎样部署mxGraph？

在典型的瘦客户端环境中，mxGraph分为在客户端的JavaScript库和在服务器端两种支持的语言之一的.NET或Java库。 JavaScript库作为一个更大的基于浏览器的web应用程序的一部分，被一个标准web服务器分发到浏览器。所有的浏览器 需要开启JavaScript能力才能运行这个应用。

在本手册的第三部分，您会看到一个嵌入了mxGraph库的HTML页面，以及一个简单的调用了库功能的应用程序。

## 1.4 mxGraph的技术

mxGraph使用在浏览器上的客户端的JavaScript功能。而在JavaScript代码层面上，在浏览器中使用了基本的矢量图形语言来显示图形，当前SVG技术已经被所有浏览器支持。 mxGraph还包括完全只使用HTML来呈现的功能， 这会限制可以使用的功能范围，但可用于较简单的图表。

作为一名开发人员，您并不是被限制在浏览器相关的特定功能。如前所述，浏览器不同，所使用的矢量图形语言也不同， 所以mxGraph的功能被抽象成一个共同的类。同样，浏览器对于事件处理和DOM，两大浏览器实施的功能也不尽相同。然而， mxGraph通过使用恒定的API来适用于所有浏览器，掩藏不同浏览器间的内在差异。、

## 1.5 mxGraph 授权

mxGraph的JavaScript客户端采用了[Apache 2.0 license](http://https://www.apache.org/licenses/LICENSE-2.0/) 许可证授权，有关详细的许可问题，请务必咨询法律专业人士。

## 1.6 图形是什么?

图形可视化是建立于网络、图论的数学理论基础上。如果您正在查找JavaScript的条形图、饼图、甘特图, 可以参考[Google Charts](http://code.google.com/apis/chart/)项目，或类似的信息。
一个图是由顶点，也称为节点，以及边（节点之间的连接线）组成。图论中没有定义图究竟如何来视觉呈现。本手册中术语图元用来描述图形的构成元素，无论是边，顶点或图元组。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_simple_graph.png)

*一张简单的图*

图论中有些额外的定义，为图形处理提供 有用的背景，如果您感兴趣的话，它们都列在附录中。

### 1.6.1 图形的可视化

可视化是创建一个有用的图形可视化展现的过程。可视化功能的范围是mxGraphs的主要力量之一。 mxGraph支持范围广泛的功能，使图元显示仅限于开发人员的技术和平台可用的功能。顶点可以是图形、图像、矢量绘图、动画以及几乎所有可以在浏览器中操作的图形。您也可以在顶点和边使用HTML标记。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_graph_vis.png)

*交通系统的可视化图* (c) Tourizm Maps2003, http://www.world-maps.co.uk

### 1.6.2 图形交互

交互是指在一个使用mxGraph的应用程序中，通过WEB应用程序的GUI改变图形模式。mxGraph支持拖动、复制图元、重新调整大小、重新构造，连接和断开，从外部源的拖放和删除，编辑图元标签中的位置等等。 mxGraph的主要好处之一是通过编程来实现互动的灵活性。
许多复杂的图形化Web应用程序依赖于与服务器往返的通讯来显示图形，不仅是基本的显示，还包括交互事件。虽然这就是通常所谓的AJAX功能，这种服务器的依赖对交互事件是不合适的。视觉反馈时间超过0.2秒在应用程序中一般严重影响了实用性。mxGraph把所有的交互事件都放置在客户端，提供了真实感觉的应用程序，而不像一个哑巴的远程终端。它还提供了脱机使用的可能性。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_graph_interaction.png)

*通过鼠标拖动选择一个区域时显示阴影效果*
### 1.6.3 图像的布局

图形图元可以布置在一个简单的应用程序的任何地方，包括在彼此顶部。 某些应用程序需要按照一般或特殊的顺序结构来显示出示信息。 这可能涉及到确保图元不重叠和至少彼此间留有一定的距离，或出现在相对于其他图元的一个相对 位置，图元通常是通过边来连接。这个活动，被称为布局的应用，可以 通过多种方式，来协助用户设置自己的图形。 对于非编辑图形，布局应用是对图元进行布局算法的过程。 对于交互式的图形，即那些可以通过用户界面进行编辑，布局应用可能只 允许用户对特定的图元进行特定位置的修改，对每个修改重新布局，或 编辑完成后，重新布局。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_graph_layout.png)

*使用水平流布局对工作流进行布局*

mxGraph支持树、有机排列和流向的布局，来满足大多数布局的需求。后面的章节中会讲述更多布局的信息。

在客户端－服务器架构中运行布局可以有两个选项。JavaScript版提供了完全在客户端布局的能力，如果需要的话，同样的布局在服务器端的Java实现可以选择卸载一些服务器的处理。

### 1.6.4 图形的分析

图形分析涉及到确定有关的图形结构的某些细节算法的应用，例如， 确定所有路径或两个图元之间的最短路径。有些更复杂的图形分析算法，往往被应用于 指定域的任务。有些技术，如聚合、分解、优化等趋向某些针对性的科学领域的，目前包含在核心的mxGraph包中。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_graph_analysis.jpg)

*最短路径分析*

## 1.7 关于本手册
### 1.7.1 mxGraph先决条件

要从本手册中获益匪浅，您需要对Web应用程序和希望部署的服务器技术有一个合理的了解。部署的例子可以在每个服务器技术支持得到，熟悉该服务器的技术显然是必需的。

对于修改描述显示和行为方面的编辑器的配置文件，基本的XML知识是有用的。您需要理解和执行JavaScript编码，并熟悉面向对象编程原理和现代软件设计。

您不需要底层的浏览器使用的矢量图形的知识，如SVG或HTML的canvas。 mxGraph将可视化组件的描述抽象成一个API。

# 2 入门

## 2.1 mxGraph 包

### 2.1.1 获取mxGraph

mxGraph可以从[ github](https://github.com/jgraph/mxgraph) 项目上获得，发布的版本号为"va.b.c",其中a,b和c版本号遵循了语义版本控制

每一个正式版本的.zip或者.tar.gz包也可以在[mxGraph发布](https://github.com/jgraph/mxgraph/releases)页面获得。

### 2.1.2 项目结构和构建选项

解压缩后，你将在根目录下获得的一系列的文件和目录。


 目录/文件 | 描述
---|---
/doc | 文档根目录，包含本用户手册
/docnet | .NET服务器端代码
/java | Java服务器端代码
/javascript | JavaScript客户端功能
/javascript/examples | 	mxGraph的HTML演示例子
ChangeLog | 发布版本间差异详情
index.html |  库的基本介绍
license.txt | 使用库的许可条款

项目目录结构表

### 2.1.3 npm

mxGraph同样可以使用 npm 包管理获得。使用mxgraph作为依赖，用 npm 安装如下：

```
npm intall graph --save
```
这个模块可以使用require()方法进行加载。它将返回一个接受对象作为选项的工厂函数。必须将mxBasePath选项提供给工厂函数，而不是将其定义为一个全局变量。


```
var mxgraph = require("mxgraph")({
  mxImageBasePath: "./src/images",
  mxBasePath: "./src"
})
```

工厂函数返回一个“命名空间对象”，通过它可以访问mxGraph包的所有对象。例如，mxEvent对象在mxgraph.mxEvent中可用。

```
var mxEvent = mxgraph.mxEvent;
mxEvent.disableContextMenu(container);
```
## 2.2 JavaScript和web应用

Web应用程序，特别是在网页浏览器中使用JavaScript来试图效仿桌面应用程序， 仍然是一个相对较新的软件工程领域。障碍JavaScript生产出高质量应用的主要 有三个问题：性能，缺乏原生性的桌面应用程序功能以及浏览器之间API的不一致性。

相当大的努力已经被投入来开发框架库，以解决功能和API这两个问题。许多的开发库 的设计需求就是由同时改善网站的设计和可用性，以及协助我们完成一般的应用功能 （如菜单、窗口、对话框、持久性、事件处理等）的要求来驱动的。他们同时也提供了 某些在JavaScript中找不到的基本功能，如基本的数学和集合功能，而这些功能在桌面 的应用程序开发中是与生俱来的。

许多这些JavaScript框架，通过原生支持或作为一个插件的支持，可以用时下流行IDE来开发， 并支持所有的主流包含JavaScript调试器的浏览器。JavaScript没有编译过程（它是一种解释语言）， 因此，除非您的IDE具有语法检查工具，打字错误通常只能在运行时刻才可以被捕获。因此，世上没有 一个能够包罗万象的工具包，您往往需要使用好几个厂商的独立组件，才能提供你开发JavaScript 应用所需要的工具库。

### 2.2.1 第三方JavaScript框架

#### 2.2.1.1 原生JavaScript框架和库

为了不用列表和比较每一个框架，请大家参阅维基百科的条目[Web应用程序框架](https://en.wikipedia.org/wiki/List_of_JavaScript_libraries#JavaScript)和[JavaScript库比较](https://en.wikipedia.org/wiki/Comparison_of_JavaScript_frameworks)。这个比较表不能被认为是最权威的，而更象说明提供的功能类型，如提供事件处理、动画、小工具、支持AJAX请求等。 [这个网站](http://javascriptlibraries.com/)(注：这个网站内容已经变了)也是一个有用的JavaScript库名单，大多是基于开放/免费源许可。

请注意，很多框架添加了隐式的行为，使JavaScript的更像是一个面向对象的语言， 并增加了语言的基本功能。在写作的的布局mxGraph部分时，我们发现，这种隐含的行为 使得调试一个例子变得非常困难。在选择一个框架时，请留意它引入的隐式的行为，是否 会导致任何问题。

当选择了一个框架和/或工具库时，考虑您会被绑定的某些特定功能，并寻找那些不同的，可以提供所需功能如动画， 独立的模块，而无需在总体设计上被绑定。

#### 2.2.1.2 mxGraph与其他JavaScript构架的集成

这个部分经常被误解，简单来讲，并不需要集成。 Web应用程序一般包括一个或多个 [div](https://en.wikipedia.org/wiki/Span_and_div)元素， 可以被HTML用来放置包装应用程序的JavaScript。如果您创建一个div作为mxGraph的容器， 这就是一个可以为mxGraph应用程序的独立显示。它可以与任何后端服务器通信本身，而并不依赖与这个div和页面的其余部分，除了它们各自占的地方。这包括事件处理，mxGraph可以处理其容器的事件， 即便网页的其余部分用一个完全不同的事件模型。只要mxGraph和页面上的其他库和框架不引入会打破 一个页面作为整体的隐式行为，客户端集成的问题根本就不需要考虑。

与mxGraph服务器端集成，我们会在后面的章节阐述。

#### 2.2.1.3 mxGraph的JavaScript扩展

在JavaScript中，将语言结构映射面向对象范式有各种方式。mxGraph在整个项目中都使用一个特定的方法， 参见下面的默认规则：

- 不要更改内置的原型
- 不要试图限制JavaScript语言的力量

在mxGraph中，有两种类型的“类”：类classes和单例singletons （其中只有一个存在的类的实例）。单例被映射到全局对象而且变量名同类名是一样的。 例如，mxConstants是一个定义了所有常量字段的对象实例。普通类映射到一个构造函数和 定义了字段和方法的原型。例如，mxEditor是一个函数而mxEditor.prototype是mxEditor 函数创建对象时的原型。mx前缀是一种命名习惯，应用于mxGraph包中的所有类，以避免 与其他对象在全局命名空间发生冲突。

为派生，父类必须提供一个构造函数，要么是无参数或者可以处理不带参数的调用。 此外，特殊的构造函数字段派生后的原型必须重新定义。例如，mxEditor派生于mxEventSource。 在JavaScript中，首先通过分配父类的一个实例到子类原型，来“继承”从父类的所有字段和方法：

```
mxEditor.prototype = new mxEventSource()
```
并定义构造函数字段：

```
mxEditor.prototype.constructor = mxEditor
```

后面的规则，使得可以通过使用构造函数的名称mxUtils.getFunctionName(obj.constructor)来检索对象的类型。

**构造函数**

在mxGraph中，对于派生的子类应采用相同的机制。例如，mxGraph的派生子类，首先， 新类的构造函数必须被定义。构造函数调用的父类的构造函数，需要显式传入调用的 mxGraph对象的每一个参数：

```
function MyGraph(container)
{
   mxGraph.call(this, container);
}
```
MyGraph的portotype从mxGraph继承如下。像往常一样，子类的构造函数在继承后被重新定义：

```
MyGraph.prototype = new mxGraph();
MyGraph.prototype.constructor = MyGraph;
```
您可能需要在上述代码之后定义与该类相关联的编解码器（参见I/O部分手册）。该代码将在类加载时执行，并确保使用相同的编解码器来编码mxGraph和MyGraph的实例。

```
var codec = mxCodecRegistry.getCodec(mxGraph);
codec.template = new MyGraph();
mxCodecRegistry.register(codec);
```

**方法**

在MyGraph的prototype中，mxGraph的方法可如下扩展。


```
MyGraph.prototype.isSelectable = function(cell)
{
   var selectable = mxGraph.prototype.isSelectable.apply(this, arguments);
   var geo = this.model.getGeometry(cell);
   return selectable &&(geo == null || !geo.relative);
}
```

在第一行中的supercall是可选的。这是使用apply方法通过传入this及arguments这个变量作为参数， 到mxGraph的protoype的isSelectable这个方法上。父类的方法只有在不被覆盖的时候才可能被调用，这也是JavaScript中另一种“继承”的方式。


```
mxGraph.prototype.isSelectable = function(cell)
{
   var geo = this.model.getGeometry(cell);
   return selectable && (geo == null || !geo.relative);
}
```

如果方法的定义需要被完全覆盖，上述方案是有用的。

为了增加新的方法和字段，可以使用如下代码。在下面的例子，示范了增加了一个返回图模型的XML的新方法：

```
MyGraph.prototype.getXml = function()
{
   var enc = new mxCodec();
   return enc.encode(this.getModel());
}
```

**字段**

新的字段通过如下方式声明和定义：

```
MyGraph.prototype.myField = ‘Hello, World!’;
```
需要注意的是myField的值只分配了一次，那就是说，所有MyGraph的实例共享相同的值。 如果您需要每个实例拥有自己的值，则该字段必须定义在构造函数中。例如：


```
function MyGraph(container)
{
   mxGraph.call(this, container);
   this.myField = [];
}
```
最后，使用以下代码将一个新的MyGraph实例，其中container是一个图形视图的容器的DOM节点：

```
var graph = new MyGraph(container);
```

### 2.2.2 JavaScript开发综述

#### 2.2.2.1 JavaScript混淆

默认情况下，当你向浏览器客户端发送JavaScript时，发送都是JavaScript的全部源代码。然后，JavaScript在浏览器上被解析并运行。在客户端运行的时候，不可能在任何程度上加密JavaScript，因为JavaScript解析器必须理解和解释JavaScript源码，而且它不具有二进制的中间形式。

可以做到的是，在传输的过程中，将JavaScript加密，在客户端运行前解密，但客户端仍然能够访问解密后的源代码。

我们不做混淆，因为方法的名称形成的公共的API和I/O，在通信的两端都需要理解这样的混淆。

#### 2.2.2.2 命名空间

命名空间的概念在JavaScript中并不存在，所以在创建新的类名称时要非常谨慎。 mxGraph中，所有的类都以“mx-”的前缀开始，以避免无意中冲突或覆盖掉原型。 

## 2.3 Hello World!

mxGraph中的Hello World，是一个简单的客户端的例子，显示了两个相连的“Hello”和“世界”的顶点标签。 这个例子演示了以下几件事：

- 创建一个嵌入了mxGraph客户端JavaScript的HTML页面
- 创建了一个容器来装载mxGraph
- 在图形中加入了所需的元素

这个例子的源代码，helloworld.html，可以在mxGraph的源代码的示例目录下找到。 在HTML源代码包含两个主要部分组成，head和body。建立一个基本的mxGraph 应用程序的模板应包含以下主要内容：

**mxBasePath：** 这是一个JavaScript变量，用来定义CSS，图片， 资源和js的使用的目录。它是一段JavaScript代码，并需要被放置在 *script* 标签内。 它必须在加载mxClient.js之前，而且不应该斜线。

**mxClient.js：** 这是mxGraph库的路径。如果HTML文件在本地执行， 路径可能是本地计算机路径或公共互联网的路径。如果HTML页面是从Web服务器上下载，这路径 通常是一个公共的因特网路径。

**创建容器：** 在body元素中底部的代码，被定义为加载项 的方法（onload事件），加载网页时会被调用。它通过在传递即下定义的一个div 容器作为参数。mxGraph组件将被放置在这个div容器中。在此示例中网格被添加作为背景， 这在图表应用程序中经常用到。在容器创建时，其他视觉效果或者其他的背景和以及容器的 宽度和高度都没有定义。
注意，如果你想不出现滚动条，overflow:hidden格式应该一直被使用。

**入口方法：** 在这种情况下，该文件的主要代码是在页面加载时执行。 这是JavaScript代码，还必须在JavaScript的 *script* 标签当中。任何mxGraph 应用程序的第一行应该检查浏览器的支持，如果不支持应该适当退出。如果浏览器支持， mxGraph将在div容器内被创建，在开始/结束更新调用之间，三个图元被添加到图中。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_hello_world.png)

*mxGraph的HelloWorld例子*


```
<html>
<head>
   <title>Hello, World! example for mxGraph</title>

   <!-- Sets the basepath for the library if not in same directory -->
   <script type="text/javascript">
      mxBasePath = '../src';
   </script>

   <!-- Loads and initializes the library -->
   <script type="text/javascript" src="../src/js/mxClient.js"></script>

   <!-- Example code -->
   <script type="text/javascript">
      // Program starts here. Creates a sample graph in the
      // DOM node with the specified ID. This function is invoked
      // from the onLoad event handler of the document (see below).
      function main(container)
      {
         // Checks if the browser is supported
         if (!mxClient.isBrowserSupported())
         {
            mxUtils.error('Browser is not supported!', 200, false);
         }
         else
         {
            // Creates the graph inside the given container
            var graph = new mxGraph(container);

            // Enables rubberband selection
            new mxRubberband(graph);

            // Gets the default parent for inserting new cells. This
            // is normally the first child of the root (ie. layer 0).
            var parent = graph.getDefaultParent();

            // Adds cells to the model in a single step
            graph.getModel().beginUpdate();
            try
            {
               var v1 = graph.insertVertex(parent, null,
                        'Hello,', 20, 20, 80, 30);
               var v2 = graph.insertVertex(parent, null,
                        'World!', 200, 150, 80, 30);
               var e1 = graph.insertEdge(parent, null, '', v1, v2);
            }
            finally
            {
               // Updates the display
               graph.getModel().endUpdate();
            }
         }
      };
   </script>
</head>

<!-- Page passes the container for the graph to the program -->
<body onload="main(document.getElementById('graphContainer'))">

   <!-- Creates a container for the graph with a grid wallpaper -->
   <div id="graphContainer"
      style="overflow:hidden;width:321px;height:241px;background:url('editors/images/grid.gif')">
   </div>
</body>
</html>
```
这个例子中的重要概念有：
- mxClient.js是一个包含所有的mxGraph源代码的JavaScript文件。从Web服务器下载时， 获得包含所有的JavaScript的单个文件，要比分成多个独立文件要快得多，这是由于每个文件 都具有独立的请求/确认开销。无论服务器对于一个客户的并行接口的能力差异有多大，速度的 提升通常至少是两倍以上。
- 所有JavaScript代码及所有的依赖都是放在head元素中
- 默认情况下，Internet Explorer安全选项是开启的，将导致试图从本地文件系统中运行 JavaScript得到用户提示。这可以在选项菜单中禁用，但请注意，从本地文件系统上运行， 不是通常的mxGraph部署场景，这只会发生在开发过程中遇到。
- 您的应用程序可以写在HTML文件中并链接到应用程序，也可以写在另外的JavaScript文件中，再被链接到HTML中，就像在本例中的mxClient.js文件使用的方式。

## 2.4 mxGraph部署和调试

mxclient.js文件有两个版本，一个用于生产用途，另一个用于的开发/调试使用。*javascript/src/js/mxClient.js* 的是生产版， *javascript/debug/js/mxClient.js* 的是用于开发。第一个版本剥离了所有的换行符， 以确保该文件是最可能小的尺寸。这样做的副作用，是破坏了JavaScript的调试器。在开发过程中， 我们建议您使用调试版本，其中有换行符，支持的在浏览器中启用调试。

两个mxClient.js文件是包含整个mxGraph的JavaScript源代码，为减少文件大小，所有的空格和注释都被删除。 在调试过程中，如果您需要调试到mxGraph库本身，使用单独的源文件更加容易。在source.zip的 javascript/devel目录中，包含完整的源代码的文件。将它们解压到mxBasePath，并除去加载完整版 的mxClient.js文件，会使得调试mxGraph更加容易。需要注意的是，源文件的zip文件中的mxclient.js文件, 会引导加载的所有其他JavaScript源代码。

通过压缩代码，客户端的程序的下载速度，可以进一步提高。所有的现代浏览器都支持传输在服务器端压缩过的内容， 而所有良好的网络服务器可以检测出不支持的浏览器，并发送未压缩版本作为备用。

例如，在Apache Web服务器中有一个mod_deflate模块，通过一个标准的搜索，可以了解其使用的细节。jgraph.com服务器一直在使用这个模块，没有发现有任何浏览器的支持问题。

通过使用压缩，mxClient.js文件的大小从约600KB减少到只有130KB左右。对于使用最先进的网络用户而言， 区别并不明显，但在某些情况下，倾向于使用较小的版本。

# 3 mxGraph的模型和图元
## 3.1 mxGraph的核心架构
### 3.1.1 mxGraph的模型

mxGraph模型是，描述了图形结构的核心的模型，被称为mxGraphModel，可以在model包中发现。 另外，对图形结构的添加，更改和清除是通过图模型API来完成的。该模型还提供了方法来确定图形 的结构，以及提供方法来设置，如能见度、分组和样式的视觉状态。

然而，虽然对于模型进行的处理是被存储在模型上的，mxGraph被设计成一种通过mxGraph类的主要公共API来使用的方式。 “添加该单元格到图形”的概念，是一个比“添加单元到图形的模型”的更自然的动作。它是直观的，在模型上和单元上的方法被复制到了图形类上，而这些图形类上的方法被认为是主要的公共API。本手册的其余部分，这些关键的API方法都被以粉红色的背景标示(注：真实情况似乎是文字加粗)：

```
anExampleCoreAPIMethod()
```

因此，尽管许多的主要API通过mxGraph类来调用，请注意，mxGraphModel是基本的对象，它存储着图形的数据结构。

mxGraph使用事务处理系统来更新模型。在HelloWorld的例子里，我们看到如下代码：

```
// Adds cells to the model in a single step
graph.getModel().beginUpdate();
try
{
   var v1 = graph.insertVertex(parent, null, 'Hello,', 20, 20, 80, 30);
   var v2 = graph.insertVertex(parent, null, 'World!', 200, 150, 80, 30);
   var e1 = graph.insertEdge(parent, null, '', v1, v2);
}
finally
{
   // Updates the display
   graph.getModel().endUpdate();
}
```

执行2个节点和1条连线的插入。对于模型的每一个变化，请调用beginUpdate()，作出适当的调用更改模型，然后调用endUpate()方法来完成的变化，通知发送变化的事件出去。

**关键API方法：**

- **mxGraphModel.beginUpdate()** - 启动一个事务或子事务处理。
- **mxGraphModel.endUpdate()** - 完成一个事务或子事务处理。
- **mxGraph.addVertex()** - 添加一个新节点到指定的父单元。
- **mxGraph.addEdge()** - 添加一个连线到指定的父单元。

**注意** 从技术上讲，你不必用开始和结束调用来包围着你的更改。此更新范围之外所做的更改会立即生效，并立即发出通知。事实上，更新范围内的更改会立即在模型上立即实现，更新范围是控制事件通知的时间和连接。除非更新包装导致代码审美问题，否则值得使用它来避免事件和撤消粒度的可能问题。

请注意，这种将模型更改的包装在try块中，endUpdate()放在finally块中的方式。即使模型的更改有错误，它依然确保了更新的完整性。

现在请先忽略parent图元的引用，在本章节的后面再做解释。

### 3.1.2 事务模型

以上蓝色块中的子事务，是指事务可以被嵌套。也就是说，在模型中有这样一个计数器，每次调用beginUpdate计数递增，每次调用endUpdate计数递减。在计数器增加超过1后，当该计数再次达到0时，模型的事务被认为是完成，模型的事件通知被触发。

这意味着，每个子代码的部分就可以（而且应该）被开始/结束组合来包围。在mxGraph中，这创建单独的事务，被用来作为“库事务”的能力，能够为创建复合改动，一系列事件的所有改动一起触发并且只需要创建一个撤消。自动布局是说明这个功能必需性的很好的例子。

在自动布局中，在用户通常通过用户界面修改了图形，应用程序自动根据默认规则定位结果。自动定位即布局，在开始/结束调用之间的独立算法，它并不知道具体的变化内容。因为所有的在开始/结束变化范围内的更新是由直接作用在图形模型上，布局是根据模型的状态的变化来进行。

需要重点区分的是，作用在图形模型上的功能，是作为复合改动的一部分，还是原子态图形的改动事件。在第一种情况下，如用于自动布局，该功能将模型就当成那样而作用于它。此方法只用于作为复合变化的一部分时使用。应用程序的所有的其他部分，应该依据模型的改变事件而作出反应。

当最后一个endUpdate调用将计数器还原到0并指示至少发生了一个原子图更改时，会触发模型更改事件。改变事件包含着完整的已改变信息（参见后面的部分Events更多详细信息）。

#### 3.1.2.1 模型改变方法

以下是更改图形模型并应直接或间接放置更新范围的方法的列表：

```
add(parent, child, index)
remove(cell)
setCollapsed(cell, collapsed)
setGeometry(cell, geometry)
setRoot(root)
setStyle(cell, style)
setTerminal(cell, terminal, isSource)
setTerminals(edge,source,target)
setValue(cell, value)
setVisible(cell, visible)
```

最初，我们只关心添加和删除，以及几何和样式编辑方法。请注意，这些方法不是核心API方法，像往常一样，这些方法在mxGraph类中是适用的，他们执行的是被封装的更新。

*设计背景* - 有些人对可视信息被存储的模型中感到困惑。这些属性包括图元定位，可见性和折叠状态。模型存储了这些属性的默认值，提供一个共同的地方对每个单元进行设置，以及对每个视图的单独设置。模型是整个架构中，第一个通用的地方可以以全局的方式设置这些属性。请记住，这是一个图形可视化库，可视化的部分是核心功能。

**插入图元**

在HelloWorld应用程序中，创建的三个图形单元包括两个节点和一条连线。如果你不熟悉基本图形理论和术语，请参阅 [维基百科条目](https://en.wikipedia.org/wiki/Graph_theory) 。

你可以使用add()方法添加节点和连线到模型中。但是，考虑到日常使用库的场景，请学习mxGrap.insertVertex()和mxGraph.insertEdge()这两个添加图元的核心公共API。

模型功能的要求，被添加的图元必须已经创建，而mxGraph.insertVertex()为你创建了图元。

**核心API方法：**

**mxGraph.insertVertex(parent, id, value, x, y, width, height, style)** –在调用开始/结束更新中，创建并插入一个新的节点到模型中。

**mxGraph.insertEdge(parent, id, value, source, target, style)** –在调用开始/结束更新中，创建并插入一条新的连线到模型中。

mxGraph.insertVertex() 会创建一个mxCell对象并返回。方法的参数为：

**parent** – 组结构中此图元的直接父图元。我们会很快谈论到组结构，但现在我们直接使用graph.getDefaultParent();作为默认的父图元，就像在 HelloWorld 这个例子一样。

**id** – 描述此单元的全局唯一身份号码，总是一个字符串。主要用于外部对这单元的引用。如果你不想自己维护这些号码，只需要传入一个空参数并确保mxGraphModel.isCreateIds()返回真即可。这样，模型就会管理这些号码，并保证它们的唯一性。

**value** – 此单元的用户对象。用户对象只是一些对象，可以让您把应用程序的商务逻辑与mxGraph的可视化呈现相关联。在手册的后面有详细地描述，这里我们就只用字符 串就好，并把它们显示成顶点和边的标签。

**x, y, width, height** – 就像名字提到的，这是节点的左上角的 x 和 y 的位置以及它的宽度和高度。

**style** – 将被应用到节点的样式描述。关于样式，很快会有更详细的描述，简单来讲，就是一个特定格式的字符串。这个字符串有零个或多个样式名字和一些键/值配对，用来覆盖全局设置或者创立新的样式。除非我们要创建自己的样式，我们可以直接使用这些现有的设置。

添加连线的方法和添加节点的方法使用了同样的参数。source和target参数定义了节点要连接的节点。注意，源节点 和目标节点需要已经被加入到模型中。

### 3.1.3 mxCell

mxCell是节点和连线的图元对象。mxCell从模型那里复制了许多的方法。它们的主要差别在于，使用模型的方法会创建相关的事件通知以及撤销方法，使用图元的方法可以发生改变但不记录它们。这对于临时改变视觉效果，如动画或鼠标效果，是非常有用的。作为通用规则，一般使用模型的编辑API，除非您遇到什么特殊问题。

当创建新的图元时，构造函数需要三部分参数，值（用户数据），几何参数以及样式。我们在回到讨论图元之前，先了解一下这三个概念。

#### 3.1.3.1 样式

样式和样式表的概念挺像CSS的样式表，尽管你已经注意到mxGraph中事实上使用的就是CSS，但CSS只是影响HTML的DOM的全局样式。当你使用编辑器打开 util.mxConstants.js 文件并查询开头皮匹配“STYLE_”,如果你向下滚动鼠标，将会看到很多带有这个前缀的各种样式定义字符串。一些样式应用到节点上，一些适用于节点，一些适用于连线，一些都适用。正如你所见，这些视觉属性定义在它们操作的元素上。

mxStylesheet包含一个对象，样式，则以一个散列表映射样式名称到一个样式数组。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_styles.png)

*样式集合中的样式列表*

上面蓝框里的图显示了在mxStyleSheet里面的样式表。字符串“defaultVertex”是真实样式串/值配对列表中的键值。请注意，mxGraph创建两组默认样式，一个给节点，一个给连线。如果你看回helloworld这个例子，作为可选参数，没有任何样式值传入insertVertex或insertEdge。这种情况下，默认的样式会被使用。

**设置图元的样式**

如果你希望给一个图元指定非默认的样式，你必须在创建时传入（mxGraph的insertVertex和insertEdge都有 为这个用途的可选参数），或者对这个图元用model.setStyle()设定样式。

你传入的样式有样式名，请注意，样式名和键/值配对可以按照任何顺序排列。下面是这个概念的示例，使用我们在helloworld中看到的对insertVertex的调用：

1. 创建一个叫'ROUNDED'的样式，并应用到一个节点上：

```
var v1 = graph.insertVertex(parent, null, 'Hello', 20, 20, 80, 30, 'ROUNDED');
```

2. 用ROUNDED样式创建一个新节点，覆盖笔画样式和填充颜色：


```
var v1 = graph.insertVertex(parent, null, 'Hello',  20, 20, 80, 30, 'ROUNDED;strokeColor=red;fillColor=green');
```

3. 创建一个没有全局样式，但有本地笔画样式和填充颜色：


```
var v1 = graph.insertVertex(parent, null, 'Hello', 20, 20, 80, 30, ';strokeColor=red;fillColor=green');
```

4. 用默认defaultVertex样式，但本地填充颜色的节点：

```
var v1 = graph.insertVertex(parent, null, 'Hello', 20, 20, 80, 30, 'defaultVertex;fillColor=blue');
```

请注意，这种情况下，默认样式必须显式的指明，在分号起始的字符串之后，没有指明样式名这个图元即会 缺失全局样式。如果没有分号，则默认样式会被使用。

同样，mxGraph在核心API中提供了工具方法来访问和修改图元的样式：

**核心API方法：**


 **mxGraph.setCellStyle(style, cells)** – 封装在开始/结束的更新中，指定一组图元的样式。
 
 **mxGraph.getCellStyle(cell)** – 返回指定单元的样式，融合了这种单元类型，任何本地的和默认全局的样式。
 
**创建新的全局样式**

要创建上述ROUNDED全局样式，你可以按照这个模板来创建一个样式，并将其注册到mxStyleSheet上：

```
var style = new Object();
style[mxConstants.STYLE_SHAPE] = mxConstants.SHAPE_RECTANGLE;
style[mxConstants.STYLE_OPACITY] = 50;
style[mxConstants.STYLE_FONTCOLOR]= '#774400';
graph.getStylesheet().putCellStyle('ROUNDED',style);
```


#### 3.1.3.2 几何

在helloworld例子中，我们看到在调用insertVertex方法时，传入了节点的位置及大小信息。在JavaScript的坐标系统中，x是向右为正，y是向下为正，而对图形而言，是相对mxGraph放置的容器的绝对位置。

有专门独立的mxGeometry而不是简单地用mxRectangle保存这个信息的原因，是因为连线也有相应的几何信息。

对于连线而言，宽带和高度的值被忽略，而x和y对应的是连线的标签位置。另外，连线还有控制点的概念。它们是沿边的中间点位置，画线时需要经过。控制点的使用有时也被称为边缘路由。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_edge_routing.png)

*一条由两个控制点决定的边*

在几何里面还有两个重要的概念，相对位置和偏移。

**相对位置**

默认情况下，一个节点的x和y位置是图元本身的边界矩形的左上角点与父图元的边界矩形的左上角点的偏移量。父图元和组的概念将在本章的后面进行讨论，这里就不深入细节，如果一个图元没有父图元， 那么为了定位，图形容器就是它的父图元。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_non_relative_pos.png)

非相对的节点位置

对于一条连线，在默认的非相对模式中，连线的标签位置是对图形原点的绝对位置。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_non_realtive_edge_pos.png)

*非相对连线的标签位置*

对于相对模式中的节点，(x,y)是沿父图元（宽度，高度）的图元的原点所在的比例。(0,0)是与父图元 相同的原点，(1,1)是原点放在父图元的右下角。两个方向上，相对位置向0和1以上延伸。这有助于子图元保持 对父图元整体大小的固定。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_rel_vert_pos.png)

*相对节点位置*

最后，在相对模式下的连线的标签位置，是根据连线的中心来确定。连线的x坐标是相对位置，-1是连线的源端， 1是边的目标端。连线的y坐标是了连线的正交像素偏移量。下图显示了在相对模式下的各种连线标签的x，y的值。 请注意，对于一条直线，计算是非常简单的。对于有多个控制点的连线，连线是沿要跟踪段（段结束点和/或 控制点之间的界线）来找到正确的沿连线的距离。 y值是到该段的正交偏移量。

对于连线的标签，切换到使用相对位置，是一种常见的应用程序的偏好。导航到mxGraph的mxGraph.insertEdge() 方法中，你会看到createEdge()这样的调用。在createEdge()中，几何上设置为相对位置，是使用这个创建每一条连线的。在mxGraph中辅助方法有一定数量，是因为他们能够很容易改变默认行为。你应该在应用程序中， 尝试尽可能多地使用mxGraph类中API，享受这项福利。

**偏移**

在mxGeometry中，偏移量字段是应用到图元标签的绝对x，y偏移量。在连线标签的情况下，该偏移量总是施加在边标签已根据上面部分相对标志计算好之后。

**核心API方法：**

- **mxGraph.resizeCell(cell, bounds)** - 在开始/结束的更新调用之间，改变指定图元的大小到指定的边框。
- **mxGraph.resizeCells(cells, bounds)** - 在开始/结束的更新调用之间，改变指定队列中所有图元的大小到指定的边框。

#### 3.1.3.3 用户对象

用户对象给了mxGraph一个环境，可以把业务逻辑与可视图元相关联。在HelloWorld的例子里，用户对象只是一个字符串，只是简单地用来呈现单元的标签。在更加复杂的应用里，用户对象可以是一个复杂的对象。这个对象的一些属性可以用来作为图元的显示使用，而对象的其余部分可以用来描述应用领域的逻辑关系。

用一个简单的工作流或过程应用程序来做例子，假定我们有以下的图形（[这个例子已在线](https://jgraph.github.io/mxgraph/javascript/examples/editors/workfloweditor.html)，在任务窗口选择泳道Swimlanes的例子）：

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_simple_workflow.png)

*一个简单工作流*

通常情况下，该工作流程将存在于某些应用服务器和/或数据库上。浏览器端用户连接到该服务器，或者一些前端服务器连接到应用程序服务器和用户的Web应用程序请求“订购”的工作流。网站服务器取得该工作流中的数据并将其发送到客户端。

mxGraph支持服务器端填充模型、发送到客户端，然后再返回的过程。请参阅后面的章节关于“I/O和服务器之间的通信”。

数据的发送在视觉模型（图中）和以及业务逻辑（主要是包含在用户对象）都会发生。客户端将首先显示如上图。如果用户有权限编辑工作流程，他们通常会做两件事情：1）编辑图表，添加和删除节点，以及改变的连接，2）编辑图元的用户对象（节点和/或连线）。

在在线演示中，如果右键点击菱形“Check Inventory”并选择属性，你会看到如下对话框：

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_vertex_props.png)

*节点的属性*

这些属性展示了几何数据，标签，ID等，但一个对话框可以很容易地图元的用户对象。这有可能是在工作流引擎某个过程的引用，关于怎样检查库存清单。这可能是一个用于特定应用程序的机制，在服务器和客户端为远程方法调用分配一些识别标志。另一种类型的值可能是调用过程的返回对象，也许是一个布尔值或整数（在这种情况下，表示库存水平）。由于这个返回类型，它有可能可以加强对图形的约束，并提供视觉化的提示，如，出口连线的决定检查不符合返回的节点类型。

接下来，作为一个示例，发出的连线的用户对象可能包含一个标签和一个布尔状态。同样，基于mxGraph的编辑器可能会提供更改布尔值的方法。在服务器端，当执行到该步骤时，它可能会跟随对应的决策的节点返回的布尔值的连线。

请记住，上述示例是非常具体的领域的，它用来解释如何将用户对象映射到应用程序的业务逻辑。它展现了mxGraph如何创建我们所谓的上下文图。这上下文是由节点之间的连接和用户对象存储的业务逻辑构成的。一个典型的应用程序从服务器接收可视化部分和业务逻辑，可能允许编辑它们，接着发送到服务器去持久化和/或执行。

#### 3.1.3.4 图元类型

如前所述，mxGraph是使用这个库时的主要API，同样图元也是。在图上没有暴露图元的一个是节点还是连线的基本状态，这个调用可以在图元上或在模型上找到。

在mxCell上有两个标志量，顶点和边，在一个图元创建时，辅助函数将设置其中一个值为true，isVertex(), isEdge() 在 mxGraphModel中用来检测一个图元的类型，所以这两种类型没有分离的对象。从技术上讲，在运行时可以随便改一个图元的类型，但是要注意在改变类型后无效的图元状态。同时，要留心几何对象方法的参数在顶点和连线上是不同的。通常，不建议在运行时修改一个图元的类型的。

### 3.1.4 组结构

在mxGraph中，分组的概念就是逻辑上将一个图元与另一个进行关联。在许多的图形开发库中，这通常被成为子图。在图形模型的数据结构中，分组就是把一个或更多的连线或节点变成一个父节点或连线的子图元。分组使得mxGraph拥有了更多的有用的特性：

- 子图 一个逻辑上独立的图形的概念，在较高的层次图中显示为每个子图的图元。
- 展开和折叠 折叠是这样的一种能力，它使用父图元在视觉上来替换一组子图元。展开则是与其相反的逻辑。通过单击在线[工作流程示例](http://jgraph.github.io/mxgraph/javascript/examples/editors/workfloweditor.html)中泳道示例的组单元格左上角的小“ - ”可以看到此行为。这会在下面的 _复杂性管理_ 章节中进行讲解。
- 分层 层次的概念是指在图形的显示中，让图元以特定的顺序显示。
- 下钻，递升 这两个概念是让子图可以当作完整的图形一样可视化和编辑。在 _用户对象_ 章节我们看到 “check inventory” （检查库存）节点作为一个简单图元。举个例子来说，一个开发人员正在描述流程中每一个节点作为软件流程中执行的任务。应用程序中可能会有一个选项去下钻到检查库存的节点。这将导致一个新的图形出现，详细地描述了检查库存的细节。图中可能会有一个标题为“检查库存”的节点用以表示它是一个子图，以及一个选项去递升回到上一个级别。


在分组中，图元都分配了一个父图元。最简单的情况是，所有的图元都有一个默认的父图元作为他们的父图元。这个父图元是一个不可见的图元，有着和整张图相同的界限。这个图元在 helloworld 例子中可以通过 graph.getDefaultParent() 返回。一个节点的x,y位置是相对它的父节点的，因此在默认分组的情况下（所有的图元共享默认父图元），图元的定位也是图形组件上的绝对坐标。在所有的图元都被添加到默认根图元的情况下，该组的结构逻辑上的模样，在hello world例子中，看起来如下图所示。


注意添加了0层图元，这是在组结构中的默认间接方式，允许根据附加图元的要求进行图层的更改。我们将它包含在下面以便正确性，但在稍后的组图中它将被省略。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_hello_struct.png)

*helloworld例子中的组结构*

同时，请注意连线标签的位置(几何上的x,y)是相对其父图元的。


如果我们回头去看用户对象章节的简单工作流例子，能看到组看起来是什么样的。在这个例子中组图元表示人，并且子节点表示分配给这些人的任务。在这个例子中，逻辑组结构如下所示：

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_log_group_struct.png)

*工作流示例的逻辑组结构*

工作流程操作节点是黄色的子节点，泳道组节点被标记为蓝色。

插入图元的到组结构是通过使用mxGraph类的insertVertex和insertEdge的parent参数方法。这些函数相应地将父图元格设置在子图元上，而且重点是，会通知父图元新子图元的加入。

通过mxGraph.groupCells（）和mxGraph.ungroupCells（）函数来更改组结构。

**核心API方法**

- mxGraph.groupCells(group, border, cells) – 添加指定的图元到指定的组，在一个begin/end更新结构中。
- mxGraph.ungroupCells(cells) – 从指定图元的父图元中移除它们，并将其加入到它们的父图元的父图元中。任何空的组在这个操作后将被删除。这个操作需要在一个begin/end更新结构中


### 3.1.5 复杂度管理

任何时候控制显示图元的个数主要有两个原因。首先是性能，绘制越来越多的图元在任何平台上都将会在某个时间点达到性能的瓶颈。第二个原因是易用性，一个人只能理解一定量的信息。上面列出的与组相关的所有概念，能够用来为用户降低屏幕上信息的复杂度。

#### 3.1.5.1 可折叠

可折叠是我们用来描述组展开和折叠一个集合名词。我们可以将令一个图元内的子图元不可见称为折叠。有许多与此特性相关的方法：

**核心API方法**

- **mxGraph.foldCells(collapse, recurse, cells)** – 在一个begin/end更新结构中，指定图元的折叠状态。


**可折叠相关方法：**

- **mxGraph.isCellFoldable(cell, collapse)** – 对于有子图元的图元而言，默认为真。

- **mxGraph.isCellCollapsed(cell)** – 返回图元的折叠状态

当一个组图元折叠时，默认发生三件事：

- 图元的子图元变为不可见
- 组图元的边界被使用。在mxgeometry中有一个alternativebounds字段，并且在组图元中，默认地分别存储了展开和折叠状态的边界。这些实例之间的切换由mxgraph.swapbounds（）调用，实际上这些是foldcells（）调用过程中为你处理的。这允许折叠组能够被改变大小，同时当再次展开看起来和折叠前的尺寸一样。
- 默认情况下会发生连线提升。连线提升意味着去展现这样的连线，它们连着子图元通过折叠组图元，组图元同样连着外面的折叠组图元，通过使得这些子图元消失而转去连接折叠的父图元。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_expand_swim.png)

_展开泳道_

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_collapse_swim.png)

_折叠泳道_

以上两张图片展示了这三个概念。在扩展状态下，上面的组图元在左上角显示一个小框，里面有一个“ - ”字符。这表示单击此框会折叠组图元。点击后我们将获得下面的图片，图中组图元使用着它的折叠尺寸。没有离开子节点和边的图元都是不可见的。最后，离开组图元的连线被提升，表现为连接到折叠的组图元。点击框中现在出现的“+”字符展开组图元，并将其返回到上面的那个张图的原始状态。

通过调用mxGraph.foldCells()方法，你可以通过编程获得与单击展开/折叠符号相同的结果。一个常见的用法是这样的，当应用缩放到指定的数值，图元群被分组并且组图元折叠（往往不带“-”框，因为应用程序在控制折叠）。通过这种方式，用户可以看到更少，更大的图元，逻辑上每一个图元都代表其子图元。接着你可以提供一种机制去放大一个组，以在该过程中扩展它。你也可以提供下钻/递升，接下来就解释一下。

#### 3.1.5.2 子图, 下钻 / 递升

有时候，作为一种展开/折叠方案的另一个选择，或者可能与其结合使用，你的图会由一组图组成，嵌套到层次结构中，下面我们看一个简单的例子：

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_drill_down.png)

_一个顶级工作流的例子_

这个简单的流程由三个高级别的步骤组成。显然，单个步骤包含许多子步骤，我们将查看 _Solve Bug_ 图元的子图。


在 _Solve Bug_ 节点下，我们创建了一些子节点来呈现解决一个问题的流程的细节，在这种情况下，解决了在企业号星舰（[Starship Enterprise](http://en.wikipedia.org/wiki/Starship_Enterprise)）上的一个问题。

在这个用GraphEditor的例子里，在上图显示的选中的菜单选项调用了mxGraph.enterGroup(cell),这是子图相关的一个核心的API。

**核心API方法：**

- **mxGraph.enterGroup(cell)** – 使指定的图元成为显示区域的根图元。
- **mxGraph.exitGroup()** - 使当前图元的父图元（如果有）成为新的根图元。
- **mxGraph.home()** - 离开所有组，使默认父图元成为根图元


到目前为止，图的根图元已经是所有第一级图元的默认父节点。使用这些函数你能够将任何组结构内的组图元变成根图元，这样父图元的子图元就可以作为完整的图形显示出来。

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_drilling.png)

_下钻到Solve Bug节点的结果_

同样的图形如采用折叠方式会看起来如下：

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_top_level.png)

退出组用 _shape->exit group_ 选项，它会调用mxGraph.exitGroup，带你回到原始的三个节点的最高一级的图。

#### 3.1.5.3 分层和过滤

在mxGraph里, 像其它图形化应用一样，它也有z顺序的概念。也就是说，你看向屏幕的方向就是对象的顺序。对象可以位于其他对象的后面或前方，如果它们重叠且不透明，则最后面的对象将部分或完全遮盖。让我们回顾一下上面的HelloWorld图的图形结构。子图元以确定的顺序被存储在父图元下（默认情况下，是你添加它们的顺序）

如果我们移动HelloWorld例子中的图元，我们将看到如下的结果：

![image](https://jgraph.github.io/mxgraph/docs/images/mx_man_overlap.png)

-重叠的节点-

可以看到World节点位于hello节点的前面。这是因为World节点比Hello节点有一个更高的子顺序，它们分别在根图元的有序子图元集合中的位置1和0位置上。

改变顺序我们可以用mxGraph.orderCells方法。

**核心API方法：**

- **mxGraph.orderCells(back, cells)** – 在开始/结束的更新调用之间，根据标志位，移动一组图元到它们的兄弟图元的前面或者后面。

mxGraph中的兄弟图元是指任何拥有相同父图元的图元。因此，对Hello节点执行此方法，会使其覆盖World节点。

排序和分组可以扩展成逻辑分层组。图元通过深度优先搜索被绘制。再次采用helloworld示例，设想一下，hello和world节点下面都有一些同层的子图元。Hello节点及其子图元会比World节点或其子图元先绘制。如果Hello节点和World子点是不可见组图元，那么你就会有两个图元层次结构，一个完全在另一个之前绘制。你还可以通过简单地切换不可见组图元的顺序来切换层次结构的顺序。

layers.html示例演示了分层的概念。这里按钮用于设置组图层图元的可见性。这个例子非常接近过滤的概念。

筛选具有一些特定的属性的图元来显示。提供过滤功能的一种方法是在渲染图元之前检查某个状态。另一种方法，如果过滤条件简单且事先已知，则按组分配可过滤单元。执行这个过滤操作时，可以显示或隐藏这些组。











