# VirtualSpectre
a free vt-x&amp;ept debugger

# 虚拟幽灵
一个免费的基于vt-x&ept技术的多功能调试器

![avatar](https://wx4.sinaimg.cn/mw690/e9978128gy1gqecu134gdj21110cbq5m.jpg)

## 当前版本
Beta v1.0
## 环境需求
使用系统可以是所有的Win10版本x64系统 ,必须是支持intel虚拟化的cpu,且需要在主板中打开vt选项


## 功能

### 超级调试引擎
使用重构的调试引擎接管系统，不受各种反调试影响 (BE/XE/XC3/EAC/TP...)

调试EAC示例:
![avatar](https://wx1.sinaimg.cn/large/e9978128gy1gqeiyn721kj21h90u0hdv.jpg)

### 超级断点引擎
一方通行，使用ept技术接管硬件断点 R/W/E。使用虚拟的硬件断点，不受占坑影响，且无法被检测到drx

读写测试

![avatar](https://wx3.sinaimg.cn/large/e9978128gy1gqemddcrpdj21c20u0x12.jpg)

执行测试

![avatar](https://wx4.sinaimg.cn/large/e9978128gy1gqemdea0grj21cf0u0keh.jpg)

### 超级句柄引擎
使用自定义句柄引擎接管，独立于系统句柄之上,无法被检测句柄

### 反ASLR
基址固定，可以指定程序或其加载的DLL时的基址，方便调试

![avatar](https://wx4.sinaimg.cn/mw690/e9978128gy1gqecu142kcj211d0bdq82.jpg)

![avatar](https://wx4.sinaimg.cn/mw690/e9978128gy1gqecu15resj20wj09l46m.jpg)

### 内存监视器
使用EPT技术监视指定进程中的内存的读写访问记录，支持指定长度，同时支持内核地址，类似于CE的查找访问读写地址，不仅可以监视目标进程，同时还可以监视其他进程的访问

比如下图的调试器访问目标内存的时候也被捕捉到。 不限制长度，可方便调试基址，定位CRC等

![avatar](https://wx3.sinaimg.cn/large/e9978128gy1gqem55uqqmj21h10iyazu.jpg)


### 调试器保护
保护调试器本身内存跟句柄不被读取，检测

### 异常忽略器
自动跳过频繁的异常，不发送给调试器

## 用法
将x32/x64dbg.exe修改成od.exe，将cheatengine.exe修改为ce.exe，然后调试器附加即可，推荐用法，x32/x64dbg附加后，cheatengine搜索数据，配合内存监视器快速定位代码

## 点我下载 VirtualSpectre V1.0 Beta
