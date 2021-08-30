# EDK2 UEFI Firmware For Snapdragon 835 (MSM8998)

## WARNING

**DO NOT EVER TRY TO PORT IT TO *SONY* and *GOOGLE* DEVICES**
**YOUR UFS WILL BE ERASED**

Basic edk2 implementation for msm8998, heavily based on lumingyu0423:s work with some really small modifications and added devices.
Currenly supported devices:
OnePlus 5 and 5T (cheeseburger, dumpling)
Xiaomi Mi6 (sagit)
Xiaomi Mi Mix 2 (chiron)


Windows crashes because all 8 cores are enabled. With only single core enabled it can load, but drivers cause lun0 getting erased from UFS.
