# EDK2 UEFI Firmware For Snapdragon 835 (MSM8998)

[Chinese version (中文版)](https://github.com/lumingyu0423/edk2-MSM8998/blob/new/README.zh.md)

## Resources

[Telegram group](https://t.me/joinchat/MNjTmBqHIokjweeN0SpoyA)

[Discord group](https://discord.gg/XXBWfag)

QQ chinese group: 697666196 (Main group, full)  996450026 (Second group)  737223105 (Linux/edk2)

[Windows Drivers](https://github.com/edk2-porting/WOA-Drivers)

[Project website](https://renegade-project.org/)

[Project forum](https://forum.renegade-project.org/)

## WARNING

**DO NOT EVER TRY TO PORT IT TO *SONY* and *GOOGLE* DEVICES,**
**YOUR UFS WILL BE WIPED CLEAN!!!**

Basic edk2 implementation for msm8998, heavily based on lumingyu0423:s work with some really small modifications and added devices.

Beware of bugs, broken framebuffers and noob mistakes on code!

## Supported devices

1. OnePlus 5 and 5T (cheeseburger, dumpling)
2. Xiaomi Mi6 (sagit)
3. Xiaomi Mi Mix 2 (chiron)
4. Motorola Moto Z2 Force (nash)
5. LG V30 (joan)

Supported devices(need test)
1. Samsung Galaxy S8 [Snapdragon] (dream)
2. Samsung Galaxy Tab S4 (gts4llte)
3. Asus ZenFone 4 Pro (zs551kl)
4. Nokia 8 Sirocco (NB1)

## Dependencies

For Windows/MacOS/Other Linux distributions:

Install Docker manually or use an Ubuntu virtual machine

For Ubuntu 20.04:

```bash
sudo apt update
sudo apt upgrade
sudo apt install build-essential uuid-dev iasl git nasm gcc-aarch64-linux-gnu abootimg python3-distutils python3-pil python3-git gettext
```

## Building

1.Clone this project

```bash
git clone https://github.com/lumingyu0423/edk2-MSM8998.git --depth=1
cd edk2-MSM8998
```

2.1 Build this project (only on linux)

```bash
bash build.sh --device DEVICE
```

2.2 For Macos/Windows (you can use docker)

````bash
docker-compose run edk2 ./build.sh -d DEVICE
````

3.Boot the image

```bash
fastboot boot boot_DEVICE.img
```

(DEVICE is the codename of your phone.)

Additionally, you can flash the image to recovery to achieve dual-boot.

```bash
fastboot flash recovery boot_DEVICE.img
```

## Credits

`fxsheep` for his original `edk2-sagit`

`strongtz` for maintaining Renegade Project

`BigfootACA` for build script and SimpleInit


