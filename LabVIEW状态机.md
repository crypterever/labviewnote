# 状态机

## 顺序编程

- 使用错误簇强行指定程序执行顺序![image-20200826210320880](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826210320880.png)

- 如需强行指定执行顺序，请使用顺序结构，由多个帧组成的结构，按照帧的先后顺序执行

![image-20200826210405678](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826210405678.png)

尽管顺序结构或顺序连接子`VI`可完成任务，但对于下列情况并非理想选择：

- 需改变执行顺序时
- 需重复执行顺序结构中某一帧时
- 需仅在满足一定条件时才执行某几帧时
- 需立即停止程序，而不是等待最后一帧执行完毕才结束程序时

## 基本结构

- 状态机由状态的集合以及对应状态切换的转换函数构成
- 每个状态可触发一个或多个状态或结束进程处理

![image-20200826211448032](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826211448032.png)

## 默认转移

![image-20200826211749062](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826211749062.png)

## 状态转移

![image-20200826211814832](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826211814832.png)

## 条件结构转移

![image-20200826211848510](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826211848510.png)

## 转换数组转移

![image-20200826211931278](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826211931278.png)

## 示例

![image-20200826212521402](https://gitee.com/zr001/writeimges/raw/master/images/image-20200826212521402.png)