# LC_WPF
WPF入门必备：首先熟悉常用控件的基本使用、然后资源样式、模板（控件模板与数据模板）、各种数据绑定、命令系统、MVVM、Prism框架的DelegateCommand/MVVMLight的RelayCommand
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
    布局控件   Panel
    
    内容控件   ContentControl 只能容纳一个控件或布局控件
    
    带标题内容控件  内容控件可以设置标题  Header     父类：HeaderedContentControl
    
    条目控件  可以显示一列数据，数据类型一般相同 ItemControl
    
    带标题的条目控件  条目控件可以设置标题  Header    父类：HeaderedItemControl
    
    特殊内容控件   常用的控件：TextBox PasswordBox TextBlock Image等
  
    第三方WPF控件
    
