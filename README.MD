# Lenovo-WEI6-Pro-13-IWL-Hackintosh EFI
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


### 无问题

1. CPU睿频正常（通过CPU-S查询）
2. 亮度调节正常
3. 开启HiDPI -> [开启方法点我传送](https://github.com/xzhih/one-key-hidpi/blob/master/README-zh.md)
4. 声音输入输出正常（耳机孔输出正常）
5. 睡眠正常
6. Hdmi接口接入显示器正常
7. 蓝牙正常

### 有问题
1. **电池电量显示为0**
> 我已经拆解了**DSDT**16位，打了0电量补丁，但无效。详细可见ACPI的`DSDT.aml`。
2. **TouchID？（虽然识别了指纹模块，但估计搞不了）**
3. **触控板和FN快捷键（还没去看）**



## 近期更新记录(更多请查看Commits)


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

[黑果小兵的博客 macOS Mojave 10.14.5 镜像下载](https://blog.daliansky.net/macOS-Mojave-10.14.5-18F132-official-version-with-Clover-4928-original-image.html)


## 系统截图

![系统截图](https://raw.githubusercontent.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/master/_images/1.png)
![系统截图2](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/blob/master/_images/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-08-19%20%E4%B8%8B%E5%8D%888.31.53.png?raw=true)
![系统截图3](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/blob/master/_images/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-08-19%20%E4%B8%8B%E5%8D%888.33.14.png?raw=true)
