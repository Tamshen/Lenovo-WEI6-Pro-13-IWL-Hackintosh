# Lenovo-WEI6-Pro-13-IWL-Hackintosh EFI
> 此笔记本还有另外一个名字：**Lenovo Thinkbook 13S**（应该通用）



**驱动未完全完整！详细请看[各项功能情况](#各项功能情况)！个人暂不推荐使用，但可以尝尝鲜！**

主要是我太菜了，所以很多驱动还没完善，希望各位大佬 **help help me**....

### 注意
**关闭Intel SGX后会无法使用指纹！**
- Security
  - Intel SGX: Disable or Software Control 视BIOS版本不同操作会有所不同


## 配置信息

| 规格     | 详细信息                                                     |
| -------- | ------------------------------------------------------------ |
| 系统版本 | macOS Mojave 10.14.5(18F132)                                 |
| 电脑型号 | 联想Lenovo 威6 RPO 13 IWL笔记本电脑（Thinkbook 13s）           |
| 主板     | 联想LNVNB161216                                              |
| 处理器   | Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz                     |
| 内存     | 8GB 2400MHz Micron                                           |
| 硬盘     | HFM512GDHTNG-831 (500G固态)                                  |
| 显卡     | 英特尔 UHD Graphics 620 （独显AMD 540X Series已屏蔽）          |
| 显示器   | FHD 1920x1080 (13.3 英寸)                                    |
| 声卡     | 瑞昱 High Definition Audio @ 英特尔 英特尔智音技术音频控制器   |
| 网卡     | 英特尔AC9560 需要更换为 **`USB网卡：CF-WU810N`**              |


## 各项功能情况

### 无问题

1. CPU睿频正常（通过CPU-S查询）
2. 亮度调节正常
3. 开启HiDPI -> [开启方法点我传送](https://github.com/xzhih/one-key-hidpi/blob/master/README-zh.md)



### 已知问题

1. 无声音 - 声卡驱动 （尝试万能驱动貌似直接卡五国禁止符号）
2. 电池信息
3. 移除触摸板驱动 `VoodooI2C_9ed8_9ed9.kext`（添加此驱动后不用 `-v` 运行会直接重启）
4. FN快捷键



## 系统镜像下载

[黑果小兵的博客 macOS Mojave 10.14.5 镜像下载](https://blog.daliansky.net/macOS-Mojave-10.14.5-18F132-official-version-with-Clover-4928-original-image.html)




## 系统截图

![系统截图](https://raw.githubusercontent.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/master/_images/1.png)
![系统截图2](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/blob/master/_images/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-08-19%20%E4%B8%8B%E5%8D%888.31.53.png?raw=true)
![系统截图3](https://github.com/Tamshen/Lenovo-WEI6-Pro-13-IWL-Hackintosh/blob/master/_images/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-08-19%20%E4%B8%8B%E5%8D%888.33.14.png?raw=true)
