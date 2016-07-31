## USB2TTL-CH340G

这是采用CH340G芯片的USB转UART模块的KiCAD工程设计文件，同时可以作为Arduino下载器。

#### 目标功能

1. 通用的usb转uart功能
2. 为Arduino下载程序
3. 自由选择3.3V或5V供电和信号电平模式。
4. 电源LED指示、TX和RX的LED指示

#### 原理图

![sch](img/sch.png)

#### PCB

![pcb](img/pcb.png)

#### PCB的3D预览

![sch](img/preview.png)

#### 附：

[CH340](http://www.wch.cn/product/CH340.html) 是一个 USB 总线的转接芯片,实现 USB 转串口、USB 转 IrDA 红外或者 USB 转打印口，其中设计中采用的CH340G是一款只有USB转串口功能的芯片。

##### I. 芯片驱动

1. [windows驱动](http://www.wch.cn/download/CH341SER_ZIP.html)
2. [Mac OSX驱动](http://www.wch.cn/download/CH341SER_MAC_ZIP.html)
3. [Linux驱动](http://www.wch.cn/download/CH341SER_LINUX_ZIP.html)

##### II. 注意

电路完成焊接后，因为稳压二极管的性能误差，可能会造成输出的3.3V不准，电压低于3.2V时可能会造成Mac电脑在使用3.3V的工作模式时UART通信有问题。可以通过更换稳压二极管或者更小阻值的电阻R3来解决。
