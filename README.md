# ASRock Z390m-ITX/ac Hackintosh

## Opencore 版本
* 0.5.8

## 硬件配置

* Intel Core i5-9600K 3.70GHz
* ASRock Z390M-ITX/ac (BIOS Version: 4.30)
* USCORSAIR DDR4 3000 16GB (8G×2)
* Intel UHD Graphics 630
* Asrock Radeon RX 5500 XT Challenger D 8G OC
* HP SSD EX920 512GB (macOS 10.15.4)
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

* 变频节能正常
* 休眠唤醒正常, 关闭系统节能设置里面的电能小憩，我尚未优化
* 核显加速正常
* 5500 XT 显卡性能正常, Geekbench 5.1.1 跑分: Metal Score(41632), OpenCL Score(39026)
* 有线网卡
* 无线网卡 + 蓝牙
* USB, 使用 USBPorts 定制, 如果你没有定制先使用 USBInjectAll 和打开
* NVRAM（SSDT-PMC.aml）
* iMessage/FaceTime/Hand-off (修改三码)

## 使用说明

* 先修改三码后再使用
* 如果你的 CPU 和我不一样，请到 Windows 下使用 [SSDTTime](https://github.com/corpnewt/SSDTTime) 生成自己的 SSDT-PLUG.aml
* 如果你的独立显卡和我不一样，请注意 [自定义显卡优化参数](Resources/5500XT/README.md)

## 一些图片

![系统信息](Images/macOS.png ''系统信息'')
![Metal 跑分](Images/Metal.png ''Metal 跑分'')
![OpenCL 跑分](Images/OpenCL.png ''OpenCL 跑分'')

## 更新

* 2020-05-13
  * 首次提交