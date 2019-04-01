### SAMA5D27-SOM1 BASICS: How to boot from SD1

Buildroot Video Step by Step Guide for SAMA5D27-SOM1-EK1 available here:

#### Check previous guide to see how and where: 

- Pre Requirements 
- Linux version 
- Find info. on the web
- Required packets
- Git repositories

#### Configure and compile from sources a demo image:
```
BR2_EXTERNAL=../buildroot-external-microchip/ make sama5d27_som1_ek_headless_defconfig
```
#### Change some basic system settings: 
```
make menuconfig

System configuration  --->
        ...
    [*] System hostname
	[*] System Banner
	[*] Root password
```
#### Change bootstrap, uboot and u-env configs:

```
Bootloaders  --->



time make
```

#### Check previous guide to see how and where: 
- Find ready image
- Burn the image to SD card

#### Play with image:
```
sudo minicom -b 115200 -D /dev/ttyS2
```