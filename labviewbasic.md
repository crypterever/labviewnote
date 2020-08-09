# LabVIEW 的基本操作

## 实例 一

基于模板打开一个`VI`并运行

> ![](https://gitee.com/zr001/writeimges/raw/master/img/20200805115316.png)

### 窗口介绍

#### `LabVIEW`前面板：

- 前面板是VI代码的接口，是用户交互界面，前面板界面上放置了各种图形控件，这些控件主要分为输入控件（`Controls`）和显示控件（`Indicators`）两大类。

- ![](https://gitee.com/zr001/writeimges/raw/master/img/20200805130722.png)

#### `LabVIEW`程序框图：

- ![](https://gitee.com/zr001/writeimges/raw/master/img/20200807200819.png)

## **实例二**

### 俄罗斯方块游戏界面

- ***STEP1***：在前面板插入两个空数组和两个布尔控件方形指示，调整两个数组显示为 **4*3**和**10*15**

- ***STEP2***：插入两个字符串显示控件，分别命名为分数和等级

- ***STEP3***：放置一个停止按钮

> ***参考界面***：![](https://gitee.com/zr001/writeimges/raw/master/img/20200807172141.png)

### 未优化结果：![](https://gitee.com/zr001/writeimges/raw/master/img/20200807173051.png)

### 工具选板

> ![](https://gitee.com/zr001/writeimges/raw/master/img/20200807174010.png)
>
> 工具选板包含以下工具，用于操作或修改前面板和程序框图对象
>
> ![](https://gitee.com/zr001/writeimges/raw/master/img/20200807174153.png)

### 程序框图

包含以下对象：

- 接线端
  - 前面板对象的程序框图外观
  - 在快捷菜单中不选显示为图标，更改接线端的显示类型
- 节点
  - 程序框图对象，带有输入和`/`或输出端，并在`VI`运行时执行运算
  - ![](https://gitee.com/zr001/writeimges/raw/master/img/20200807182553.png)
  - `函数节点`
    - `LabVIEW`的基本操作元素
    - 不带有前面板或程序框图，但有连线版
    - 双击函数仅表示选中函数，而双击子VI则直接打开`VI`
  - `子VI节点`
    - 子`VI`：用于另一`VI`内部的`VI`
    - 任何`VI`均可用作子`VI`
    - 双击程序框图中的子`VI`，可查看子`VI`的前面板和程序框图。
      - 前面板和程序框图右上角显示当前`VI`的图标
      - 如`VI`用作子`VI`，程序框图中显示的即为子`VI`的图标。

- 子VI
  - `Experss VI`
    - 一种特殊的子`VI`
    - 所需连线数量少，主要通过对话框配置
    - `Experss VI`配置可保存为子`VI`
  - 程序框图对象间通过连线传输数据
  - 不同数据类型的连线颜色、粗细和样式均有差异
  - 断开的连线显示为中间带有红叉的黑色虚线
  - ![](https://gitee.com/zr001/writeimges/raw/master/img/20200807191022.png)
  - 按下`Ctrl + B`删除程序框图中所以断开连线
  - 单击右键可以选择整理连线![](https://gitee.com/zr001/writeimges/raw/master/img/20200807191909.png)
    - 使用整理程序框图工具，整理已有连线和对象，以增强可读性
      - 1、选中程序框图的一部分
      - 2、单击工具栏部分的整理程序框图按钮![](https://gitee.com/zr001/writeimges/raw/master/img/20200807192133.png)

### 即时帮助

- 鼠标悬停于对象上方时，显示`LabVIEW`对象的基本信息。
- 点击帮助》》显示即时帮助、按下`Ctrl + h`或点击工具栏上的显示即时帮助窗口按钮。

### LabVIEW帮助

- 多数选板、菜单、工具、VI和函数的详细介绍及`LabVEIW`使用说明都在`LabVIEW`的帮助中。
- 打开`LabVIEW`帮助：
  - 点击帮助》 搜索`LabVIEW`帮助。
  - 使用即时帮助窗口的详细帮助信息链接或按钮。
  - 右键单击对象，选择快捷菜单中的帮助项。![](https://gitee.com/zr001/writeimges/raw/master/img/20200807195825.png)

### `NI范例查找器`

- ![](https://gitee.com/zr001/writeimges/raw/master/img/20200807195917.png)

### 修正断开的`VI`

- 常见问题：
  - 断线
    - 将布尔型输入控件与字符串型显示控件相连。
    - 将数值型输入控件与数值型数值型输入控件相连。
  - 必须连接的程序框图接线端断开。
  - 子`VI`断开或将子`VI`图标放置在`VI`程序框图上之后，对连线版进行了编辑。

### 调试技术

`VI未断开，但产生某些未预期数据或事件`

- 是否存在未连线或隐藏的子`VI`？
- 是否使用了不正确的默认数据？

- 是否传递了未定义数据？
- 是否使用了正确的数值表示法？
- 节点执行顺序是否正确？

- ![](https://gitee.com/zr001/writeimges/raw/master/img/20200807200819.png)

### 错误检查和处理

- 虽然开发人员在创建`VI`时，努力确保`VI`的完善性。但用户仍可能碰到不可预期的问题。
- 如果没有错误检查机制，仅能确定`VI`不能正常工作。
- 错误检查能够指出错误发生的原因及位置
  - 手动错误处理
  - 自动错误处理
- `LabVIEW`使用下列方式自动处理`VI`运行中的已知错误：
  - 挂起执行
  - 高亮显示出错的子`VI`或函数
  - 显示错误对话框
- 点击文件》`VI`属性，在类别下拉菜单中选择执行，可禁用指定`VI`的自动错误处理功能
- 如果要禁用子`VI`或函数的自动错误处理功能，可将其错误输出簇与另一子`VI`或函数的错误输入簇连线，或连接错误输出显示控件
- 使用`LabVIEW`错误处理`VI`、函数和参数管理错误![](https://gitee.com/zr001/writeimges/raw/master/img/20200807201756.png)

- 使用错误簇输入控件和显示控件创建子`VI`错误输入和输出
- 错误输入和错误输出簇包含下列信息![](https://gitee.com/zr001/writeimges/raw/master/img/20200807201956.png)
  - 状态
  - 代码
  - 源

## 实例三

### 滤波器程序设计

##### 数据流

- `LabVIEW`按照数据流模型运行`VI`
- 仅当所有输入数据都准备好时，节点才能执行功能
- 仅当节点执行完后才能向输出端提供数据
- ![](https://gitee.com/zr001/writeimges/raw/master/img/20200808081021.png)

##### 数据采集

用于数据采集的`Express VI`：

- DAQ助手`Express VI`<img src="https://gitee.com/zr001/writeimges/raw/master/img/20200808082023.png" style="zoom:67%;" />
- 仪器I/O助手`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082830.png)

- 仿真信号`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082901.png)
- 读取测量文件`VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082923.png)

##### 分析`Express VI`：

- 幅值和电平测量`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082518.png)
- 统计`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082545.png)
- 频谱测量`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082611.png)
- 单频测量`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082635.png)
- 滤波器`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082657.png)

##### 显示

- 执行显示：实现函数功能的`Express VI`或在`VI`前面板显示数据的显示控件
- 显示控件包含波形图表、波形图和`XY`图
- `Express VI`包含写入测量文件`Express VI`、创建文本`Express VI`等

##### 运行

1、放置`Express VI`至程序框图

2、配置弹出的对话框

3、连线`Express VI`

4、保存并运行`VI`

##### 结果

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808092547.png)

## 数值型控件

### 基础知识

- 数值型控件可表示不同类型的数值

- 右键单击输入控件、显示控件或常量，从快捷菜单中选择表示法，改变数值型数据的表示法。![](https://gitee.com/zr001/writeimges/raw/master/img/20200808093039.png)

- 在前面板点击窗口-显示程序框图，从右键菜单中选择表示法，改变数值型数据的表示法。![](https://gitee.com/zr001/writeimges/raw/master/img/20200808093226.png)
- 并可通过右键转换为显示控件、常量![](https://gitee.com/zr001/writeimges/raw/master/img/20200808093258.png)

## 实例四
### 数值型控件的实际应用

- 数值型数据在温度采集系统中，可以用于设置温度的上下限值；
- 当前温度（监控）与最低温度与最高温度的比较，输出当前状态。

- 温度监控系统中，基于数值型数据应用了程序框图内的比较功能，实现当前状态的输出。

### 结果

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808110653.png)

## 布尔型控件

- 按钮型
- 开关型
	- 右键开关型控件可以选择特定的`机械动作``
	- 点击`查找范例`搜索`机械动作`即可查询到相关范例![](https://gitee.com/zr001/writeimges/raw/master/img/20200808124236.png)

## 字符串显示控件

- 可显示或不可显示的`ASCII`字符序列
- 通过快捷菜单更改显示类型：
- 正常显示、‘/’代码显示、密码显示和十六进制显示![](https://gitee.com/zr001/writeimges/raw/master/img/20200808124843.png)

- 字符串类型显示为`粉红色`
- 字符串的数据/控件可以通过程序框图-函数面板-字符串内的函数进行编辑操作和属性修改；![](https://gitee.com/zr001/writeimges/raw/master/img/20200808125343.png)

- 字符串的数据通过字符串面板实现查询、搜索、替换等功能；
- 字符串的数据/控件可以通过数值/字符串转换函数实现字符串与各种类型数值数据之间的转换；![](https://gitee.com/zr001/writeimges/raw/master/img/20200808125710.png)

- 字符串数据/控件也可以与路径、数组之间进行转换

- 字符串控件可以通过函数面板的连接字符串以及制表符、回车/换行符将多个字符串数据转换成指定格式的字符串，用于报表的制作

## 下拉列表和枚举型控件

- 采集电压信号：要在参数设置界面输入数据采样频率 `fs`供后续计算，为用户提供1000,2000,300,4000Hz这样整数的选项进行选择，如何实现？

- 在许多`VI`的程序框图中，枚举和下拉列表常数随处可见。
- 左端带有双向箭头，右端带有下拉箭头的是`枚举常数`；而仅右端带有下拉箭头的是`下拉列表常数`。

### 下拉列表

- 下拉列表控件以下拉菜单的形式出现，用户可在循环浏览的过程中做出选择

- 右键单击下拉列表控件，并从快捷菜单中选择`编辑项`，向控件的下拉列表中添加内容。`下拉列表属性`对话框的`编辑项`选项卡中的项顺序决定了控件中的项顺序。![](https://gitee.com/zr001/writeimges/raw/master/img/20200808160933.png)

### 枚举型控件

- 可以将枚举类型的控件看作下拉列表控件。
- 枚举型的数据类型是：U 8（256）、U 16 （65536）、U 32（更多），括号内是枚举类型可保留的元素数目。

- 将枚举型控件连接至条件结构的选择器接线端时，LabVIEW将控件中的`字符串`与分支条件相比较，而不是控件的数值。
- 当所需要设置的对象的单位为`M`或者其他的时候，可以使用下拉列表类型更加直观，只需要更改`数据类型`和`值`的大小即可。

## 动态数据类型

- 在`LabVIEW`中，动态数据类型表示为<font color=Blue>深蓝色</font>                                                 ![](https://gitee.com/zr001/writeimges/raw/master/img/20200808174037.png)

- 保存由`Express VI`产生或采集的信息，包含与信号相关的数据，以及信号相关的属性信息。例如，信号的名称、采集的日期和时间，等等

- 非`Express VI`无法接受动态数据类型
  - 如果使用内置`VI或函数分析和处理动态数据类型，必须先进行数据类型转换`
  - 如已连线，数值、波形和布尔型数据显示控件或输入端可自动转换动态数据

### 从动态数据类型转换

- 在程序框图上放置"从动态数据转换" `Express VI`时。
- 出现配置对话框，配置对话框显示的选项用于指定如何格式化"从动态数据转换"`Express VI`返回的数据类型。

### 转换至动态数据类型

- 在程序框图上放置"转换至动态数据"`Express VI`

- 在出现的配置对话框中，指定待转换动态数据的转换类型，然后单击确定按钮

### 获取和设置动态数据的属性

- 使用<font color=blue>获取动态数据属性</font>`Express VI`获取动态数据的属性。在程序框图上放置“获取动态数据属性”`Express VI`时，将出现一个配置对话框。使用该对话框获取连接至`Express VI`的动态数据中信号的属性。
- 使用<font color=blue>设置动态数据属性</font>`Express VI`设置动态数据的属性，例如，信号名、时间标识、时间模式、等等。在程序框图上设置“设置动态数据类型属性”`Express VI`时，将出现一个配置对话框、使用该对话框修改或设置连接至`Express VI`的动态数据中的信号的属性。

- 使用`Express VI`，模拟信号输入，在波形图上显示波形，获取采样数据、采样时间和信号名称

## 实例五

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808180449.png)

## 综合应用 1

> <font color=red>任务要求</font>:
>
> - 输出正弦波信号，频率0-50M；
> - 采样率10M、50M、100M可选；
> - 检测信号频率
> - 输出采样信号的功率谱，如果频率或采样率发生变化，重新开始平均过程

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808182954.png)

## 自定义控件的设置

- 右键控件-高级-进入自定义
- 进入控件编辑模式
- 重新设计控件外观，导入图片

## while循环的应用

> 为了进行连续的数据采集或信号输出
>
> - 文本编程语言：`While循环`
>
>   ```c
>   While (1){
>   
>   code
>   
>   }
>   ```
>
> - `LabVIEW`：
>
>   - ![](https://gitee.com/zr001/writeimges/raw/master/img/20200808184457.png)

- 计数接线端：返回已执行循环的次数，从0开始计数

- 条件接线端：定义循环结束条件
  - 红色表示真的时候循环停止
  - 绿色表示真的时候循环继续

### 隧道

- 隧道用于结构间的数据输入和输出
- 隧道根据接入的数据类型更改颜色
- 隧道向循环传送数据时，需所以数据均到达隧道后，循环才能执行

### 应用（修改综合应用1）

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808185910.png)

> 可随时进行数据采集，频率显示

## 实例六

> 将`while`用于`LabVIEW`图片切换器

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808193219.png)

## 时间函数

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808194555.png)

- 已用时间函数：设置循环到指定时间后停止。

## For循环的创建和配置

- 采集温度信号
  - 连续采集------->While循环
  - 采集有限个点