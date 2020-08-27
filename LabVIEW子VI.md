# 子`VI`的使用

- `LabVIEW`中模块称为子`VI`
- 模块化就是将程序分为若干区块。这样，对程序某个模块的修改就不会影响到其他模块

> 在`VI`内部被调用的`VI`称为子`VI`
>
> - 子`VI`相当于文本编程语言中的子程序
>
> - 前面板和程序框图右上角均显示`VI`图标
>
> - 图标为程序框图中`VI`的图形化表示
>
>   ![image-20200826180029167](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826180029167.png)
>
>   ![image-20200826180054082](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826180054082.png)
>
>   ![image-20200826180114589](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826180114589.png)

## 图标和连线板

- 创建`VI`后，通过设置图标和连续板可将`VI`用作子`VI`![image-20200826180250886](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826180250886.png)
- 图标和连线板相当于文本编程语言中的函数原型
- 每个`VI`前面板和程序框图的右上角均有一个图标
- 图标是`VI`的图形化表示
- `VI`用作子`VI`时，程序框图上将显示该`VI`的图标

### 较好的`VI`图标

- 一个较好的`VI`图标应具有下列特性
  - 通过以下参数表述`VI`功能：
    - 相关图形
    - 描述性文本![image-20200826180834942](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826180834942.png)

### 创建图标

- 右键单击前面板或程序框图右上角的图标，从快捷菜单选择`编辑图标`或`双击`改图标，可执行图标自定义操作
- 用户也可将系统中的任意图片拖拽至该图标上
- 使用编辑工具手动修改图标
- 点击`符号`选项卡，显示所有可用作图标的图形符号
- 点击`工具`》》`同步ni.com图标库`更新图标
- 使用`图标文本`选项卡，指定图标中的显示文本
- ![image-20200826181318366](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826181318366.png)
- 点击`模板`选项卡，显示可用作图标背景的模板
- ![image-20200826182900796](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826182900796.png)
- ![image-20200826181011535](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826181011535.png)

## 设置连线板

- 右键单击前面板右上角图标，从快捷菜单选择`显示连线板`![image-20200826183046890](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826183046890.png)
  - 连线板上的每个单元格代表一个接线端
  - 使用各接线端分配输入和输出
- 右键单击连线板，从快捷菜单选择`模式`，可选择所需连线模式

## 标准

- 以此连线板布局为标准![image-20200826183547133](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826183547133.png)

- 顶部接线端通常预留为引用接线端，例如文件引用
- 底部接线端通常预留为错误簇![image-20200826183642942](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826183642942.png)

## 使用子`VI`

- 如要放置一个子`VI`至程序框图：
  - 在`函数`选板选择`VI`
  - 选择要用作子VI的VI
  - 双击VI，将其放置在程序框图上
- 如要放置一个已打开的`VI`至另一个打开的`VI`的程序框图：
  - 单击要用作子VI的VI的图标
  - 拖拽此图标至另一VI的程序框图