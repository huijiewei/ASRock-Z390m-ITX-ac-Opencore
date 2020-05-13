# Asrock Radeon RX 5500 XT Challenger D 8G OC 注入优化

## 如果你的显卡也是 5500 XT，但是品牌不同

* 只需要修改 config.plist 里面 DeviceProperties -> PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0) 的 4个 @name 的值就可以了, 我使用的是 ATY,Python, 如果进入系统感觉有卡顿，可以试试 ATY,Boa, 5500 XT 基本就是这两个值

## 如果你的显卡不是 5500 XT

1. 删除 DeviceProperties -> PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0), 或者自己找自己的 fbname 注入
2. 使用 https://www.insanelymac.com/forum/topic/343461-kext-tired-of-low-geekbench-scores-use-radeonboost/ 替换 Kexts 目录里面的 RadeonBoost.kext
3. 能耗优化待补充