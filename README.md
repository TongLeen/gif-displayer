# gif-displayer
A LCD displayer that display gif automatically.

# 动图显示器
一个可以显示动图的设备。~~终于可以将gif打印出来了~~

更新中


## 项目结构

本项目由三个子仓库构成，当前仓库是整个项目的目录。

项目分为三个部分：
- 硬件电路——包含设备的物理结构，包括器件的选型、连接方式等；
- 单片机程序——运行在单片机上的程序，用来实现目标功能；
- [数据处理程序](https://github.com/TongLeen/gif-displayer-dataGenTool)——对视频文件进行预处理，并将其下载到设备上。

可点击对应部分进入子仓库。

## 实现方法简述

STM32F103 微控制器作为设备的主控芯片，显示屏(ST7789)和FLASH芯片(W25Q64)，二者均使用SPI总线传输数据。

主控芯片芯片在配置完成显示器和FLASH芯片后，将FLASH中的数据读出，将其写入到显示屏。

~~没错，主控芯片只干了这么一件事：将数据原封不动地从FLASH搬到显示屏~~

实现的具体细节参见子仓库。

## 效果展示

https://github.com/user-attachments/assets/653a8051-c7d4-46b5-ba3f-05c5a5610225

---
