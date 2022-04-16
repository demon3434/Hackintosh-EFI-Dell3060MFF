# Hackintosh-EFI-Dell3060MFF
## 戴尔3060MFF，黑苹果EFI

### 软件版本
| 软件 | 版本 |
| --- | :--: |
| 系统 | macOS Big Sur 11.6.5 (20G527) |
| 引导 | OpenCore v0.7.9 |

### 自选硬件
|   硬件    |   型号  |
| -------- | :----: |
| 主机 | Dell OptiPlex 3060 MFF |
| CPU | Intel Core i5 8600T |
| 内存 | 杂牌 DDR4 2666 8G*2 |
| 硬盘 | 铠侠TC10，Sata 480GB |
| 显卡 | Intel UHD Graphics 630 |
| 显示器 | DIY便携屏，4K 60Hz |
| 声卡 | ALC255 |
| 无线网卡 | Dell拆机卡（ngff，2个缺口），博通DW1560 |
| WiFi天线 | Dell内置隐形天线 |

### 完成度
+ 核显正常驱动，2048MB显存
+ 声卡可以驱动，但接蓝牙音响声音卡顿
+ Wi-Fi、蓝牙正常驱动。Big Sur 11.6.5 (20G527) 下可以双向隔空投送，反应非常灵敏
+ HDMI、DP接口均能亮屏，VGA接口未测试
+ 睡眠可唤醒
+ USB定制，所有USB接口正常
+ NVMe硬盘装Win10，OC可引导Win10
+ 引导界面图形化，理论上开机应该有“duang”声音，但我的机器没有内置喇叭
+ “关于本机”界面，处理器显示为i5（机型选择Macmini8,1，默认处理器为i7）

### 缺陷
+ 初始安装，使用黑果小兵的镜像 macOS Big Sur 11.5.2 (20G95)，安装完毕未升版本，搜索不到蓝牙音响；升级到11.6.5 (20G527)，蓝牙正常连接音响，但声音时不时地会卡顿，打了[补丁](https://github.com/hackintosh-stuff/ComboJack)仍没有改善，不清楚是硬件问题，还是驱动不完善导致（测试Win10也有此现象）
+ 隔空投送，升级到Monterey，只能接收，不能发送

### 备注
1. PlatformInform 模拟机型，选择 Macmini8,1
2. 建议不要升级Monterey，隔空投送会变成只能接收、不能发送
3. 由于本人使用4K显示器，故设置了UIScale=02；如果用1080P显示器，苹果logo会显得巨大，请自行到nvram的“4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14”中，修改UIScale为01
4. 如需使用此EFI，请***务必重新三码摇号***（适合OpenCore v0.7.9的OCC编辑器已放入本仓库，[图文教程](https://blog.csdn.net/xuanxue11/article/details/107873835)）

### 效果图
![关于本机.png](https://github.com/demon3434/Hackintosh-EFI-Dell3060MFF/blob/main/OpenCore%20v0.7.9%20%26%20macOS%20Big%20Sur%2011.6.5%20(20G527)/1.%E5%85%B3%E4%BA%8E%E6%9C%AC%E6%9C%BA.png "关于本机")
![蓝牙.png](https://github.com/demon3434/Hackintosh-EFI-Dell3060MFF/blob/main/OpenCore%20v0.7.9%20%26%20macOS%20Big%20Sur%2011.6.5%20(20G527)/2.%E8%93%9D%E7%89%99.png "蓝牙")
![Hackintool系统信息.png](https://github.com/demon3434/Hackintosh-EFI-Dell3060MFF/blob/main/OpenCore%20v0.7.9%20%26%20macOS%20Big%20Sur%2011.6.5%20(20G527)/3.Hackintool%E7%B3%BB%E7%BB%9F%E4%BF%A1%E6%81%AF.png "Hackintool系统信息")
