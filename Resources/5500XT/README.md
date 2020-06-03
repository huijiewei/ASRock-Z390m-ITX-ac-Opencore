# Asrock Radeon RX 5500 XT Challenger D 8G OC 注入优化

## 如果你的显卡也是 5500 XT，但是品牌不同

* 如果你使用这个配置没有感觉到卡顿就不需要修改

* 如果感觉到卡顿，修改 config.plist 里面 DeviceProperties -> PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0) 里面值有 Python 的，把 Python 替换为 Boa, 5500 XT 基本就是这两个值

* 我优化了 PP_PhmSoftPowerPlayTable 参数，让风扇最低速度是 15%，你可以使用 20% 速度和 25% 速度的参数，都在本说明文件同目录下的 txt 文件里面的内容，修改 config.plist 里面 DeviceProperties -> PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0) 下的 PP_PhmSoftPowerPlayTable 数据即可

## AMD NAVI 核心显卡 PP_PhmSoftPowerPlayTable 参数生成方式

* 需要进入 Windows 系统
* 下载 GPU-Z：https://www.techpowerup.com/download/techpowerup-gpu-z/
* 使用 GPU-Z 保存显卡 ROM 文件
* 下载 MorePowerTool https://www.igorslab.de/wp-content/uploads/2019/08/MorePowerTool_Setup.exe
* 使用 MorePowerTool 加载 GPU-Z 保存的 ROM 文件
* 不推荐修改任何数据，除了 Fan 标签里面的 PWM Minimum(风扇最小转速百分比)
* 点击 Write SPPT，写入注册表
* 打开注册表编辑器，找到 PP_PhmSoftPowerPlayTable，导出注册表
* 使用编辑器打开导出的注册表，只保留 PP_PhmSoftPowerPlayTable 的数据，然后替换掉空格，逗号，斜杠，回车等特殊字符