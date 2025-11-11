# 校园网焚诀

## 🌍 介绍

在许多校园网络中，网络访问受到各种限制，如 DNS 劫持、流量限制、访问控制等。这个项目的目标是通过使用 OpenWRT 路由器，帮助用户绕过这些限制，提升校园网的使用体验。我们将介绍如何配置和优化 OpenWRT 路由器，使其适应不同的校园网络环境，并提供解决方案来应对常见的网络限制和局限性。本项目旨在通过 **OpenWRT 路由器** 提供解决方案，帮助用户绕过不同类型的校园网认证方式，实现更自由的网络访问。

---

## 🌐 项目结构

本项目进行分类试图帮助用户针对不同的认证场景找到相应的解决方案。

 1. **[客户端认证](https://github.com/yooz55655/Campus-Net-Savior/tree/main/solutions/client-authentication-solutions)**  
   针对不同厂商的客户端进行解决方案适配。
```
锐捷、赛尔等校园网客户端认证
```

 3. **[网页认证](https://github.com/yooz55655/Campus-Net-Savior/tree/main/solutions/web-authentication-solutions)**  
   针对网页认证方式进行通用方案适配。
   
 4. **[其他认证](https://github.com/yooz55655/Campus-Net-Savior/tree/main/solutions/other-authentication-solutions)**  
   针对其他方式进行通用方案适配。

 5. **[认证插件集合](https://github.com/yooz55655/Campus-Net-Savior/tree/main/solutions/auth-plugin-collection)**  
   应用于OpenWrt的主流校园网认证插件集合。

   ---

   ## 💡 相关内容

**[OpenWrt/iStoreOS插件推荐](https://github.com/yooz55655/Campus-Net-Savior/tree/main/solutions/auth-plugin-collection)**

**[路由器配置、操作教程](https://github.com/yooz55655/Campus-Net-Savior/tree/main/solutions/operation-tutorial)**  

**[恩山OpenGirl固件](https://www.right.com.cn/forum/thread-8411432-1-1.html)**  
   
---

## 🛠️ 如何使用

- 请根据你的校园网认证方式选择相应的分类。
- 进入对应的文件夹，查看详细的解决方案、配置文件和安装说明。
- 如果你遇到任何问题，请提交 Issue 或加入讨论！

## ⚠️ 免责声明

- 此项目仅用于教育和研究目的。请确保在合法的范围内使用，且对自己和他人的行为负责。我们不对使用本项目技术所带来的任何后果负责。
- 在本项目中引用的所有第三方内容均已标明出处，如有侵权请联系删除。

## 📂 目录结构

本项目的目录结构

```
Campus-Net-Savior/
├── README.md                     # 项目根目录的 README 文件，概述项目的目的与使用说明
├── solutions/                    # 存放解决方案的目录
│   ├── README.md                 # 该目录的 README 文件，概述整个认证解决方案部分
│   ├── client-authentication-solutions/   # 客户端认证解决方案
│   │   ├── README.md             # 该部分的 README 文件，概述客户端认证解决方案
│   │   ├── client-Dr.COM/        # Dr.COM 客户端认证的具体实现目录
│   │   ├── client-ruijie/        # 瑞捷客户端认证的具体实现目录
│   │   └── ...                   # 其他客户端认证方案的目录
│   ├── other-authentication-solutions/    # 其他认证解决方案
│   │   └── README.md             # 该部分的 README 文件，概述其他认证方式
│   │   └── ...                   # 其他认证方案的目录
│   ├── web-authentication-solutions/      # 网页认证解决方案
│   │   ├── README.md             # 该部分的 README 文件，概述网页认证解决方案
│   │   ├── Luci-app-nettask      # nettask 自定义 Shell 脚本的工具
│   │   └── ...                   # 其他网页认证方案的目录
│   └── auth-plugin-collection/   # 存放所有认证插件集合
│       ├── README.md             # 该部分的 README 文件，概述认证插件集合
│       └── ...                   # 其他插件的目录
└── ...                           # 项目根目录其他文件
```

---

### 🔗 相关链接

- [OpenWrt 官方文档](https://openwrt.org/docs/start)
- [iStoreOS 官网](https://site.istoreos.com/)
- [恩山无线论坛](https://www.right.com.cn/forum/)
- [CSDN](https://www.csdn.net)
- [kenzok8大佬的插件仓库主页](https://github.com/kenzok8)


## 💡 贡献

欢迎各位贡献者！如果你有新的认证方式解决方案或者优化建议，欢迎提交 Pull Request。
