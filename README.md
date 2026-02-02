# Action Openwrt 云自动编译
⏰ **每周自动拉取最新源码自动编译**


<p align="center">
  <a href="https://github.com/alloneinfo/AC_LEDE">
    <img src="./assets/images/action1.jpg" alt="Logo" width="500" />
  </a>
  <h3 align="center">Openwrt/LEDE 云编译(带应用商店)</h3>
  <p align="center">
    👉 每周定时自动拉取Openwrt最新源码编译，自动发布到 [<a herf="https://github.com/alloneinfo/AC_LEDE/releases"> Releases </a>]👈
    <br />
    <a href="https://github.com/alloneinfo/AC_LEDE"><strong>探索本项目的文档 »</strong></a>
    <br />
    <br />
    <a href="https://github.com/alloneinfo/AC_LEDE/releases">下载地址</a>
    ·
    <a href="https://github.com/alloneinfo/AC_LEDE/actions">Action</a>
    ·
    <a href="https://github.com/alloneinfo/AC_LEDE/issues">提出新特性</a>
  </p>

</p>

## 目录

- [Action Openwrt 云自动编译](#action-openwrt-云自动编译)
  - [目录](#目录)
  - [支持的设备](#支持的设备)
    - [🎯固件默认设置](#固件默认设置)
  - [固件特性](#固件特性)
  - [自带插件](#自带插件)
  - [文件目录说明](#文件目录说明)
  - [定制固件](#定制固件)
    - [注意事项](#注意事项)
  - [固件预览](#固件预览)
  - [版权说明](#版权说明)
  - [项目支持](#项目支持)  

<br>


## 支持的设备
🎯 带应用商店的固件：
|           支持的设备        |         固类别         |        Action         |            状态          |              下载页          |
| :------------------------: | :---------------------: | :-------------------: | :-------------------: | :--------------------------: |
|             x86_64                    |  [LEDE](https://github.com/coolsnowwolf/lede) |[🍕](https://github.com/alloneinfo/AC_LEDE/actions/workflows/x86_64.yml) | ![x86_64](https://github.com/alloneinfo/AC_LEDE/actions/workflows/x86_64.yml/badge.svg) |  [✔](https://github.com/alloneinfo/AC_LEDE/releases) |
|             Orange Pi R1 Plus LTS         |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/alloneinfo/AC_LEDE/actions/workflows/r1.yml) | ![OrangePiR1](https://github.com/alloneinfo/AC_LEDE/actions/workflows/r1.yml/badge.svg) | [✔](https://github.com/alloneinfo/AC_LEDE/releases) |
|             OCP Hilink H28K         |  [LEDE](https://github.com/coolsnowwolf/lede) | [🍕](https://github.com/alloneinfo/AC_LEDE/actions/workflows/h28k.yml) | ![OrangePiR1](https://github.com/alloneinfo/AC_LEDE/actions/workflows/h28k.yml/badge.svg) | [✔](https://github.com/alloneinfo/AC_LEDE/releases) |

<br>

### 🎯固件默认设置
- 路由器地址: `192.168.1.1`
- 默认用户名: `root`
- 默认密码  : `password`

<br>

## 固件特性
⏰ 固件编译改为`周更`(稳定为主，减少资源浪费)

✨ iStore应用商店 [AppStore](./assets/images/appstore.png)

✨ 自带常用的插件

✨ 全新的 [Them](https://github.com/jerrykuku/luci-theme-argon)

<br>

## 自带插件
🍕 默认插件
- PassWall2
- luci-app-turboacc
- luci-app-upnp
- luci-app-turboacc
......

<br>

## 文件目录说明
eg:

```
filetree
├── .github/workflows
│  ├── Rockchip.yml
│  ├── x86_64.yml
│  ├── x86_64Lite.yml
├── /configs/ (配置文件目录)   
│  ├── /luci/ (app插件配置)   
│  |  ├── Lite.config (简洁配置)   
│  |  ├── Standard.config (标准配置 大量插件)
│  ├── x86_64.config
│  ├── Rockchip.config
├── feeds_add.sh (固件参数修改)
├── package.sh (luci-app)

```
<br>

## 定制固件
1. Fork 此项目
2. 按需修改 ```feeds_add.sh``` 和 ```package.sh``` 文件
3. 上传你自己的 ```xx.config``` 配置文件到configs目录
4. 添加或修改自己的``````xx.yml``````文件
5. 最后根据个人喜好修改 ```update-checker.yml``` 需自行添加 ```Actions secrets``` (触发自动编译)

### 注意事项：
📌 修改默认系统参数 👉 ```feeds_add.sh```   
📌 添加其它Luci插件 👉 ```package.sh```   
📌 插件 / 应用配置文件 👉 ```configs/Standard.config```   
<br>

## 固件预览
**主界面(主题一)：**
![主界面](./assets/images/openwrt.png)

**应用商店/插件**
![应用商店/插件](./assets/images/appstore.png)

**服务/插件：**
![服务/插件](./assets/images/service.png)

**网络：**
![网络](./assets/images/network.png)

**经典主题二：**
![登录页](./assets/images/infinityfreedom-theme.png)

**主界面：**
![主界面](./assets/images/infinityfreedom-theme-main.png)


## 版权说明

该项目签署了MIT 授权许可，详情请参阅 [LICENSE](https://github.com/alloneinfo/AC_LEDE/blob/main/LICENSE)


## 项目支持
- [P3TERX/Actions-OpenWrt](https://github.com/P3TERX/Actions-OpenWrt)
- [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)
- [luci-theme-argon](https://github.com/jerrykuku/luci-theme-argon)
- [istore](https://github.com/linkease/istore)
- [bigbugcc](https://github.com/bigbugcc/OpenWrts)