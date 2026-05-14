## 项目简介
西门子杯嵌入式赛项代码
西门子杯 项目 - 基于 GD32F470VET6 的电压采集与存储系统

## 主要功能
- 实时电压采样与显示
- OLED 显示当前时间与电压值
- 按键控制系统参数设置
- SD 卡文件存储与 FATFS 支持
- NOR FLASH 读写
- USB 串口调试输出
- LED 指示与系统自检
- 超限数据记录与隐藏存储模式

## 硬件资源说明
- LED:
  - LED1 - PD1
  - LED2 - PD3
  - LED3 - PD5
  - LED4 - PD7
  - LED5 - PB4
  - LED6 - PB6
- 按键:
  - KEY1 - PE15
  - KEY2 - PE13
  - KEY3 - PE11
  - KEY4 - PE9
  - KEY5 - PE7
  - KEY6 - PB0
  - WK_UP - PA0
- USB 串口 (PA9/PA10，经 CH340 芯片)
- SPI FLASH (GD25Q40):
  - SPI1_SCK  - PB13
  - SPI1_MISO - PB14
  - SPI1_MOSI - PB15
  - SPI1_CS   - PD12
- OLED 模块:
  - SCL - PB8
  - SDA - PB9

## 软件目录结构
- `Drivers/` - 底层外设驱动和 BSP 代码
- `Middlewares/` - FATFS、动态内存等中间件
- `User/` - 用户主程序入口和中断服务文件
- 
## 开发环境
- 目标芯片: `GD32F470VET6`
- 开发工具: Keil MDK-ARM
- 语言: C


## 注意事项
- 串口调试波特率与程序中设置一致，推荐使用 `115200`。
- 若需要通过 USB 下载或调试，请选择 DTR 线，确保 MCU 复位正确。
- 系统运行时须确保按键和 LED 所连接的 IO 引脚与硬件一致。

## 联系与参考
本项目适用于嵌入式系统实验、传感器数据采集、单片机接口学习等场景。如需进一步扩展，可在该基础上添加更多传感器、无线通信或远程数据上传功能。
