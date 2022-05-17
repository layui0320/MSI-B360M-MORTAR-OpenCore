# MSI-B360M-MORTAR-OpenCore

# 项目不再维护


> 本项目efi基于此修改：https://github.com/SuperNG6/MSI-B360-Big-Sur-EFI

# 硬件介绍
|		硬件			|				型号			|
|:------------------|:-----------------------|
|		CPU			|		i5-8500			|
|		主板			|		B360M MORTAR		|
|		核显			|		UHD630				|
|		显卡			|		NVIDIA Quadro 410 512M|
|		硬盘			|		Samsung 970evo 250G|
|		网卡			|		BCM94360CS2 + bluetooth 4.0	|
|		显示器		|		BenQ EW3270U 4k60hz 	|
| OS			|	macOS BigSur 11.6		|




# EFI介绍

此 EFI 使用iMac19,1机型，微星 B360M 迫击炮 已开启核显硬解(有时间再补充

创建该项目原因是主板自带的DP接口输出有问题（故障原因：正常使用时随机会突然黑屏等几秒又亮屏），所以买了一个便宜的NVIDIA显卡来使用，只是修改了部分参数而已。PS：Quadro 410 512M显存还是不够用，拖动Safari起始页直接占用99% 推荐买1G显存的独显


# BIOS设置

请先确定正在使用的 BIOS 版本，迫击炮`7B23v16` 之后拔掉电源线并且扣掉主板电池等十分钟后进行下面设置：

`SETTINGS`->`高级`->`内建显示配置`->`设置第一显卡 [PEG]`

`SETTINGS`->`高级`->`内建显示配置`->`集显共享内存 [64M]`

`SETTINGS`->`高级`->`内建显示配置`->`集成显卡多显示器 [允许]`


# 使用方法

下载整包后，使用 Clover Configurator （其他工具亦可）选择iMac19,1机型生成新的`三码` + `ROM`，用 ProperTree 打开`/EFI/OC/config.plist`文件，填入到 `PlatformInfo` -> `Generic` 位置中


如果开机画面大小有问题的用工具更改`NVRAM`->`4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14`->`UIScale`的值由`01`改为`02`即可，我设置成02的开机画面会变大，改01就正常了。



# 其他啥的后面有空继续补充。
