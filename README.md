# LC_WPF
## WPF入门必备
首先熟悉常用控件的基本使用、然后资源样式、模板（控件模板与数据模板、面板模板）、各种数据绑定、命令系统、MVVM、Prism框架的DelegateCommand/MVVMLight的RelayCommand 。

资源样式：静态资源和动态资源、样式定义、样式触发器。

模板：

 1) 控件模板：针对于控件本身，修改它可以改变控件本身表现的样子。

 2) 数据模板：针对控件的数据，修改它可以改变控件绑定的数据表现样子，一般应用于数据绑定控件。
 
 3) 面板模板：针对控件的布局，修改它可以改变控件的布局方式。

依赖属性、附加属性：

数据绑定：

 1) 对象间的绑定-》UI与UI(xaml)、UI与.net对象(代码)
 
 2) 对象绑定到集合-》ItemsSource
 
 3) 数据绑定-》Binding

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




