![App Icon](app/src/main/res/mipmap-xxxhdpi/ic_launcher.png)

# Android DVB-T Driver

This driver provides a simple TCP based API that allows controlling USB DVB-T/DVB-T2 tuners on Android. It gives other apps access to the raw DVB MPEG-2 TS stream.<br>

The driver is a simplified user space port of a subset of the V4L2 Linux kernel drivers. Under the hood it uses Android USB Host API with a small helper library that allows fast kernel controlled USB bulk transfers.

## Supported hardware

This driver version is forked to support the following DVB-T devices:

1. Realtek RTL2832U:
  - 1164:3284 - UPMOST DVB171 USB DVB-T dongle
  - 282d:0608 - FunUV TV1520 USB DVB-T dongle

2. ITE IT9135:<br>
  - 1d19:110b - FunUV TV9135 USB DVB-T dongle
  - 1d19:110c - OEO Design iDTV S Android MobileTV dongle (Dexatek OEO5220)

PS. To use these USB DVB-T dongles on Linux, please add the Product ID information to the `dvb-usb-rtl28xxu` or `dvb_usb_af9035` kernel module.
* <https://github.com/torvalds/linux/blob/master/include/media/dvb-usb-ids.h>
* <https://github.com/torvalds/linux/blob/master/drivers/media/usb/dvb-usb-v2/rtl28xxu.c>
* <https://github.com/torvalds/linux/blob/master/drivers/media/usb/dvb-usb-v2/af9035.c>

## Apps that use the driver

* [Aerial TV](https://play.google.com/store/apps/details?id=info.martinmarinov.aerialtv): This app has been verified to be able to scan and play digital TV channels of Taiwan.  
<img src="https://raw.github.com/denir-li/AndroidDvbDriver/master/graphics/AerialTV-Scan.png" width="270" alt="Aerial TV - Scan"/>  
<img src="https://raw.github.com/denir-li/AndroidDvbDriver/master/graphics/AerialTV-Play.png" width="270" alt="Aerial TV - Play"/>

* [DVBT Televizor](https://github.com/petrj/DVBTTelevizor): Scan settings for Taiwan digital TV channels: Press the buttons in the sequence "Tune" > "DVBT" > "Manual scan". Then, select "DVBT", set the Bandwidth to 6 MHz, and configure the Frequencies from 533 MHz to 596 MHz.  
<img src="https://raw.github.com/denir-li/AndroidDvbDriver/master/graphics/DVBTTelevizor.png" width="270" alt="DVBT Televizor"/>

## Reference

* [OEO Design | iDTV S](https://web.archive.org/web/*/http://www.oeodesign.com/idtvs)
* [Air DTV](https://web.archive.org/web/*/https://play.google.com/store/apps/details?id=com.dexatek.airdtv.player)
* [DVB-Android-Apps Compatibility Chart](https://redeemer.biz/dvb-android-app-compatibility-chart/)
* [ITE IT9135 Devices](https://linuxtv.org/wiki/index.php/ITE_IT9135)
* [DVB-T USB Devices](https://linuxtv.org/wiki/index.php/DVB-T_USB_Devices)
* [FunUV 下載專區](https://web.archive.org/web/*/http://www.funuv.com/download.html)
