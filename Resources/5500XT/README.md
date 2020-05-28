# Asrock Radeon RX 5500 XT Challenger D 8G OC 注入优化

## 如果你的显卡也是 5500 XT，但是品牌不同

* 如果你使用这个配置没有感觉到卡顿就不需要修改

* 如果感觉到卡顿，请修改 config.plist 里面 DeviceProperties -> PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0) 里面值有 Python 的 把 Python 替换为 Boa, 5500 XT 基本就是这两个值

# 我优化了 PP_PhmSoftPowerPlayTable 参数，让风扇最低速度是 25%，你可以使用 15% 速度和 20% 速度的参数，都在本说明文件同目录下的 txt 文件就是。使用 ProperTree 修改 Kexts/RX5500XT.kext 里面的 info.plist 文件即可