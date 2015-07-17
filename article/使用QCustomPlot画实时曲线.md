#使用QCustomPlot画实时曲线

##项目当中的实际情况

FID的检测信号通过信号放大电路板，然后通过主接口板的二级放大电路，到达AD采集芯片的输入端，ADS1271作为AD采集芯片通过SPI与FPGA通信，FPGA接收到AD采集芯片的数字信号，通过串口功能发送到天嵌E8（Linux+QT系统环境）的板子。现在需要将FID的检测信号的变化通过实时曲线显示出来。怎么样才能够肩负起这样伟大的历史使命呢？

##QCustomPlot与Qwt

从功能上来看，这两者都能够达到显示实时曲线的目的。QCustomPlot画实时曲线参照官方给出来的Real Time Data Demo，代码的注释写的很清楚，能够在自己的项目当中实现快速的调用。具体的使用例子可以参考其他的文档，[qt超强精美绘图控件-QCustomPlot一览及安装使用教程 ](http://blog.csdn.net/czyt1988/article/details/10143141)。如下图为Real Time Data Demo运行后的效果图。


<center>![](../Image/setupRealtimeDataDemo.png)</center>

Qwt在画实时曲线方面相对QCustomPlot来说就显得复杂一些，官方给出来的Demo也很复杂，而且官方的参考文档也是由doxygen生成的，关于如何使用说的不是很详细。Qwt的显示分为曲线图、散布图、等高线图、柱状图和刻度盘、罗盘、把手、轮子、滑块等图形控件，这里根据需求对曲线图Curve Plots深入了解。






