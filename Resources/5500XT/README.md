# Asrock Radeon RX 5500 XT Challenger D 8G OC 注入优化

## 如果你的显卡也是 5500 XT，但是品牌不同

* 只需要修改 config.plist 里面 DeviceProperties -> PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0) 里面值有 Python 的 把 Python 替换为 Boa, 5500 XT 基本就是这两个值