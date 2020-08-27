# 实例一

基于模板打开一个`VI`并运行

> ![](https://gitee.com/zr001/writeimges/raw/master/img/20200805115316.png)

## 窗口介绍

### `LabVIEW`前面板：

- 前面板是VI代码的接口，是用户交互界面，前面板界面上放置了各种图形控件，这些控件主要分为输入控件（`Controls`）和显示控件（`Indicators`）两大类。

- ![](https://gitee.com/zr001/writeimges/raw/master/img/20200805130722.png)

### `LabVIEW`程序框图：

- ![](https://gitee.com/zr001/writeimges/raw/master/img/20200807200819.png)

# **实例二**

## 俄罗斯方块游戏界面

- ***STEP1***：在前面板插入两个空数组和两个布尔控件方形指示，调整两个数组显示为 **4*3**和**10*15**

- ***STEP2***：插入两个字符串显示控件，分别命名为分数和等级

- ***STEP3***：放置一个停止按钮

> ***参考界面***：![](https://gitee.com/zr001/writeimges/raw/master/img/20200807172141.png)

## 未优化结果：
![](https://gitee.com/zr001/writeimges/raw/master/img/20200807173051.png)

# 实例三

## 滤波器程序设计

#### 数据流

- `LabVIEW`按照数据流模型运行`VI`
- 仅当所有输入数据都准备好时，节点才能执行功能
- 仅当节点执行完后才能向输出端提供数据
- ![](https://gitee.com/zr001/writeimges/raw/master/img/20200808081021.png)

#### 数据采集

用于数据采集的`Express VI`：

- DAQ助手`Express VI`<img src="https://gitee.com/zr001/writeimges/raw/master/img/20200808082023.png" style="zoom:67%;" />
- 仪器I/O助手`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082830.png)

- 仿真信号`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082901.png)
- 读取测量文件`VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082923.png)

#### 分析`Express VI`：

- 幅值和电平测量`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082518.png)
- 统计`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082545.png)
- 频谱测量`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082611.png)
- 单频测量`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082635.png)
- 滤波器`Express VI`![](https://gitee.com/zr001/writeimges/raw/master/img/20200808082657.png)

#### 显示

- 执行显示：实现函数功能的`Express VI`或在`VI`前面板显示数据的显示控件
- 显示控件包含波形图表、波形图和`XY`图
- `Express VI`包含写入测量文件`Express VI`、创建文本`Express VI`等

#### 运行

1、放置`Express VI`至程序框图

2、配置弹出的对话框

3、连线`Express VI`

4、保存并运行`VI`

#### 结果

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808092547.png)

# 实例四

## 数值型控件的实际应用

- 数值型数据在温度采集系统中，可以用于设置温度的上下限值；
- 当前温度（监控）与最低温度与最高温度的比较，输出当前状态。

- 温度监控系统中，基于数值型数据应用了程序框图内的比较功能，实现当前状态的输出。

## 结果

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808110653.png)

# 实例五

使用expressVI进行数据的显示（采用数组输出）

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808180449.png)

# 实例六

> 将`while`用于`LabVIEW`图片切换器

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808193219.png)

# 实例七

- `task`：求信号的频率和功率谱，当频率或者采样率发生变化的时候要求重新进行平均过程![image-20200813212037109](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813212037109.png)

- 改用`移位寄存器`

# 实例八

> 任务：
>
> - 监测一天中温室的温度，任意选取50个点作为抽样值
> - 显示当天温度最高值和最低值
> - 将前两个时刻的温度值和当前时刻温度值的平均值作为实时温度，显示温度变化曲线

![image-20200814205145411](https://gitee.com/zr001/writeimges/raw/master/images/image-20200814205157377.png)

![image-20200814205236442](https://gitee.com/zr001/writeimges/raw/master/images/image-20200814205236442.png)

# 实例九

> 交通信号灯

![image-20200821171917545](https://gitee.com/zr001/writeimges/raw/master/images/image-20200821171917545.png)

# 实例十

> 简易抽奖程序
>
> ![image-20200822223512703](https://gitee.com/zr001/writeimges/raw/master/images/image-20200822223512703.png)

![image-20200822223533698](https://gitee.com/zr001/writeimges/raw/master/images/image-20200822223533698.png)

# 实例十一

> ![image-20200823104226750](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823104226750.png)
>
> ![image-20200823104300522](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823104300522.png)
>
> `写入文件中的数据`
>
> ![image-20200823104506289](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823104506289.png)

# 实例十二

>  录音笔程序

![image-20200823213242921](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823213242921.png)

![image-20200823213310153](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823213310153.png)

> 读取录音文件

![image-20200823214037910](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823214037910.png)

![image-20200823214124152](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823214124152.png)

# 实例十三

绘制波形

![image-20200823215108144](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823215108144.png)

指定`初始值`和`时间间隔`

![image-20200823215628241](https://gitee.com/zr001/writeimges/raw/master/images/image-20200823215628241.png)

# 实例十四

> 多种波形数组和簇数组显示的不同
>
> ![image-20200824153526242](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824153526242.png)
>
> ![image-20200824153556673](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824153556673.png)

# 实例十五

>  波形图显示多条曲线与波形图表的区别

![image-20200824204002600](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824204002600.png)

![image-20200824204052664](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824204052664.png)

> 将波形图表列显示使用`数组转置`方法进行转换

![image-20200824204443298](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824204443298.png)

![image-20200824204513043](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824204513043.png)

> 实时更新指定量数据的波形图表

![image-20200824210131588](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824210131588.png)

![image-20200824210229178](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824210229178.png)

> 使用`expressVI`输出到波形图表

![image-20200824212132766](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824212132766.png)

![image-20200824212158994](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824212158994.png)

# 实例十六

> XY图显示单条曲线/多条曲线

![image-20200824220434562](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824220434562.png)

![image-20200824220533707](https://gitee.com/zr001/writeimges/raw/master/images/image-20200824220533707.png)

# 实例十七

使用顺序结构实现跑马灯

![image-20200825120451864](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825120451864.png)

![image-20200825120515851](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825120515851.png)

# 实例十八

**任务要求**

- 产生频率可调、波形类型可设置的信号；
- 以足够的采样率产生和显示波形，并产生采样率可调的波形，以进行比较；
- 显示波形和信号频谱

> ![image-20200825150921016](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825150921016.png)
>
> ![image-20200825151004671](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825151004671.png)

# 实例十九

> ![image-20200826205822152](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826205822152.png)![image-20200826205858951](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826205858951.png)

- 将温度采集报警系统设置为子VI

> ![image-20200826205958451](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826205958451.png)![image-20200826210012847](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826210012847.png)

- 在新`VI`中应用温度采集子`VI`

# 实例二十

> 温度采集系统
>
> - 实时采集当前温度
> - 温度高于上限或低于下限输出报警信息，中暑或冷冻，同时报警灯亮
> - 将采集数据保存到文本文件中
> - 每隔`0.5S`界面更新一次

# 实例二十一 

> <font color=red>任务要求</font>:
>
> - 输出正弦波信号，频率0-50M；
> - 采样率10M、50M、100M可选；
> - 检测信号频率
> - 输出采样信号的功率谱，如果频率或采样率发生变化，重新开始平均过程

![](https://gitee.com/zr001/writeimges/raw/master/img/20200808182954.png)

# 高级实例

- 科学计算器
- 虚拟示波器
- `Simon`游戏设计