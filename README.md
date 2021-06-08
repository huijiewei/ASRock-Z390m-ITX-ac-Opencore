# ASRock Z390m-ITX/ac Hackintosh

## macOS 版本
* 11.4 (20F71)

## Opencore 版本
* 0.7.0

## 硬件配置

* Intel Core i5-9600K 3.70GHz
* ASRock Z390M-ITX/ac (BIOS Version: 4.30)
* USCORSAIR DDR4 3000 16GB (8G×2)
* Intel UHD Graphics 630
* Asrock Radeon RX 5500 XT Challenger D 8G OC (推荐蓝宝石, 华擎的这个一言难尽)
* HP SSD EX920 512GB (macOS 10.15.5)
* HP SSD S700 250GB (Windows 10)
* BCM94360CS2

## BIOS 设置

* Primary Graphics Adapter -> PCI Express
* CFG Lock -> Disabled
* IGPU Multi-Monitor -> Enabled
* XHCI Hand-off -> Enabled
* Secure Boot -> Disabled
* CSM -> Disabled
* Above 4G Decoding -> Disable (这个不使用双显卡的情况下必须关闭, 不然和 CSM 设置冲突, 造成 Windows 无法启动)

## 工作正常

* CPU 变频节能正常
* 休眠唤醒正常
* 核显加速正常
* 5500 XT 显卡性能正常, Geekbench 5.1.1 跑分: Metal Score(41632), OpenCL Score(39026)
* 5500 XT 风扇 PMW 正常
* 有线网卡
* 无线网卡 + 蓝牙
* USB, 使用 USBPorts.kext 定制，自己定制可以删除 USBPorts，然后使用 USBInjectAll 和开启 Kernel->Quirks->XhciPortLimit
* NVRAM（SSDT-PMC.aml）
* iMessage/FaceTime/Hand-off (修改三码)

## 唯一一点不够完美

* 因为苹果驱动的问题，现在还拿不到显卡的监控数据

## 使用说明

* 先修改三码后再使用
* 如果你的 CPU 和我不一样，请到 Windows 下使用 [SSDTTime](https://github.com/corpnewt/SSDTTime) 生成自己的 SSDT-PLUG.aml
* 如果你的独立显卡和我不一样，请注意 [自定义显卡优化参数](Resources/5500XT/README.md)

## 一些图片

![系统信息](./Images/macOS.png "系统信息")
![Metal 跑分](./Images/Metal.png "Metal 跑分")
![OpenCL 跑分](./Images/OpenCL.png "OpenCL 跑分")

## 更新
* 2021-06-08
  * Opencore 升级到 0.7.0
  
* 2021-05-04
  * Opencore 升级到 0.6.9
  * macOS 升级到 11.3.1 (20E241)

* 2021-04-06
  * Opencore 升级到 0.6.8
  
* 2021-03-02
  * Opencore 升级到 0.6.7
  
* 2021-02-04
  * Opencore 升级到 0.6.6
  
* 2021-02-02
  * macOS 升级到 Big Sur 11.2 (20D64)
  
* 2021-01-05
  * Opencore 升级到 0.6.5
  
* 2020-12-08
  * Opencore 升级到 0.6.4

* 2020-11-13
  * macOS 升级到 Big Sur 11.0.1 (20B29)
  
* 2020-11-03
  * Opencore 升级到 0.6.3
  
* 2020-10-06
  * Opencore 升级到 0.6.2
  
* 2020-09-08
  * Opencore 升级到 0.6.1

* 2020-08-05
  * 升级 10.15.6 补丁成功
  * Opencore 升级到 0.6.0
  
* 2020-06-02
  * 升级 10.15.5 补充补丁成功
  * Opencore 升级到 0.5.9

* 2020-05-27
  * 升级到 10.15.5 正常使用
  * 修复 NVRAM 的一些值

* 2020-05-13
  * 首次提交