# Lenovo-WEI6-Pro-13-IWL-Hackintosh

> [**中文说明**](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/blob/master/README_CN.MD) | **[English](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/blob/master/README.MD)**
>
> **威 6 Pro/Thinkbook 13s/扬天 S540 QQ交流群**：[681175557](https://jq.qq.com/?_wv=1027&k=54ugIhI)
>
> The author's English is not very good (mainly with the help of translation software). If there is an error, please understand or help correct it. Thank you.

**Extra name for this notebook:**

> - **Lenovo WEI 6 PRO**
> - **Lenovo Thinkbook 13S**
> - **Lenovo S540**

### Warning

The EFI of this repository is limited to macOS `10.14.6`

## Laptop Configuration

| Hardware    | info                                                         |
| ----------- | ------------------------------------------------------------ |
| Motherboard | Lenovo LNVNB161216（300 series）                             |
| CPU         | Intel(R) Core(TM) i7-8565U（UHD Graphics 620）               |
| Memory      | DDR4 8GB 2400MHz Micron（Config needs to inject memory information） |
| DISK        | SSD-HFM512GDHTNG-831（Received feedback, Lenovo S540 series has Micron hard drive, Micron hard drive will not be able to install the system） |
| Graphics    | AMD 540X Series（Blocked ）                                  |
| Monitor     | FHD 1920x1080                                                |
| Sound       | ACL 257                                                      |
| Network     | Intel AC9560（Unable to drive! Please use a USB network card or replace the network card） |
| Trackpad    | Intel I2C HID INT34BB                                        |

## Operating status

| Status | Name                 | info                                                         |
| :----: | -------------------- | ------------------------------------------------------------ |
|   ✔    | Battery              | The functions are normal，[Can set battery conservation mode](#Maybe you need to turn on these features) |
|   ✔    | Camera               | USB custom port：`HS07`                                      |
|   ✔    | Bluetooth            | Either it can't be closed or it can't be opened, I chose to open it (test found that the file can be sent to the phone, but the phone can't send the file to the computer, and Airdrop cannot be used) |
|   ✔    | Speaker / Microphone | `ALC257`,**Counterfeit** ID `11` ,The functions are normal, and the headphone jack is automatically switched.([Shortcut key](#Shortcut key)) |
|   ✔    | Trackpad             | The author has limited ability and only implements polling mode([VoodooI2C、HID](https://github.com/alexandred/VoodooI2C/releases)),Support gesture, support close([Shortcut key](#Shortcut key)),[Need to be set separately, please click me for setup tutorial!](#Touchpad setup tutorial) |
|   ✔    | HDMI                 | The external display is normal (plugged and unplugged many times during the test) |
|   ✔    | Type-C               | USB custom port：`HS03`                                      |
|   ✔    | 3.5mm headphone jack | Supports automatic switching of headset plug and unplug.     |
|   ✔    | USB                  | USB custom port：`HS01`、`HS02`                              |
|   ✔    | CPU Turbo            | Query via CPU-S                                              |
|   ✔    | Brightness           | The EC codes of the shortcut keys `F11` and` F12` are `Q82`,` Q83`. I wrote a hot patch, **but it was invalid**, but there was one [Shortcut key](#Shortcut key) |
|   ❓❌   | Sleep                | After you click Sleep, after a while, the power button flashes white to indicate that you have completely slept, but the system will runs more slowly than before after waking up! There is also a case where it cannot be waked up (directly black screen or restart !!!) |
|   ❌    | Fingerprint          | USB custom blocked                                           |
|   ❌    | Graphics             | Blocked                                                      |
|   ❌    | WIFI                 | Unable to drive                                              |

#### Chance Problem

**1.Sudden restart when entering macOS**

**2.The screen is black after entering the system (but when connecting to HDMI, it will be found that the system has been started, it should be a driver problem)**

>**Workaround**:
>1.Press and hold the power button to restart (use `-v`, etc.)
>2.`Windows system` and `macOS system` switch back and forth
>3.Clover Use `configold.plist` to configure startup.



## Shortcut key
> Note: In macOS, F1-F12 is the same as Windows system, you must press Fn + key, but if you do n’t press Fn, there are volume function keys and touchpad key off. It is detected that pressing F9 and F10 in the keyboard has feedback, but the operation is not defined.

| Button |                                                              |
| ------ | ------------------------------------------------------------ |
| FN+P   | Adjust brightness-increase brightness (yes, there is only one increase brightness button) |
| F1     | Adjust sound-mute (same as keyboard logo)                    |
| F2     | Adjust sound-reduce volume (same as keyboard logo)           |
| F3     | Adjust sound-increase volume (same as keyboard logo)         |
| F6     | Close touchpad（same as keyboard logo,👍）                    |

## Maybe you need to turn on these features

#### 1. Set battery and power mode 

Enter Windows and open `_Drive and Tools`, and run` BatterySetting_联想管家电池管理.exe` settings.

#### 2.Open macOS HiDPI

[Click on the opening method](https://github.com/xzhih/one-key-hidpi/blob/master/README.md)

## Touchpad setup tutorial 

**(Shield Apple original I2C driver)**

1.Go to the driver folder `\ System\Library\Extensions\` 

2.**Delete** the two troublesome files (I config masked, but invalid):

- **`AppleIntellpssI2C.kext`**
- **`AppleIntellpssI2CController.kext`**

3.Use the `Hackintool`-` tool (the box icon in the lower right corner)` -` to rebuild the cache and repair permissions` Or execute `sudo kextcache -i /` to rebuild the cache

4.**Put `VoodooI2C_9ed8_9ed9.kext` in the` _Drive and Tools` folder into `CLOVER\kexts`. **

| images                                                       |                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [![Trackpad1](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/Trackpad%20(1).png)](https://tva2.sinaimg.cn/large/006bfoyggy1gc1wl59dh0j31hc0u0qv6.jpg) | [![Trackpad2](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/Trackpad%20(2).png)](https://tva4.sinaimg.cn/large/006bfoyggy1gc1wl6ey6ej31hc0u07wh.jpg) | [![Trackpad3](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/Trackpad%20(3).png)](https://tva3.sinaimg.cn/large/006bfoyggy1gc1wl6uaivj31hc0u0e82.jpg) |
| [![Trackpad4](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/Trackpad%20(4).png)](https://tva4.sinaimg.cn/large/006bfoyggy1gc1wl7bug0j31hc0u0hdu.jpg) | [![Trackpad5](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/Trackpad%20(5).png)](https://tvax1.sinaimg.cn/large/006bfoyggy1gc1wl7tim7j31hc0u0hdu.jpg) |                                                              |

*Tips:It is recommended to right-click the new window to open the picture or view the `_images` folder.*

## Test Screenshot

[![0](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/screenshot.png)](https://tvax1.sinaimg.cn/large/006bfoyggy1gc1wl4t65aj31hc0u0qv5.jpg)

[![1](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/pic1.png)](https://tvax3.sinaimg.cn/large/006bfoyggy1gc1wl3rccrj31hc0u0kjl.jpg)

[![2](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/pic2.png)](https://tvax4.sinaimg.cn/large/006bfoyggy1gc1wl4drwqj31hc0u0b2a.jpg)

![1](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/bluetooth%20(1).png)

![2](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/bluetooth%20(2).png)

![3](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/raw/master/_images/bluetooth%20(1).png)

