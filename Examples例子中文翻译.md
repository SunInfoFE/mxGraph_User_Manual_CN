## mxGraph JavaScript 
### 安装
这些例子可以通过任何文本编辑器进行编辑。要运行这些示例，请将浏览器直接指向本地文件（使用下面的链接）或者使用一个web服务器。需注意的是生产中一定要使用web服务来跑这些文件。仅建议在开发和测试时使用本地访问文件方式。（请阅读[这个](https://jgraph.github.io/mxgraph/docs/known-issues.html#AccessDenied)内容，了解Internet Explorer中本地文件系统的运行示例。）

### 例子

javascript/examples/editors 包含以下例子:

* [Graph Editor](https://jgraph.github.io/mxgraph/javascript/examples/grapheditor/www/index.html) - 全功能图形编辑器和绘图应用
* [mxDraw](https://jgraph.github.io/mxgraph/javascript/examples/editors/diagrameditor.html) - Web 2.0样式的绘图编辑器和绘图应用.
* [mxProcess](https://jgraph.github.io/mxgraph/javascript/examples/editors/processeditor.html) - 一个具有花哨的样式表和用户界面的流程编辑器。
* [mxWorkflow](https://jgraph.github.io/mxgraph/javascript/examples/editors/workfloweditor.html) - BPMN工作流编辑器，内置多个图形的实例.
* [mxWorkflow/Layout](https://jgraph.github.io/mxgraph/javascript/examples/editors/layouteditor.html) - BPMN工作流编辑器，带有自动布局（实验性）

javascript/examples 包含以下例子:

* [Codec](https://jgraph.github.io/mxgraph/javascript/examples/codec.html) -通过XML动态的建立一张图和解析model为XML，以及改变连线的默认样式。
* [Dynamicloading](https://jgraph.github.io/mxgraph/javascript/examples/dynamicloading.html) - 动态的载入图片模型（model）数据限制在模型（model）中细胞（cell）个数
* [Dynamic Style](https://jgraph.github.io/mxgraph/javascript/examples/dynamicstyle.html) - 通过重写mxGraphModel来改变细胞（cell）的样式
* [Dynamic Toolbar](https://jgraph.github.io/mxgraph/javascript/examples/dynamictoolbar.html) - 运行时改变toolbar的状态
* [Editing](https://jgraph.github.io/mxgraph/javascript/examples/editing.html) - 用即时编辑器触发指定的编辑值并将新的值写入用户对象的指定区域。同时例子中展示了包装标签和DOM节点作标签。
* [Events](https://jgraph.github.io/mxgraph/javascript/examples/events.html) - 建立一个图片的容器并且用mxDivResizer去更新尺寸，在图上交互，包括选取框选择，自定义提示，上下文菜单绑定和改变默认菜单透明度。它也演示了在默认的样式表中如何使用一个连线样式，并且绑定双击事件在调整点上。可查看：overlays.html 文件可以看到如何绑定点击事件。
* [File I/O](https://jgraph.github.io/mxgraph/javascript/examples/fileio.html) - 读取一个xml文件，写一个自定义解析器，提供一个自动布局和定义一个2-way连线。
* [Graphlayout](https://jgraph.github.io/mxgraph/javascript/examples/graphlayout.html) - 用一个自动布局并监听图片大小的改变同步保证容器的大小。
* [Hello, World!](https://jgraph.github.io/mxgraph/javascript/examples/helloworld.html)- 用一个DOM节点（node ）来建立一个图片并添加节点（vertex）和连线(edge)。
* [Hierarchical Layout](https://jgraph.github.io/mxgraph/javascript/examples/hierarchicallayout.html) - 用分级和有机布局算法。
* [Images](https://jgraph.github.io/mxgraph/javascript/examples/images.html) - 用背景图片和图片作为标签和图片形状。
* [Indicators](https://jgraph.github.io/mxgraph/javascript/examples/indicators.html) - 将一个子图形（指示）放入一个父图形中，典型的是一个mxLabel
* [Label Position](https://jgraph.github.io/mxgraph/javascript/examples/labelposition.html) - 用一个标签位置样式来设置节点标签的位置
* [Labels](https://jgraph.github.io/mxgraph/javascript/examples/labels.html) - 包装并裁剪节点的html标签，截断标签来适应节点的尺寸，并且手动设置节点的标签，使用相对子节点作为其“子标签“
* [Layers](https://jgraph.github.io/mxgraph/javascript/examples/layers.html) - 使用多图层来放置细胞（cell）。
* [Merge](https://jgraph.github.io/mxgraph/javascript/examples/merge.html) - 使用mergeChildren方法合并两张图
* [Monitor](https://jgraph.github.io/mxgraph/javascript/examples/monitor.html) - 使用mxGraph来展示一个工作的的当前状态
* [Offpage Connectors](https://jgraph.github.io/mxgraph/javascript/examples/offpage.html) - 在一张图中创建页外连接器，通过点击连接器实现加载一张新图。
* [Orgchart](https://jgraph.github.io/mxgraph/javascript/examples/orgchart.html) - 使用自动布局，适应页面的缩放和页面打印（跨多页面）
* [Overlays](https://jgraph.github.io/mxgraph/javascript/examples/overlays.html) - 细胞（cell）高亮，覆盖物和响应单击事件、双击事件。参见：events.html 示例了解更多事件响应。
* [Permissions](https://jgraph.github.io/mxgraph/javascript/examples/permissions.html) - 在一张图中建立权限来规定可用操作。
* [Ports](https://jgraph.github.io/mxgraph/javascript/examples/ports.html) - 使用相对位置子节点（vertices ）来实现端口，在细胞（cell）上应用拖拽操作、使用图片和HTML。
* [Schema](https://jgraph.github.io/mxgraph/javascript/examples/schema.html) - 实现一个数据库结构编辑器
* [Scrollbars](https://jgraph.github.io/mxgraph/javascript/examples/scrollbars.html) - 使用一个可滚动的表格作为一个细胞（cell）的标签
* [Secondlabel](https://jgraph.github.io/mxgraph/javascript/examples/secondlabel.html) - 添加另一个字符串作为当前节点的标签。
* [Shape](https://jgraph.github.io/mxgraph/javascript/examples/shape.html) - 怎样实现并使用一个自定义图形。
* [Stylesheet](https://jgraph.github.io/mxgraph/javascript/examples/stylesheet.html) - 在连线（edge）上使用一个自定义样式表和控制点，同时覆盖getLabel和getTooltip方法来返回动态的信息，并且在Javascript中构建一个supercall的方法。
* [Swimlanes](https://jgraph.github.io/mxgraph/javascript/examples/swimlanes.html) - 使用泳道（一种cell）来表示池（pools）和 跑到（lanes）并使用堆栈布局做为一个自动布局。
* [Thread](https://jgraph.github.io/mxgraph/javascript/examples/thread.html) - 通过一个定时执行函数在mxGraph上添加覆盖物。
* [Toolbar](https://jgraph.github.io/mxgraph/javascript/examples/toolbar.html) - 使用已存在的细胞（cell）作为模板来建立新的细胞（cell）。
* [Tree](https://jgraph.github.io/mxgraph/javascript/examples/tree.html) - 在一个非循环图（树）中折叠子树
* [UIConfig](https://jgraph.github.io/mxgraph/javascript/examples/uiconfig.html) - 使用一个配置文件来配置工具栏（toolbar）和弹出菜单在一个编辑器（mxEditor）中。
* [Userobject](https://jgraph.github.io/mxgraph/javascript/examples/userobject.html) - 使用 XML对象作为细胞（cell）的值。
* [Validation](https://jgraph.github.io/mxgraph/javascript/examples/validation.html) - 使用多样性（multiplicities）来动态校验一张图。
* [Windows](https://jgraph.github.io/mxgraph/javascript/examples/windows.html) - 使用mxWindow 类来作为展示弹窗
* [Wrapping](https://jgraph.github.io/mxgraph/javascript/examples/wrapping.html) - 在节点（vertex）和连线(edge)的标签上使用HTML标签和字符换行。
* [HelloPort](https://jgraph.github.io/mxgraph/javascript/examples/helloport.html) - 在连接另一个细胞（cell）的视觉交互中使用isPort钩子函数
* [Pagebreaks](https://jgraph.github.io/mxgraph/javascript/examples/pagebreaks.html) - 使用pageBreaksVisible和preferPageSize开关。(展示页面打印和页面分页的处理)
* [FixedPoints](https://jgraph.github.io/mxgraph/javascript/examples/fixedpoints.html) - 使用固定连接点来接到节点(vertices )的连线。
* [ServerView](https://jgraph.github.io/mxgraph/javascript/examples/serverview.html) - 使用一个服务器端的图片作为图在客户端展现。
* [ContextIcons](https://jgraph.github.io/mxgraph/javascript/examples/contexticons.html) - 在选中的节点上添加图标来实现特殊操作。
* [Guides](https://jgraph.github.io/mxgraph/javascript/examples/guides.html) - 使用guidesEnabled和snapToTerminals开关，通过一个画布和绑定光标键事件建立一个网格系统。
* [FixedIcon](https://jgraph.github.io/mxgraph/javascript/examples/fixedicon.html) - 在mxLabel图形上自定义图标的的位置。
* [Markers](https://jgraph.github.io/mxgraph/javascript/examples/markers.html) - 建立自定义标记（marker）
* [Dragsource](https://jgraph.github.io/mxgraph/javascript/examples/dragsource.html) - 多张图使用一个拖拽源并改变拖动的图标。
* [Orthogonal](https://jgraph.github.io/mxgraph/javascript/examples/orthogonal.html) - 演示点约束、正交线样式和连线处理函数的使用
* [Standardsmode](https://jgraph.github.io/mxgraph/javascript/examples/standardsmode.html) -  怎样使用mxGraph VML渲染一个IE中的文档。
* [EdgeTolerance](https://jgraph.github.io/mxgraph/javascript/examples/edgetolerance.html) - Increasing the tolerance for hit detection on edges.在连线上增加公差检测。
* [Stencils](https://jgraph.github.io/mxgraph/javascript/examples/stencils.html) - Using an XML file to define new stencils to be used as shapes.使用xml文件来定义新的模板作为图形。
* [IE9SVG](https://jgraph.github.io/mxgraph/javascript/examples/ie9svg.html) - 在IE9下使用SVG去渲染一张图片。（使用html5文档类型）
* [HoverIcons](https://jgraph.github.io/mxgraph/javascript/examples/hovericons.html) - 当鼠标划过节点上显示图标。
* [Portrefs](https://jgraph.github.io/mxgraph/javascript/examples/portrefs.html) - 通过ID引用连接点
* [Control](https://jgraph.github.io/mxgraph/javascript/examples/control.html) - 在一张图的指定细胞（cell）上添加控制。
* [Wires](https://jgraph.github.io/mxgraph/javascript/examples/wires.html) - 绘制带有设备和电线的电器和数字电路。
* [Menustyle](https://jgraph.github.io/mxgraph/javascript/examples/menustyle.html) - 使用css修改内置弹出菜单的样式
* [Perimeter](https://jgraph.github.io/mxgraph/javascript/examples/perimeter.html) - .如何避免连线和标签重叠的问题
* [Grid](https://jgraph.github.io/mxgraph/javascript/examples/grid.html) - 使用HTML5的canvas技术绘制一个动态的网格系统。
* [Groups](https://jgraph.github.io/mxgraph/javascript/examples/groups.html) - 将细胞（cell）变为其它细胞（cell）的一部分。
* [Visibility ](https://jgraph.github.io/mxgraph/javascript/examples/visibility.html)- 隐藏和现实细胞的各种解决方案。
* [Autolayout](https://jgraph.github.io/mxgraph/javascript/examples/autolayout.html) - 在每次图的动态改变后应用一个具有动画效果的布局算法。
* [Touch](https://jgraph.github.io/mxgraph/javascript/examples/touch.html) - 响应轻触（touch）事件、鼠标事件和msPointerEvents
* [Collapse](https://jgraph.github.io/mxgraph/javascript/examples/collapse.html) - 改变一个具有折叠功能的细胞的样式
* [Folding](https://jgraph.github.io/mxgraph/javascript/examples/folding.html) - 使用一个布局来处理一个具有嵌套关系的结构
* [LOD](https://jgraph.github.io/mxgraph/javascript/examples/lod.html) - 实现在一层上每个细胞（cell）的详情。
* [Hoverstyle](https://jgraph.github.io/mxgraph/javascript/examples/hoverstyle.html) - 鼠标浮动（mouseover）改变一个节点的样式（vertex）
* [Anchors](https://jgraph.github.io/mxgraph/javascript/examples/anchors.html) - 为所有的图形定义固定的连接点
* [Showregion](https://jgraph.github.io/mxgraph/javascript/examples/showregion.html) - 使用一个自定义橡皮圈（rubberband）事件在新窗口展示选中的范围。
* [Boundary](https://jgraph.github.io/mxgraph/javascript/examples/boundary.html) - 在BPMN图上实现边界事件。
* [Map](https://jgraph.github.io/mxgraph/javascript/examples/map.html) - 在Google地图上增加覆盖物。
* [JQuery](https://jgraph.github.io/mxgraph/javascript/examples/jquery.html) -使用一个JQuery插件来作为到处乱飞节点的标签。
* [Morph](https://jgraph.github.io/mxgraph/javascript/examples/morph.html) - 使用mxMorphing实现简单细胞动画
* [HTML label](https://jgraph.github.io/mxgraph/javascript/examples/htmllabel.html) - 使用HTML标签关联一个用户对象状态。
* [Drop](https://jgraph.github.io/mxgraph/javascript/examples/drop.html) - 处理原生拖拽图片到图中（需要高级浏览器）
* [Handles](https://jgraph.github.io/mxgraph/javascript/examples/handles.html) - 使用mxHandle来改变自定义样式的交互。
* [Extend canvas](https://jgraph.github.io/mxgraph/javascript/examples/extendcanvas.html) - 使用滚动条实现一个无限的画布
* [Clipboard](https://jgraph.github.io/mxgraph/javascript/examples/clipboard.html) - 
* 使用粘贴板实现跨页签和浏览器的拷贝和粘贴功能。
* [Constituent](https://jgraph.github.io/mxgraph/javascript/examples/constituent.html) - 使用细胞作为其他细胞的一部分。
* [JSON data](https://jgraph.github.io/mxgraph/javascript/examples/jsondata.html) - 使用JSON在mxCodec中编码/解码图模型的各个部分。
* [Animation](https://jgraph.github.io/mxgraph/javascript/examples/animation.html) - 使用SVG动画可视化管道中的流动。
* https://jgraph.github.io/mxgraph/javascript/examples/resources.html
* [Resources](https://jgraph.github.io/mxgraph/javascript/examples/resources.html) - 在主线程警告上禁用同步XMLHttpRequest。