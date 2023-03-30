## OpenCore 0.9.0 版本 黑苹果EFI

#### 电脑配置
```swift
主板：微星PRO B660M-G DDR4参数
CPU：i5-12490F
显卡：蓝宝石Radeon RX 6600 8G 白金版
内存：阿斯加特 弗雷 16GB x 2
固态：金士顿KC3000 512GB
风扇：利名AS120
电源：微星MAG A650BN 铜牌650W
WiFi/蓝牙：奋威FV-HB1200
```

#### EFI下载地址
* [https://github.com/MF-dosear/macos](https://github.com/MF-dosear/macos)

#### 特别提醒
* 1、安装前请认真阅读[黑苹果安装网站](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/opencore-efi.html)（英文网站，读不懂就直接翻译），少走弯路，否则熬夜一周也搞不定黑苹果系统。
* 2、确定微星PRO B660M-G DDR4主板BIOS版本，可以去[微星官网](https://store.msicn.com.cn/)（客户服务->售后服务->驱动与下载->选择您的产品）下载，当前只建议**7D45V13**版本
* 3、安装前认真设置BIOS（参考[黑苹果安装网站](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/opencore-efi.html)，一步步设置，千万别用BIOS搜索，有些配置搜索不出来，但是它有这个配置，这里被坑了好久...），否则可能引导界面都进不去。
* 4、同配置可以用[我的EFI](https://github.com/MF-dosear/macos)，其他配置参考网站编写。
* 5、建议官方下载完整系统制作U盘安装（我下载的咋是俄语，边安装边翻译），在线安装下载很慢，失败重来特别费时间。支持macOS，Windows，Linux系统制作。
* 6、有其他问题，可以关注我的抖音（**[抖音号：dosear](https://v.douyin.com/ABPAFFS/)**）私信我解答。

## 开始
### 一、统计硬件参数（越详细越好，以下是我统计的部分参数。懒的话，直接根据我的硬件参数购买硬件）
#### 主板：微星PRO B660M-G DDR4参数
##### 主板芯片
* **集成芯片**  *声卡/网卡*
* **主芯片组**	*Intel B660*
* **音频芯片**	集成*Realtek ALC897 7.1*声道音效芯片
* **网卡芯片**  板载*Realtek 8125BG 2.5GbE*网卡

##### 处理器规格
* **CPU类型**	*第十二代 Core/Pentium/Celeron*
* **CPU插槽**	*LGA 1700*

##### 内存规格
* **内存类型**	   *2×DDR4 DIMM*
* **最大内存容量**	*64GB*
* **内存描述	支持** *双通道DDR4 4600（OC）/4400（OC）/4266（OC）/4200（OC）/4000（OC）/3800（OC）/3733（OC）/3600（OC）/3466（OC）/3400（OC）/3333（OC）/3200（OC）/3200（JEDEC）/2933（JEDEC）/2666（JEDEC）/2400（JEDEC）/2133（JEDEC）MHz内存*
##### 板型
* **主板板型**	*Micro ATX板型*
* **外形尺寸**	*24.4×22.0cm*
* *软件管理*
* **BIOS性能**	*1x256 Mb flash*
* *UEFI AMI BIOS*
* *ACPI 6.4，SMBIOS 3.4*
* *Multi-language*
##### 存储扩展
* **PCI-E标准**	*PCI-E 4.0*
* **PCI-EX16插槽** *1个*
* **PCI-EX1插槽**	 *1个*
**存储接口**	*2×M.2接口，4×SATA III接口*
##### I/O接口
* *USB（背板）	4×USB3.2 Gen1接口*
* *2×USB2.0接口*
* *USB（内置）	2×USB3.2 Gen1接口*
* *4×USB2.0接口*
* *视频接口	 1×VGA接口，1×HDMI接口，1×DisplayPort接口*
* *电源接口	 一个8针，一个24针电源接口*
* *其它接口 	1×PS/2键鼠通用接口，1×RJ45网络接口，3×音频接口纠*
##### 其它参数
* **多显卡技术**	*支持AMD CrossFire技术*
* **RAID功能**	*支持RAID 0，1，5，10*
* **操作系统**	*Windows 11 64-bit，Windows 10 64-bit*

#### CPU：Intel 酷睿 i5-12490F
##### 基本参数
* **CPU系列**  *酷睿i5 12代系列*
* **制作工艺** *Intel 7（10纳米）*
* **核心代号** *Alder Lake*
* **CPU架构** *Golden Cove*
* **虚拟化技术** *Intel VT-x，VT-d，EPT*
* **指令集** *SSE4.1/4.2，AVX2，64bit*

#### 显卡：蓝宝石Radeon RX 6600 8G D6 白金版参数
##### 显卡核心
* **芯片厂商**	*AMD*
* **显卡芯片	Radeon** *RX 6600*
* **显示芯片系列**	*AMD RX 6000系列*
* **核心代号**	*Navi 23*
* **核心频率**	*2491MHz*
* **流处理单元**	*1792个*
##### 显存规格
* **显存频率**	*14000MHz*
* **显存类型**	*GDDR6*
* **显存容量**	*8GB*
* **显存位宽**	*128bit*
##### 显卡接口
* **接口类型	PCI** *Express 4.0 16X*
* **I/O接口** *1×HDMI2.1接口，3×DisplayPort1.4接口*
* **电源接口** *8pin*
##### 其它参数
* **显卡类型**	*发烧级*
* **散热方式**	*双风扇散热*
* **产品尺寸**	*193×120×40mm*
* **建议电源**	*500W以上*

### 二、制作U盘引导（这里采用macOS系统制作，我刚好有本MacBook Pro）

#### 1、命令行软件更新实用程序
* 打开终端窗口，然后复制并粘贴以下命令：
```swift
softwareupdate --list-full-installers;echo;echo "Please enter version number you wish to download:";read;$(if [ -n "$REPLY" ]; then; echo "softwareupdate --fetch-full-installer --full-installer-version "$REPLY; fi);
```
<img width="753" alt="commandlinesoftwareupdateutility e1679420" src="https://user-images.githubusercontent.com/20237339/228758162-5f3b0c3c-c102-4b2c-bd9b-cd09ac1e12ad.png">


#### 2、设置安装程序
现在我们将格式化 USB 以准备 macOS 安装程序和 OpenCore。我们希望使用带有 GUID 分区映射的 macOS Extended (HFS+)。这将创建两个分区：主分区MyVolume和第二个分区EFI，用作引导分区，您的固件将在其中检查引导文件。

* 注意1：EFI通过格式化 USB 创建的分区在您挂载它之前是隐藏的。这将在稍后设置 OpenCore 的 EFI 环境时安装
* 注意2：默认情况下，磁盘工具仅显示分区 – 按 Cmd/Win+2 显示所有设备（或者您可以按查看按钮）
* 注意3：使用“Legacy macOS: Online Method”部分的用户可以跳到设置OpenCore的EFI环境
![format-usb 83a24b13](https://user-images.githubusercontent.com/20237339/228757617-712d688a-1086-485a-9be5-52079bc64009.png)


接下来运行苹果createinstallmedia提供的命令 （打开新窗口）. 请注意，该命令是为 USB 格式化的，名称为MyVolume：
```swift
sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```

这将需要一些时间，因此您可能想喝杯咖啡或继续阅读指南（公平地说，您真的不应该在不先阅读整个内容的情况下逐步遵循本指南）。

#### 3、设置 OpenCore 的 EFI 环境

设置 OpenCore 的 EFI 环境很简单——您需要做的就是挂载我们的 EFI 系统分区。这是在我们使用 GUID 格式化时自动生成的，但默认情况下是卸载的，这是我们的朋友[MountEFI](https://github.com/corpnewt/MountEFI)所在的位置 （打开新窗口）进来：
![mount-efi-usb c855475e](https://user-images.githubusercontent.com/20237339/228757856-fecce492-25e7-4384-86c1-0ee71086c6da.png)

您会注意到，一旦我们打开 EFI 分区，它就是空的。这就是乐趣的开始。
![base-efi 3b1f0304](https://user-images.githubusercontent.com/20237339/228757855-44c6d9fc-fa92-485b-bdfa-51e3e406fa48.png)


### 三、配置EFI

#### ACPI
* **SSDT-AWAC.aml**
* **SSDT-EC-USBX-DESKTOP.aml**
* **SSDT-PLUG-ALT.aml**

#### Kexts
* **Lilu.text** 必须排第一
* **VirtualSMC.text**
    * *SMCProcessor.kext*
        * 用于监控Intel CPU温度
        * 不适用于基于 AMD CPU 的系统
        * 需要 Mac OS X 10.7 或更新版本
    
    * *SMCSuperIO.kext*
        * 用于监控风扇转速
        * 不适用于基于 AMD CPU 的系统
        * 需要 Mac OS X 10.6 或更新版本
* **图形：WhateverGreen.kext**
    * 用于图形修补、DRM 修复、主板 ID 检查、帧缓冲区修复等；所有 GPU 都受益于这个 kext。
    * 需要 Mac OS X 10.6 或更新版本
    * 免驱 6000 系显卡已经在 Monterey 下原生支持，已将 WhateverGreen.kext 防黑屏驱动去除，显卡性能已到最优

* **音频：AppleALC.kext**
    * AppleALCU.kext 是 AppleALC 的精简版，仅支持数字音频 - 但您仍然可以在纯数字音频系统上使用 AppleALC.kext

* **以太网：LucyRTL8125Ethernet.kext**
    * 对于 Realtek 的 2.5Gb 以太网
    * 需要 macOS 10.15 或更新版本

* **USB：USBToolBox.kext**
    * **UTBMap.kext** 
    * 电脑映射 用工具：Windows.exe

* **固态NVMe修复：NVMeFix.kext**
    * 用于修复非 Apple NVMe 上的电源管理和初始化
    * 需要 macOS 10.14 或更新版本
    * NVMeFix 至少需要 Lilu 1.4.1 和至少 10.14 系统版本

* **CPU：CPUFriend.kext**
    * **CPUFriendDataProvider.kext**

* **内存显示修复：RestrictEvents.kext**

#### Drivers
* **HfsPlus.efi**
* **OpenCanopy.efi**
* **OpenRuntime.efi**
* **ResetNvramEntry.efi**

#### config.plist文件配置
* 工具：[OCAuxiliaryTools](https://github.com/MF-dosear/macos)，注意OpenCore 0.9.0版本

#### 参考网址 
* [黑苹果安装详细教程](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/opencore-efi.html)
* *[12490F-MSI-B660M-D4-WIFI-MORTAR-RX6600](https://github.com/abc408880155/12490F-MSI-B660-MORTAR-WiFi-RX6600-EFI-OC0.8.2)*
* [微星PRO B660M-G DDR4+i5-12400F电脑](http://www.imacosx.cn/12117.html)
* [OpenCore intel 12代CPU Adler lake黑苹果指南](https://zhuanlan.zhihu.com/p/487736399)
* [Alder Lake 超频：新功能](https://skatterbencher.com/2021/11/04/alder-lake-overclocking-whats-new/#Disable_Ring_to_Core_Ratio_Offset)
* [alderlake 早起启动失败 ](https://github.com/tarbaII/OpenCore-Install-Guide/blob/alderlake/config-laptop.plist/icelake.md)
* [类似错误](https://www.insanelymac.com/forum/topic/346484-10136-opencore-065-pre-install-stuck-on-amishimtimerboostexit/)
