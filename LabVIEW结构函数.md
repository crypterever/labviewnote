# 顺序结构

- 平铺式顺序结构
  - 执行顺序：从左至右![image-20200825091135390](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825091135390.png)
  - ![image-20200825091003479](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825091003479.png)
- 层叠式顺序结构
  - 通过顺序局部变量传递数据![image-20200825091149496](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825091149496.png)
  - ![image-20200825091042691](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825091042691.png)



# 条件结构

- 类似于C语言中的if(){}else()和switch{case}语句
- 包括两个及以上子程序框图或分支
- 每次仅执行一个条件分支

![image-20200825154857223](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825154857223.png)

- 可为条件结构指定默认的条件分支
- 如已为`1、2、3`指定条件分支，输入数据`4`时，条件结构将执行默认条件分支
- 右键单击条件结构边框添加、幅值、删除、重排及选择默认分支

![image-20200825155203214](https://gitee.com/zr001/writeimges/raw/master/images/image-20200825155203214.png)

> `输入和输出隧道`
> - 可创建多个输入/输出隧道
> - 输入数据可供全部条件分支使用
> - 必须为每个条件分支定义各自的输出隧道
> ![image-20200826135143972](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826135143972.png)

# 事件结构

![image-20200826164310613](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826164310613.png)

**用户界面（静态）事件范例**

- 单击鼠标按键
- 单击键盘按键
- 修改数值控件的值
- ![image-20200826164442178](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826164442178.png)

- 事件选择器标签- 识别当前查看的事件分支

- 超时- 等待某个事件发生的事件：默认值为1，即永不超时
- 事件数据节点识别事件发生时LabVIEW提供的数据；与按名称接触捆绑函数类似
- 事件过滤节点识别在事件数据节点中，事件分支可修改的部分数据

![image-20200826164632071](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826164632071.png)

![image-20200826171438291](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826171438291.png)

**通知事件**

- 用户操作已经发生
- `LabVIEW`已处理了事件
- 仅用于事件数据节点

**过滤事件**

- 用户操作已经发生
- `LabVIEW`尚未处理事件
- 允许用户覆盖事件的默认动作

- 可用于事件过滤节点和事件数据节点

> 通常用于`While`循环![image-20200826172414923](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826172414923.png)

# 事件结构的应用

**阿拉丁神灯**

- 点击阿拉丁神灯，出现阿拉丁，询问主人有何吩咐
- 没有任何吩咐，点击退下，阿拉丁隐身
- 点击停止按钮，程序停止

> ![image-20200826175330489](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826175330489.png)
>
> ![image-20200826175443359](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826175443359.png)

## 移位寄存器

### 移位寄存器的应用

- 使用循环结构编程时，经常需要访问前一次循环产生的数据
- 移位寄存器将前一循环产生的数据传递至下一循环
- ![image-20200813211045681](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813211045681.png)
- 右键单击循环边框，从快捷菜单选择`添加移位寄存器`
- 右侧的移位寄存器存储每一次循环结束后的数据

- 左侧的移位寄存器为下一循环提供所存储的数据
- ![image-20200813211239703](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813211239703.png)

### 移位寄存器的初始化问题

- ![image-20200813211456052](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813211456052.png)

### 使用移位寄存器判断值是否更改

- 在`while循环`中利用移位寄存器判断值是否有改变
- ![image-20200813212612232](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813212612232.png)



# 属性节点

- 属性节点用于访问对象的属性
- 在某些应用中可能需要通过编程改变前面板对象外观，以响应特定输入
  - 当用户输入无效密码时，红色指示灯开始闪烁
  - 当数值值高于指定值时，线条显示为红色而不是绿色
- 通过编程属性节点可完成上述改动
- 属性节点按照由上而下的顺序执行
- 如某接线端出错，节点将在此处中止执行。返回错误消息并不再继续执行后续接线端。
  - 如要更改默认设置，可单击右键，选择忽略节点内部错误
  - ![](https://gitee.com/zr001/writeimges/raw/master/images/20200815185228.png)-
- `严格属性节点`：右键控件选择创建`引用`，进行连接。![image-20200815190228713](https://gitee.com/zr001/writeimges/raw/master/images/image-20200815190228713.png)
  - 控件的属性可以使用隐式连接的方法直接访问，也可以使用引用来访问
  - `VI`和应用程序本身的属性必须通过引用接入相应节点的方式访问
  - 显示内存中所有已经打开的`VI`的文件名，并且返回这些文件在磁盘上的路径

## 属性节点的应用

![image-20200819204646865](https://gitee.com/zr001/writeimges/raw/master/images/image-20200819204646865.png) 

## 调用节点的创建

调用节点

- 调用节点可用于执行引用的项的操作和方法
  - VI
  - 输入控件
- 大部分方法均带有相关参数
  - ![image-20200819205013138](https://gitee.com/zr001/writeimges/raw/master/images/image-20200819205013138.png)

- 使用`VI`服务器引用，关联调用节点和当前`VI`

- 创建一个`VI`方法
  - 放置一个`VI`服务器引用函数，选择本`VI`
  - 单击右键，从快捷菜单中选择创建》》类的方法，并选择所需的方法

![image-20200820133143697](https://gitee.com/zr001/writeimges/raw/master/images/image-20200820133143697.png)

- 要创建隐式链接调用节点，右键单击控件，从快捷菜单选择创建》》调用节点并选择方法

- 控件常见的方法为“重新初始化为默认值”方法

# 变量的应用

## 并行 

- 从文件中读取停止按钮的值
  - 每个循环独立访问文件
  - 但读写文件会占用大量的处理器时间
  - 通过连线无法在并行循环间传递数据

![](https://gitee.com/zr001/writeimges/raw/master/images/20200813192716.png)

![](https://gitee.com/zr001/writeimges/raw/master/images/20200813200809.png)

## 变量类型：

- `局部变量`：将数据存储在前面板输入控件和显示控件中（单个`VI`传递数据）
- `全局变量`：将数据存储在多个`VI`可访问的特殊数据库中

- `功能全局变量`：将数据存储在`while`循环移位寄存器中
- `共享变量`：在通过网络连接的分布式任务间传递数据

## 使用局部变量在单个`VI`中传递数据

![](https://gitee.com/zr001/writeimges/raw/master/images/20200813202209.png)

> `作用`：使得两个循环同事停止

## 布尔型控件

- 具有关联局部变量的布尔控件必须使用开关机械动作
- 布尔触发动作与局部变量不兼容![image-20200813202605027](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813202605027.png)

## 局部变量的创建

- 点击控件右键创建`局部变量`

- ![image-20200813202930614](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813202930614.png)

  > 点击之后`所创建的局部变量`会出现一系列的可以创建局部变量的控件
  >
  > 对于`布尔控件`：需要选择对应的机械动作，才能创建局部变量`不出错`![image-20200813203428119](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813203428119.png)![image-20200813204648213](https://gitee.com/zr001/writeimges/raw/master/images/image-20200813204648213.png)