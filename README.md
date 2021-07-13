﻿#### AutoBuild-OpenWrt
[1]: https://img.shields.io/badge/license-GPLV2-brightgreen.svg
[2]: /LICENSE
[3]: https://img.shields.io/badge/PRs-welcome-brightgreen.svg
[4]: https://github.com/kenzok8/openwrt_Build/pulls
[5]: https://img.shields.io/badge/Issues-welcome-brightgreen.svg
[6]: https://github.com/kenzok8/openwrt_Build/issues/new
[7]: https://img.shields.io/github/v/release/hyird/Action-Openwrt
[8]: https://github.com/kenzok8/openwrt_Build/releases
[10]: https://img.shields.io/badge/Contact-telegram-blue
[11]: https://t.me/joinchat/JjxmyRZZXJWb74I-sCrryA
[12]: https://github.com/kenzok8/openwrt_Build/workflows/autobuild/badge.svg
[13]: https://github.com/kenzok8/openwrt_Build/actions

[![license][1]][2]
[![GitHub Stars](https://img.shields.io/github/stars/kenzok8/openwrt_Build.svg?style=flat-square&label=Stars)](https://github.com/kenzok8/openwrt_Build/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/kenzok8/openwrt_Build.svg?style=flat-square&label=Forks)](https://github.com/kenzok8/openwrt_Build)
[![PRs Welcome][3]][4]
[![Issue Welcome][5]][6]
[![AutoBuild][12]][13]

<a href="https://t.me/joinchat/JjxmyRZZXJWb74I-sCrryA" target="_blank">Telegram</a>



#### 源码来源：
[![esir](https://img.shields.io/badge/AutoBuild-esir-red.svg?style=flat&logo=appveyor)](https://github.com/esirplayground/AutoBuild-OpenWrt)
[![Lienol](https://img.shields.io/badge/passwall-openwrt-blueviolet.svg?style=flat&logo=appveyor)](https://github.com/xiaorouji/openwrt-passwall) 
[![immortalwrt](https://img.shields.io/badge/immortalwrt-openwrt-orange.svg?style=flat&logo=appveyor)](https://github.com/immortalwrt/immortalwrt) 
[![Lean](https://img.shields.io/badge/package-Lean-blueviolet.svg?style=flat&logo=appveyor)](https://github.com/coolsnowwolf/lede) 
[![P3TERX](https://img.shields.io/badge/Actions-P3TERX-success.svg?style=flat&logo=appveyor)](https://github.com/P3TERX/Actions-OpenWrt)


##### 固件发布:

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/kenzok8/openwrt_Build?style=for-the-badge&label=Download)](https://github.com/kenzok78/Build-OpenWrt/releases/latest)


##### 固件下载链接

- [Lienol_4.14___内核固件](https://github.com/kenzok8/openwrt_Build/actions?query=workflow%3ALienol_4.14内核)
- [Lean_5.4内核_固件地址](https://github.com/kenzok8/openwrt_Build/actions?query=workflow%3ALean_5.4内核)
- [immortalwrt-21.02固件](https://github.com/kenzok8/openwrt_Build/actions?query=workflow%3Aopenwrt_21.02)
- [immortalwrt-18.06固件](https://github.com/kenzok8/openwrt_Build/actions?query=workflow%3Aopenwrt_18.06)
- [NanoPi_R2S__固件下载](https://github.com/kenzok8/openwrt_Build/actions?query=workflow%3ANanoPi_R2S)
- [NanoPi_R4S__固件下载](https://github.com/kenzok8/openwrt_Build/actions?query=workflow%3ANanoPi_R4S)

### 默认插件包含:

+ SSR Plus 
+ passwall
+ openclash
+ 动态DDNS
+ UPNP 自动端口转发
+ Turbo ACC 网络加速
+ Mwan3 负载均衡
+ 默认多个主题
+ 默认管理 IP: 192.168.1.1, 用户名 root，密码 password


### N1云编译需要注意：

* 云编译取消以下选项(要不然编译速度慢)：
  - luci-app-filebrowser
  - luci-app-jd-dailybonus
  - luci-app-unblockneteasemusic
* 关联取消
  - vim .config
  - CONFIG_FILEBROWSER_COMPRESS_UPX=n
  - CONFIG_UnblockNeteaseMusic_Go=n
  - CONFIG_UnblockNeteaseMusic_NodeJS=n
  - CONFIG_PACKAGE_luci-app-unblockneteasemusic=n
  - CONFIG_PACKAGE_luci-app-unblockneteasemusic-go=n
  - CONFIG_PACKAGE_luci-app-unblockneteasemusic-mini=n
  - CONFIG_PACKAGE_UnblockNeteaseMusic=n
  - CONFIG_PACKAGE_UnblockNeteaseMusic-Go=n
  - CONFIG_UNBLOCKNETEASEMUSIC_GO_COMPRESS_UPX=n
  - CONFIG_PACKAGE_node=n
  - CONFIG_NODEJS_14=n
  - CONFIG_NODEJS_ICU_SMALL=n
  - CONFIG_PACKAGE_node-request=n
* 最后执行  
  - make defconfig
