# DeskMini 310 Hackintosh

## 前言

个人自用EFI文件，引用整理了诸多前辈的成果，详细见致谢名单。

## 概述

​		i3-8100集成了UHD630显卡，支持4K输出，苹果的Mac Mini 也是使用的这颗CPU，所以UHD630是免驱的，不需要`WhateverGreen.kext`注入，但如果是使用双屏就需要特别处理了。

​		平时空载时基本在12W左右；普通的网页浏览，文本编辑基本在12W-18W左右；打开多个工程，多个网页，`hexo`生成个静态页面，大概在35W左右；满载时65W左右，

# 配置

|                | 型号                                   |
| -------------- | -------------------------------------- |
| CPU            | i3-8100                                |
| 主板/机箱/电源 | DeskMini 310                           |
| 内存           | **Kingston Impact** DDR4 2666  8G x1   |
| SSD            | **Intel 540S** 128G                    |
| 无线/蓝牙      | **Intel AX200** 双千兆无线网卡         |
| 天线           | **Intel AX200** 双千兆无线网卡套装天线 |
| USB排线        | **杜邦线**：9Pin转双口USB2.0转接线     |
| 显示器         | **AOC U2790PQU**：3840×2160（4K@60Hz） |
| 散热器         | **ID-COOLING IS-30**                   |

### 安装前BIOS的设置

BIOS版本：P4.2

> 1. Load UEFI Defaults
>
> 2. Advanced
>
>    - Onboard HD Audio: Enabled
>
>    - CPU Configuration
>      - CPU C States Support : Enable
>      - CFG LOCK : Disabled
>
>    - Chipset Configuration
>      - VT-d: Disabled
>      - Onboard HD Audio: Enabled
>    - USB Configuration
>      - XHCI Hand-off: Enabled
>    - Super IO Configuration
>      - Serial Port: Disabled
>
> 3. Security
>
>    - Secure Boot: Disabled 
>
> 4. Boot
>
>    - CSM: Disable

## EFI 设置:

 	把启动U盘中的EFI删除，使用新的EFI进行替换(记得修改为自己序列号)，安装过程中WIFI能正常工作。

### 参考

​	https://blog.xjn819.com/post/opencore-guide.html

## 工作状态

- 变频
  - 正常：需要使用Intel Power Gadget工具来查看
- 硬件加速：H.264硬件解码
  - 正常
- 睡眠
  - 正常
- 声音
  - DP接口显示器音频正常
  - 机箱3.5mm音频输出正常
- 4K@60Hz输出
  - 正常
- 无线
  - 正常
- USB&USB2.0扩展&Type C
  - 正常
- 蓝牙
  - 不可用
- AirDrop
  - 不可用

## 截图

