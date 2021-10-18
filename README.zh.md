# 骁龙835(MSM8998)的EDK2 UEFI固件

**在编译该项目前，请确定你有一定的Linux常识，以下步骤已经是最简单的方法，如果你看不懂，那么请使用Releases中的编译成品**

## 资源

[Telegram英语交流群](https://t.me/joinchat/MNjTmBqHIokjweeN0SpoyA)

[Discord英语交流群](https://discord.gg/XXBWfag)

QQ中文交流群: 

主群：697666196 (已满，人数小于1900后开放)  
二群：996450026        
摸鱼专用群：737223105（需具有一定知识储备并正确回答入群问题）     
情感交流群：991796138（仅限邀请）       
核心管理群：766060878（暂不开放）     

[Windows 驱动](https://github.com/edk2-porting/WOA-Drivers)

[项目官网](https://renegade-project.org/)

[项目论坛](https://forum.renegade-project.org/)


## 警告

**请勿尝试移植到任何索尼和谷歌设备上**

**你的UFS会被清空!!!**

## 已支持的设备

1. 一加 5 一加5T (cheeseburger, dumpling)
2. 小米手机6 (sagit)
3. 小米手机Mix 2 (chiron)
4. 摩托罗拉 Z2 Force (nash)
5. LG V30 (joan)

待测试的设备：
1. 三星 Galaxy S8 [Snapdragon] (dream)
2. 三星 Galaxy Tab S4 (gts4llte)
3. 华硕 ZenFone 4 Pro (zs551kl)
4. 诺基亚 8 Sirocco (NB1)

## 依赖

Windows/MacOS/其它Linux发行版:

手动安装Docker或者使用Ubuntu虚拟机

Ubuntu 20.04:

```bash
sudo apt update
sudo apt upgrade
sudo apt install build-essential uuid-dev iasl git nasm gcc-aarch64-linux-gnu abootimg python3-distutils python3-pil python3-git gettext
```

## 构建

**不建议使用Ubuntu 18.04版本，请使用Ubuntu 20.04或以上版本**

1.克隆此项目（默认使用国内fastgit镜像加速）

come s∞n...

2.1 编译此项目（默认使用fastgit加速submodule克隆，若不需要请删去 `--chinese`）

```bash
bash build.sh --chinese --device DEVICE
```

2.2 如果你使用MacOS/Windows，则可以借助Docker编译

````bash
docker-compose run edk2 ./build.sh -d DEVICE
````

3.启动镜像

```bash
fastboot boot boot_DEVICE.img
```

(请将DEVICE替换成你的设备代号.)

另外，你可以将UEFI刷写至recovery分区以实现双重启动。

```bash
fastboot flash recovery boot_DEVICE.img
```

## 贡献

感谢`fxsheep`的`edk2-sagit`

感谢`strongtz`维护Renegade Project

感谢`BigfootACA`的编译脚本

感谢`Lemon_Ice`和`NTAuthority`提供指导以及一些有用的blob

感谢`@Freak2112`, `TAO_Croatia`和`废物`的实机调试

感谢`NekokeCore`参与了MemoryMap的修复
