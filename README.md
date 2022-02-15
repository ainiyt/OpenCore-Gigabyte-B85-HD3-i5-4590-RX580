# Hackintosh-Gigabyte-B85-HD3-i5-4590-RX580

     OpenCore 版本为 0.7.8

| 硬件 | 型号 |
| ---- |-----|
| 主板 | B85-HD3 |
| CPU | i5-4590 |
| 显卡 | RX580 |
|WiFi+蓝牙| AX200|
| SSD | Intel 545s |
|内存 | 威刚DDR3 8*2 |


- USB已定制 
- 休眠唤醒正常
- 开启默认主题

从 OpenCore 启动到 Windows 正常。 

--------问题
  - 如果引导Windows 时间过长，如需要大概黑屏8分钟才能进入系统。
     - 可在BIOS中禁用核显（内建显示）。
- -------PS::  我没有禁用核显，Windows可以正常启动。 -----
- -------Windows和OpenCore的EFI引导文件我是放在同一分区的。----
- ------我使用的是单硬盘双系统 MacOS + Windows 10  ----
  
config.plist 设置。
 - Windows 相关。 防止更改Windows uuid。
 

Kernel > Quirks > CustomSMBIOSGuid > True (默认为 False)

PlatformInfo > UpdateSMBIOSMode > Custom (默认为  Create)

Bios
 禁用
- 快速启动
- 安全启动
- 串行/COM 端口
- Parallel Port
- CSM

启用

- 4G以上解码
- 执行禁用位
- EHCI/XHCI 
- 操作系统类型：Windows 8 UEFI 模式 # CSM 设置为 从不
- DVMT ：256MB
- SATA模式：AHCI
