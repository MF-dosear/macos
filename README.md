## OpenCore黑苹果EFI

### 电脑配置
```swift
主板：微星PRO B660M-G DDR4参数
CPU：i5-12490F
显卡：蓝宝石Radeon RX 6600 8G 白金版
内存：阿斯加特 弗雷 16GB x 2
固态：金士顿KC3000 512GB
风扇：利名AS120
电源：微星MAG A650BN 铜牌650W
WiFi/蓝牙：奋威FV-HB1200（蓝牙不稳定，返厂中...）
```

### 特别提醒
* 1、安装前请认真阅读[黑苹果安装网站](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/opencore-efi.html)内容，少走弯路，否则熬夜一周也搞不定黑苹果系统。
* 2、确定微星PRO B660M-G DDR4主板BIOS版本，当前只建议**7D45V13**版本
* 3、安装前认真设置BIOS（参考[黑苹果安装网站](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/opencore-efi.html)），否则可能引导界面都进不去。
* 4、同配置可以用我的EFI，其他配置参考网站编写。
* 5、建议官方下载完整系统制作U盘安装，在线安装下载很慢，失败重来特别费时间。
* 6、有其他问题，可以关注我的抖音（**抖音号：dosear**）私信我解答。

## 以下是我电脑配置详情
### 主板：微星PRO B660M-G DDR4参数
#### 主板芯片
* **集成芯片**  *声卡/网卡*
* **主芯片组**	*Intel B660*
* **音频芯片**	集成*Realtek ALC897 7.1*声道音效芯片
* **网卡芯片**  板载*Realtek 8125BG 2.5GbE*网卡

#### 处理器规格
* **CPU类型**	*第十二代 Core/Pentium/Celeron*
* **CPU插槽**	*LGA 1700*

#### 内存规格
* **内存类型**	   *2×DDR4 DIMM*
* **最大内存容量**	*64GB*
* **内存描述	支持** *双通道DDR4 4600（OC）/4400（OC）/4266（OC）/4200（OC）/4000（OC）/3800（OC）/3733（OC）/3600（OC）/3466（OC）/3400（OC）/3333（OC）/3200（OC）/3200（JEDEC）/2933（JEDEC）/2666（JEDEC）/2400（JEDEC）/2133（JEDEC）MHz内存*
#### 板型
* **主板板型**	*Micro ATX板型*
* **外形尺寸**	*24.4×22.0cm*
* *软件管理*
* **BIOS性能**	*1x256 Mb flash*
* *UEFI AMI BIOS*
* *ACPI 6.4，SMBIOS 3.4*
* *Multi-language*
#### 存储扩展
* **PCI-E标准**	*PCI-E 4.0*
* **PCI-EX16插槽** *1个*
* **PCI-EX1插槽**	 *1个*
**存储接口**	*2×M.2接口，4×SATA III接口*
#### I/O接口
* *USB（背板）	4×USB3.2 Gen1接口*
* *2×USB2.0接口*
* *USB（内置）	2×USB3.2 Gen1接口*
* *4×USB2.0接口*
* *视频接口	 1×VGA接口，1×HDMI接口，1×DisplayPort接口*
* *电源接口	 一个8针，一个24针电源接口*
* *其它接口 	1×PS/2键鼠通用接口，1×RJ45网络接口，3×音频接口纠*
#### 其它参数
* **多显卡技术**	*支持AMD CrossFire技术*
* **RAID功能**	*支持RAID 0，1，5，10*
* **操作系统**	*Windows 11 64-bit，Windows 10 64-bit*

### CPU：Intel 酷睿 i5-12490F
#### 基本参数
* **CPU系列**  *酷睿i5 12代系列*
* **制作工艺** *Intel 7（10纳米）*
* **核心代号** *Alder Lake*
* **CPU架构** *Golden Cove*
* **虚拟化技术** *Intel VT-x，VT-d，EPT*
* **指令集** *SSE4.1/4.2，AVX2，64bit*

### 显卡：蓝宝石Radeon RX 6600 8G D6 白金版参数
#### 显卡核心
* **芯片厂商**	*AMD*
* **显卡芯片	Radeon** *RX 6600*
* **显示芯片系列**	*AMD RX 6000系列*
* **核心代号**	*Navi 23*
* **核心频率**	*2491MHz*
* **流处理单元**	*1792个*
#### 显存规格
* **显存频率**	*14000MHz*
* **显存类型**	*GDDR6*
* **显存容量**	*8GB*
* **显存位宽**	*128bit*
#### 显卡接口
* **接口类型	PCI** *Express 4.0 16X*
* **I/O接口** *1×HDMI2.1接口，3×DisplayPort1.4接口*
* **电源接口** *8pin*
#### 其它参数
* **显卡类型**	*发烧级*
* **散热方式**	*双风扇散热*
* **产品尺寸**	*193×120×40mm*
* **建议电源**	*500W以上*
## 一、注意事项：系统 macOS Monterey 12.6.3

### 1、macOS 12 及更高版本注意
* **macOS 12 及更高版本**注意：由于最近的 macOS 版本对 USB 堆栈进行了更改，强烈建议您在安装 macOS 之前映射 USB 端口（使用 USBToolBox）。
    * 注意：对于 **macOS 11.3 和更新**版本，XhciPortLimit 被破坏导致启动循环 （打开新窗口）.
    * 如果您已经映射了 USB 端口 （打开新窗口）和 disabled XhciPortLimit，您可以毫无问题地启动 macOS 11.3+。

### 2、在线U盘启动安装

* [U盘在线安装制作](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install-recovery.html)
    * [挂载分区](https://github.com/corpnewt/MountEFI)
    * 分区工具 
    ```
    git clone https://github.com/corpnewt/MountEFI
    cd MountEFI
    chmod +x MountEFI.command
    ```
    * 磁盘查看：默认情况下，磁盘工具仅显示分区 – 按 Cmd/Win+2 显示所有设备

## 二、EFI配置

### 1、Text
#### 必须：Lilu-1.6.4-RELEASE
* **Lilu.text** 必须排第一

#### 必须：VirtualSMC-1.3.1-RELEASE
* **VirtualSMC.text**
* *SMCProcessor.kext 后加*
    * 用于监控Intel CPU温度
    * 不适用于基于 AMD CPU 的系统
    * 需要 Mac OS X 10.7 或更新版本
    
* *SMCRadeonGPU.kext 后加*
    * 用于监控 AMD GPU 系统上的 GPU 温度
    * 需要来自同一存储库的 RadeonSensor
    * 需要 macOS 11 或更高版本
    
* *SMCSuperIO.kex 后加*
    * 用于监控风扇转速
    * 不适用于基于 AMD CPU 的系统
    * 需要 Mac OS X 10.6 或更新版本

#### 图形：WhateverGreen-1.6.4-RELEASE
* **WhateverGreen.kext**
* 用于图形修补、DRM 修复、主板 ID 检查、帧缓冲区修复等；所有 GPU 都受益于这个 kext。
* 需要 Mac OS X 10.6 或更新版本
* 免驱 6000 系显卡已经在 Monterey 下原生支持，已将 WhateverGreen.kext 防黑屏驱动去除，显卡性能已到最优

#### 音频：AppleALC-1.8.0-RELEASE
* **AppleALC.kext**
* AppleALCU.kext 是 AppleALC 的精简版，仅支持数字音频 - 但您仍然可以在纯数字音频系统上使用 AppleALC.kext

#### 以太网：LucyRTL8125Ethernet-V1.1.0
* <u>本机</u>：板载Realtek 8125BG 2.5GbE网卡
* **LucyRTL8125Ethernet.kext**
    * 对于 Realtek 的 2.5Gb 以太网
    * 需要 macOS 10.15 或更新版本

#### USB：USBToolBox-1.1.1-RELEASE
* **USBToolBox.kext**
* **UTBMap.kext** 
* 电脑映射 用工具：Windows.exe

#### 固态NVMe修复：NVMeFix-1.1.0-RELEASE
* **NVMeFix.kext**
* 用于修复非 Apple NVMe 上的电源管理和初始化
* 需要 macOS 10.14 或更新版本
* NVMeFix 至少需要 Lilu 1.4.1 和至少 10.14 系统版本
    
### 蓝牙和WiFi
#### 蓝牙：BrcmPatchRAM-2.6.4-RELEASE
```
BrcmPatchRAM 加载顺序
输入的顺序Kernel -> Add应该是：

BrcmBluetoothInjector（如果需要）
Brcm固件数据
BrcmPatchRAM3（或 BrcmPatchRAM2/BrcmPatchRAM）
BlueToolFixup 可以在 Lilu 之后的任何位置。

然而 ProperTree 会为你处理这个，所以你不必担心自己
```

* *BlueToolFixup.text*
* 修补 macOS 12+ 蓝牙堆栈以支持第三方卡
* 所有非本地（非 Apple Broadcom、Intel 等）蓝牙卡都需要
* 包含在BrcmPatchRAM zip中
* 不要在 macOS 11 及更早版本上使用

#### WiFi：

要使用 OpenCore 启用 AirportItlwm 支持，您需要：

Misc -> Security -> SecureBootModel通过将其设置为Default或其他一些有效值 来启用
这将在本指南后面和安装后指南中讨论：Apple Secure Boot（打开新窗口）
如果您无法启用 SecureBootModel，您仍然可以强制注入 IO80211Family（非常不鼓励）
Kernel -> Force在 config.plist 中设置以下内容（本指南稍后讨论）：

### 显卡 
* agdpmod=pikera 

```
用于在某些 Navi GPU（RX 5000 和 6000 系列）上禁用板 ID 检查，
否则您将看到黑屏。如果你没有 Navi，
请不要使用（即 Polaris 和 Vega 卡不应该使用它）
```

### 补充
* AMD台式机EFI华硕B550M Plus Tuf Gaming重炮手【不带Wifi款】 5600X 6600XT EFI OpenCore Hackintosh
http://imacos.top/2022/07/31/1234-2/

### 参考网址 
* [黑苹果安装详细教程](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/opencore-efi.html)
* *[12490F-MSI-B660M-D4-WIFI-MORTAR-RX6600](https://github.com/abc408880155/12490F-MSI-B660-MORTAR-WiFi-RX6600-EFI-OC0.8.2)*
* [微星PRO B660M-G DDR4+i5-12400F电脑](http://www.imacosx.cn/12117.html)
* [OpenCore intel 12代CPU Adler lake黑苹果指南](https://zhuanlan.zhihu.com/p/487736399)
* [Alder Lake 超频：新功能](https://skatterbencher.com/2021/11/04/alder-lake-overclocking-whats-new/#Disable_Ring_to_Core_Ratio_Offset)
* [alderlake 早起启动失败 ](https://github.com/tarbaII/OpenCore-Install-Guide/blob/alderlake/config-laptop.plist/icelake.md)
* [类似错误](https://www.insanelymac.com/forum/topic/346484-10136-opencore-065-pre-install-stuck-on-amishimtimerboostexit/)
