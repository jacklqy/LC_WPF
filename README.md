# LC_WPF
## 计算机基础知识
bit（位，又名“比特”）：bit的缩写是b，是计算机中的最小数据单位（属于二进制的范畴，其实就是0或者1）

Byte（字节）：Byte的缩写是B，是计算机文件大小的基本计算单位。比如一个字符就是1Byte，如果是汉字，则是2Byte。

1B（字节）= 8b（位） 1字节最大表示二进制数为11111111(256)

1KB = 1024B

1MB = 1024KB

1GB = 1024MB

1TB = 1024GB

二进制(0/1)、八进制(0-7)、十进制(0-9)、十六进制(0-F) 之间的相互转换。
![image](https://user-images.githubusercontent.com/26539681/142978936-4f4b861e-7639-45b9-8c51-a7beed368151.png)

二进制：它由两个基本字符0，1组成，二进制代码运算规律是逢二进一。***从右到左开始计算(从低位到高位计算),不足八位则左侧补位0.***

     1)列如：00000000(0)->00000001(1)->00000010(2)->00000011(3)->00000100(4)->...->11111111(255)
其它进制的转换也是类似逢几进一。

以0x开始的数据表示16进制，逢16进1。如今的16进制普遍应用在计算机领域，这是因为将4个位元（Bit）化成单独的16进制数字不太困难。1字节可以表示成2个连续的16进制数字。可是，这种混合表示法容易令人混淆，因此需要一些字首、字尾或下标来显示。

## ASCII编码：美国信息交换标准代码
产生原因：

在计算机中，所有的数据在存储和运算时都要使用二进制数表示（因为计算机用高电平和低电平分别表示1和0），例如，像a、b、c、d这样的52个字母（包括大写）以及0、1等数字还有一些常用的符号（例如*、#、@等）在计算机中存储时也要使用二进制数来表示，而具体用哪些二进制数字表示哪个符号，当然每个人都可以约定自己的一套（这就叫编码），而大家如果要想互相通信而不造成混乱，那么大家就必须使用相同的编码规则，于是美国有关的标准化组织就出台了ASCII编码，统一规定了上述常用符号用哪些二进制数来表示[2]。

表达方式：

ASCII 码使用指定的7 位或8 位二进制数组合来表示128 或256 种可能的字符。标准ASCII 码也叫基础ASCII码，使用7 位二进制数（剩下的1位二进制为0）来表示所有的大写和小写字母，数字0 到9、标点符号，以及在美式英语中使用的特殊控制字符 [1]  。

其中：0～31及127(共33个)是控制字符或通信专用字符（其余为可显示字符），如控制符：LF（换行）、CR（回车）、FF（换页）、DEL（删除）、BS（退格)、BEL（响铃）等；通信专用字符：SOH（文头）、EOT（文尾）、ACK（确认）等；ASCII值为8、9、10 和13 分别转换为退格、制表、换行和回车字符。它们并没有特定的图形显示，但会依不同的应用程序，而对文本显示有不同的影响 [1]  。

32～126(共95个)是字符(32是空格），其中48～57为0到9十个阿拉伯数字。

65～90为26个大写英文字母，97～122号为26个小写英文字母，其余为一些标点符号、运算符号等。

同时还要注意，在标准ASCII中，其最高位(b7)用作奇偶校验位。所谓奇偶校验，是指在代码传送过程中用来检验是否出现错误的一种方法，一般分奇校验和偶校验两种。奇校验规定：正确的代码一个字节中1的个数必须是奇数，若非奇数，则在最高位b7添1；偶校验规定：正确的代码一个字节中1的个数必须是偶数，若非偶数，则在最高位b7添1 [1]  。

后128个称为扩展ASCII码。许多基于x86的系统都支持使用扩展（或“高”）ASCII。扩展ASCII 码允许将每个字符的第8 位用于确定附加的128 个特殊符号字符、外来语字母和图形符号 [1]  。
![image](https://user-images.githubusercontent.com/26539681/142962309-3a79700c-0ccc-47d4-813d-27f29395d07b.png)

问题：

在英语中，用128个符号编码便可以表示所有，但是用来表示其他语言，128个符号是不够的。比如，在法语中，字母上方有注音符号，它就无法用 ASCII 码表示。于是，一些欧洲国家就决定，利用字节中闲置的最高位编入新的符号。比如，法语中的é的编码为130（二进制10000010）。这样一来，这些欧洲国家使用的编码体系，可以表示最多256个符号 [5]  。

但是，这里又出现了新的问题。不同的国家有不同的字母，因此，哪怕它们都使用256个符号的编码方式，代表的字母却不一样。比如，130在法语编码中代表了é，在希伯来语编码中却代表了字母Gimel (ג)，在俄语编码中又会代表另一个符号。但是不管怎样，所有这些编码方式中，0--127表示的符号是一样的，不一样的只是128--255的这一段 [5]  。

至于亚洲国家的文字，使用的符号就更多了，汉字就多达10万左右。一个字节只能表示256种符号，肯定是不够的，就必须使用多个字节表达一个符号。比如，简体中文常见的编码方式是 GB2312，使用两个字节表示一个汉字，所以理论上最多可以表示 256 x 256 = 65536 个符号 [5]  。

## WPF入门必备 -》数据驱动UI
首先熟悉常用控件的基本使用、然后资源样式、模板（控件模板与数据模板、面板模板）、各种数据绑定、Command命令、MVVM、Prism框架的DelegateCommand/MVVMLight的RelayCommand 。

通信组件：Socket(网口(TcpClient、UdpClient))、SerialPort(串口)；电气接口：网口RJ45、串口232/422/485；

上位机常见通信协议：Modbus(通信库NModbus)、S7(通信库s7.net)、Fins、BACnet、Can、MQTT

(重点)通信协议入门：***理解协议报文结构，报文的组装与请求响应。***

Modbus协议的分类：协议的本质=>一组传输数据的格式，字节操作。

 1)网口：***ModbusTCP***、ModbusUDP  --  RTU Over TCP
 
 2)串口：***ModbusRTU、ModbusAscii***
 
 模拟工具 辅助软件：Modbus Slave（从机模拟）、Modbus Poll（主机模拟）、Configure Virtual Serial Port Driver(串口仿真)
 ![image](https://user-images.githubusercontent.com/26539681/143185554-201b275f-62b4-49cc-805b-543b57650345.png)

一、资源样式：静态资源和动态资源、样式定义、样式触发器。

二、模板：WPF中有三大模板ControlTemplate,ItemsPanelTemplate,DataTemplate.其中ControlTemplate和ItemsPanelTemplate是控件模板，DataTemplate是数据模板，他们都派生自FrameworkTemplate抽象类。

 1) 控件模板：针对于控件本身，修改它可以改变控件本身表现的样子。

 2) 数据模板：针对控件的数据，修改它可以改变控件绑定的数据表现样子，一般应用于数据绑定控件。
 
 3) 面板模板：针对控件的布局，修改它可以改变控件的布局方式。

三、依赖属性、附加属性：

四、数据绑定(源对象[任意类型]-》绑定-》目标对象[必须是依赖属性])：

 1) 对象间的绑定：
 
    a) UI与UI(xaml)
    
    b) UI与.net对象(代码)
 
 2) 绑定到集合-》ItemsSource。
 
    注1：对于.NET集合/对象来说，它不具备UI目标属性与源数据同步。为了让目标属性与源集合的更改保持同步，源集合必须实现一个叫INotifyCollectionChanged的接口，但通常我们只需要将集合类继承于ObservableCollection类即可。因为ObservableCollection实现了INotifyPropertyChanged和INotifyCollectionChanged接口。
 
    注2：DataContext是数据上下文对象，它是为了避免多个对象共享一个数据源时重复的对所有对象显示地用binding标记每个Source/RelativeSource/ElementName，而把同一个数据源在上下文对象的某个范围内共享，这样当一个绑定没有显示的源对象时，WPF会遍历逻辑树找到一个非空的DataContext为止。
    
 3) RelativeSource：Self/TemplatedParent/AncestorType

五、MVVM：

MVVM是Model、View、ViewModel的简写。这种模式的引入就是使用ViewModel来降低View和Model的耦合。Model就是一个class，是对现实中事物的抽象，开发过程中涉及到的事物都可以抽象为Model。View很好理解，就是界面。ViewModel就是对View的抽象，显示的数据对应着ViewMode中的Property，执行的命令对应着ViewModel中的Command。

六、Command命令：WPF中使用命令的步骤：创建命令-》绑定命令-》设置命令源-》设置命令目标

  1)自定义Command
  
  2)预定义Command
  
 七、路由事件
 
 路由事件是一种可以针对元素树中的多个侦听器而不是仅仅针对引发该事件的对象调用处理程序的事件，也就是说，触发事件源的父级或子级如果都有对该事件的监听，则都能触发事件。
 
 路由事件与一般事件的区别在于：路由事件是一种用于元素树的事件，当路由事件触发后，它可以向上或向下遍历可视树和逻辑树，他用一种简单而持久的方式在每个元素上触发，而不需要任何定制的代码（如果用传统  的方式实现一个操作，执行整个事件的调用则需要执行代码将事件串联起来）。
 
 路由事件一般使用以下三种路由策略：

 1)冒泡：由事件源向上传递一直到根元素。RoutingStrategy.Bubble

 2)直接：只有事件源才有机会响应事件。RoutingStrategy.Direct

 3)隧道：从元素树的根部调用事件处理程序并依次向下深入直到事件源。RoutingStrategy.Tunnel

 一般情况下，WPF提供的输入事件都是以隧道/冒泡对实现的。隧道事件常常被称为Preview事件
  
## 内置的 WPF 控件。
按钮：Button 和 RepeatButton。

数据显示：DataGrid、ListView 和 TreeView。

日期显示和选择：Calendar 和 DatePicker。

对话框：OpenFileDialog、PrintDialog 和 SaveFileDialog。

数字墨迹：InkCanvas 和 InkPresenter。

文档：DocumentViewer、FlowDocumentPageViewer、FlowDocumentReader、FlowDocumentScrollViewer 和 StickyNoteControl。

输入：TextBox、RichTextBox 和 PasswordBox。

布局：Border、BulletDecorator、Canvas、DockPanel、Expander、Grid、GridView、GridSplitter、GroupBox、Panel、ResizeGrip、Separator、ScrollBar、ScrollViewer、StackPanel、Thumb、Viewbox、VirtualizingStackPanel、Window 和 WrapPanel。

媒体：Image、MediaElement 和 SoundPlayerAction。

菜单：ContextMenu、Menu 和 ToolBar。

导航：Frame、Hyperlink、Page、NavigationWindow 和 TabControl。

选择：CheckBox、ComboBox、ListBox、RadioButton 和 Slider。

用户信息：AccessText、Label、Popup、ProgressBar、StatusBar、TextBlock 和 ToolTip。

## 控件分类
    布局控件：容器控件，排列和组织其他控件，其父类是Panel
    
    内容控件：只能容纳一个控件或布局控件作为他的内容，父类是ContentControl
    
    带标题内容控件：只能容纳一个控件或布局控件作为他的内容，可以加一个标题，父类是HeaderedContentControl
    
    条目控件：  可以显示一列数据，数据类型一般相同，父类是ItemControl
    
    带标题的条目控件：  可以显示一列数据，数据类型一般相同，可以设置标题，父类是HeaderedItemControl
    
    特殊内容控件：这类控件比较独立，但也比较常用，如TextBox PasswordBox TextBlock Image等
  
    第三方WPF控件
    
## WPF常用布局控件
1、Grid：网格。可以自定义行和列并通过行列的数量、行高列宽来调整控件的布局。近似Html中的table， 就犹如：

![image](https://user-images.githubusercontent.com/26539681/141948955-1ce5880e-83a6-4d5f-ad16-fcb2cfe630af.png)

2、DockPanel：泊靠式面板。内部元素可以选择泊靠的方向（上下左右），类似于Winform中设置控件的Dock属性，就犹如：

![image](https://user-images.githubusercontent.com/26539681/141949021-26ca7984-4011-4605-826d-96ac64c2c01a.png)

3、StackPanel：栈式面板。可将包含的元素在水平或垂直方向排成一条线，当移除一个元素后，后面的元素会自动向前填充空缺。

![image](https://user-images.githubusercontent.com/26539681/141949062-74157ac0-1425-41a7-9ac5-a0dac0ed2a5f.png)

4、WrapPanel：自动折行面板。内部元素在排满一行后能够自动折行，类似于Html中的流式布局。

![image](https://user-images.githubusercontent.com/26539681/141949117-e0eb7f61-a648-42f3-8713-38404d984915.png)

5、Canvas：画布。内部元素可以使用以像素为单位的绝对坐标进行定位，类似于Windows Form 的布局方式。

![image](https://user-images.githubusercontent.com/26539681/141949155-812de355-a69a-42be-94cc-2ba2260d505e.png)

## WPF窗体的生命周期
![image](https://user-images.githubusercontent.com/26539681/142174602-67e43e04-73d0-48cb-907b-8956a094ec66.png)




