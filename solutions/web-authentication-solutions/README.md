# ✨网页Web认证

采用 nettask、autoshell 两个脚本插件进行网页Web认证

## 1.nettask

### 1.1插件下载
- [链接1](https://github.com/lucikap/luci-app-nettask) 作者：lucikap（Brukamen） [个人主页](https://github.com/lucikap)

---

### 1.2nettask 介绍

#### 1.2.1前置和安装包的说明

```
luci-app-nettask_1.5.2-1_all.ipk
luci-app-nettask_2.0.0-1_all.ipk

功能特点
在 LuCI 界面上直接编辑和运行 Shell 脚本
支持多种执行方式，包括立即运行、开机运行、定时任务、按钮触发和断网触发
灵活的配置选项，可以根据需要自定义任务执行的时间和频率
```

#### 1.2.2nettask 详细操作说明

```
功能一：立即执行
编辑脚本，保存应用后点击运行即可运行，如果脚本在运行就会显示停止运行按钮，点击即可停止运行。

功能二：系统启动时运行
此脚本启用状态下，会伴随系统启动而运行，支持死循环的程序。

功能三：按下机器上的按钮时运行
轻按路由器的复位按键无需停留快速抬起，即可运行这个脚本。

功能四：断网执行
此功能适合用于某些认证上网的场景(某些校园网需要发送post请求、get请求来认证上网)，在检测到网络断开的情况下，会执行这个脚本

功能五：计划任务
除了即时执行脚本，这个插件还支持设置定时任务。用户可以轻松地安排脚本在特定时间点或间隔时间内运行，实现自动化操作。它可以自定义每月-日-周几-时-分来执行这个脚本，计划任务的规则跟系统默认的写法一样。
```

- 使用方法,一定要仔细看每一行！  
- 安装：在仓库中下载插件的ipk安装包，在openwrt中上传并安装软件包  
 （如果安装后没有在”系统“子菜单下找到“自定义脚本”请重启路由器）  
- 抓包：抓包参考---转到原帖  https://blog.csdn.net/Brukamen/article/details/131539403  
- 注意事项：在新的插件中我们需要的是curl（bash）而不是原教程中的curl（cmd），  
  然后将复制下来的内容进行一些处理，将最后两行的  

```
--compressed \
--insecure
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;删除掉，还有最后一行的\号也要删掉  

- 部署：
  打开插件的断网执行部分，将复制下来的内容粘贴到中间  


#### 1.2.3nettask 相关参考链接

- [浏览器抓包curl](https://blog.csdn.net/Brukamen/article/details/131539403) 作者：Brukamen [个人主页](https://blog.csdn.net/Brukamen?type=blog)
- [openwrt上的小插件，支持在luci上直接编写shell脚本并运行](https://www.right.com.cn/forum/thread-8348021-1-1.html) 作者：Brukamen [个人主页](https://www.right.com.cn/forum/space-uid-837703.html)
- [校园网web自动认证最新解决方案（luci-app-nettask）](https://www.right.com.cn/forum/thread-8351673-1-1.html) 作者：Brukamen [个人主页](https://www.right.com.cn/forum/space-uid-837703.html)
- [OpenWrt系统路由器自动Web认证校园网](https://suiseiko.com/?p=30) 作者：脆芙椰椰 [个人主页](https://suiseiko.com/)

---

## 2.autoshell

### 2.1插件下载

- [链接1](https://github.com/lucikap/luci-app-brukamen/tree/main/luci-app-autoshell) 作者：lucikap（Brukamen） [个人主页](https://github.com/lucikap)
```
仅有 luci-app-autoshell_1.2.3-1_mipsel_24kc.ipk
其他架构需自行编译

```
[luci-app-autoshell_1.2.3-1_mipsel_24kc.ipk](https://github.com/lucikap/luci-app-brukamen/blob/main/luci-app-autoshell_1.2.3-1_mipsel_24kc.ipk)

---

### 2.2autoshell 介绍

#### 2.2.1前置和安装包的说明


```
该插件是针对校园网 Web 认证场景开发的实用工具。很多校园网需要通过网页手动登录认证才能联网，而此插件可让用户将抓包获取的 curl 登录命令制作成 bash 脚本，配置后路由器能自动执行脚本完成联网认证，无需每次手动操作，解决了校园网频繁手动登录的痛点。
```

#### 2.2.2autoshell详细介绍

```
获取方式
该插件收录在luci-app-brukamen项目中，可通过项目仓库获取，具体路径如下：
访问 GitHub 仓库：https://github.com/lucikap/luci-app-brukamen.git ；
仓库中包含该插件的源码及对应 ipk 安装包（例如luci-app-autoshell_1.2.3-1_mipsel_24kc.ipk，不同平台版本的后缀可能有差异）；
也可通过仓库中的全自动编译脚本，自行编译生成适配自身路由器硬件平台的 ipk 文件。

生效配置：安装完成后重启路由器，重启后即可在 OpenWrt 的 LuCI Web 界面中找到该插件的相关功能入口，后续可在此配置自动登录脚本。
```

#### 2.2.3autoshell 相关参考链接

```
暂无
```
