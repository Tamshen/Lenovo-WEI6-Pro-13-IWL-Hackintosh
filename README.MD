# Lenovo-WEI6-Pro-13-IWL-Hackintosh
此笔记本的其它名字（外观、配置基本一样）：
> - **Lenovo Thinkbook 13S**
> - **Lenovo 扬天 S540**

## 配置信息

| 硬件     |                                                      |
| -------- | ------------------------------------------------------------ |
| 主板     | 联想 LNVNB161216                                              |
| 处理器   | Intel(R) Core(TM) i7-8565U (UHD Graphics 620)                   |
| 内存     | 8GB 2400MHz Micron                                           |
| 硬盘     | HFM512GDHTNG-831                                  |
|独立显卡     | AMD 540X Series （已屏蔽 ）        |
| 显示器   | FHD 1920x1080 (13.3 英寸)                                    |
| 声卡     | 瑞昱 High Definition Audio @ 英特尔 英特尔智音技术音频控制器   |
| 网卡     | 英特尔AC9560（请使用USB网卡{我是USB网卡：`CF-WU810N`}或更换网卡）              |


## 各项功能情况

|  硬件情况  | 名称            |
|:--------:|--------------------|
|   ✔   | 摄像头                 |
|   ✔   | 蓝牙                 |
|   ✔   | 扬声器                 |
|   ❌   | 触摸板    |
|   ❌   | 指纹模块    |
|   ❌   | 独显（AMD可能有机会）                 |
|   ❌   | WIFI（AC9650直接死亡，请使用USB网卡或更换）  |
|  **接口情况**  | ------            |
|   ✔   | HDMI（外接显示器）            |
|   ✔   | Type-c（数据）           |
|   ✔   | 3.5mm耳机接口             |
|   ✔   | USB接口*2                 |
|  **功能情况**  | ------           |
|   ✔   | CPU睿频（通过CPU-S查询）     |
|   ✔   | 亮度调节           |
|   ✔   | 开启HiDPI -> [开启方法点我传送](https://github.com/xzhih/one-key-hidpi/blob/master/README-zh.md)             |
|   ✔   | 声音输入输出正常（耳机孔输出正常）  |
|   ✔   | 睡眠正常  |
|   ❌   | **电池电量显示为0**  |


## 近期更新记录(更多请查看Commits)

**2020/01/11**

此次更新主要是全部流程走一遍，看看有没有错误。

测试了10.15.2(19C57)，但我是`CF-WU810N`网卡，10.15无法装驱动！但装低版本安装驱动后升级到10.15.2(19C57)可以用（其它功能具体没测试，应该会有小问题）。

我根据小新的OC试了试OC引导（10.15.2(19C57)），OC启动速度快很多，但还有很多问题！

电池驱动依然还没解决，但可以接电源外接鼠标稳定使用。

> - U>更新 macOS版本更新到**10.14.6(18G87)**
> - U>更新 Clover 版本为 **5033**
> - A>添加 `NoTouchID.kext` 驱动 屏蔽TouchID
> - F>修复 HDMI外接显示器后笔记本屏幕黑屏
> - A>添加 OC引导尝鲜（直接装10.15.2(19C57)，还有很多问题）


**2020/01/10**
> - D>删除 多余驱动和SSDT
> - F>修复 屏幕亮度（上个版本不小心删了） 

**2020/01/07**
> - A>添加 `VoodooHDA.kext` 驱动 修复声音
> - A>添加 `USBInjectAll.kext` 驱动（可显示指纹模块）
> - U>升级 Clover 版本为 **5100**
> - D>删除 多余驱动
> - U>更新 启动主题




## 注意
**关闭Intel SGX后会无法使用指纹！**
- Security
  - Intel SGX: Disable or Software Control 视BIOS版本不同操作会有所不同


## 系统镜像下载

[黑果小兵的博客 macOS Mojave 10.14.6 镜像下载](https://blog.daliansky.net/macOS-Mojave-10.14.6-18G87-Release-version-with-Clover-5033-original-image.html#10146-18g87-下载链接)


## 测试截图

![截图](https://raw.githubusercontent.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/master/_images/1.png)
![截图](https://raw.githubusercontent.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/master/_images/2.png)
