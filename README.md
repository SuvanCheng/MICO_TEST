# 12864串行显示(stm32)



##  串行接法

![](/reference/串行接法.png)

<img src="/Users/allen/Documents/GitHub/12864/reference/串行接法.png" alt="串行接法" style="zoom:60%;" />

实验器材

* [ ] 战舰STM32F103开发板V3版本

硬件资源

* [ ] DS0(连接在PB5)
* [ ] 串口1(波特率:115200,PA9/PA10连接在板载USB转串口芯片CH340上面)
* [ ] ALIENTEK 2.8/3.5/4.3/7寸TFTLCD模块(通过FSMC驱动,FSMC_NE4接LCD片选/A10接RS)
* [ ] KEY0按键(连接在PE4)/KEY1按键(连接在PE3) 

> 实验现象:
> 本实验开机后,先显示一些提示信息，然后在主循环里面检测两个按键，其中1个按键（KEY1）用来执行写入FLASH的操作，另外一个按键（KEY0）用来执行读出操作，在TFTLCD模块上显示相关信息。同时用DS0提示程序正在运行。另外,本实验可以借助USMART调试。不过切记写入地址不要把用户代码区给写了，否则可能死机。