# EDK2 UEFI Firmware For Snapdragon 835 (MSM8998)

## WARNING

**DO NOT EVER TRY TO PORT IT TO *SONY* and *GOOGLE* DEVICES**
**YOUR UFS WILL BE ERASED**

Basic edk2 implementation for msm8998, heavily based on lumingyu0423:s work with some really small modifications and added devices.

Beware of bugs, broken framebuffers and noob mistakes on code!

Currenly supported devices:

OnePlus 5 and 5T (cheeseburger, dumpling)

Xiaomi Mi6 (sagit)

Xiaomi Mi Mix 2 (chiron)

Motorola Moto Z2 Force (nash)

LG V30 (joan)


Windows crashes because all 8 cores are enabled. With only single core enabled it can load, but drivers cause lun0 getting erased from UFS.

## Building

1.Clone this project (no need for recursive)

```bash
git clone https://github.com/UsedNametag/edk2-MSM8998 --depth=1
cd edk2-MSM8998
```

2.Build this project

```bash
bash build.sh --device device
```

3.Boot the image

```bash
fastboot boot boot_device.img
```

(device is the codename of your phone.)

Additionally, you can flash the image to recovery to achieve dual-boot.

```bash
fastboot flash recovery boot_device.img
```
