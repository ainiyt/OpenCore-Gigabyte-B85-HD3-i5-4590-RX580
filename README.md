# Hackintosh-Gigabyte-B85-HD3-i5-4590-RX580

| 硬件 | 型号 |
| ---- |-----|
| 主板 | B85-HD3 |
| CPU | i5-4590 |
| 显卡 | RX580 |
|WiFi+蓝牙| AX200|


USB已定制 
休眠唤醒正常
开启默认主题

从OpenCore启动到Windows正常。 

--------问题
  - 如果引导Windows过长，可在BIOS中禁用核显（内建显示）。
  
  
config.plist 设置。
 - Windows 相关。

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
