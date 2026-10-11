<p align="center">
  <img src="docs/logo.png" width="112" alt="ETS2 存档编辑器">
</p>

<h1 align="center">ETS2 存档编辑器</h1>

<p align="center">
  <b>面向《欧洲卡车模拟 2》的本地存档修改工具</b><br>
  免安装 · 纯本地修改 · 改前自动备份
</p>

<p align="center">
  <a href="https://github.com/NullPointerExceptionCN/ETS2-Save-Editor/releases/latest"><img src="https://img.shields.io/badge/版本-v1.0.30-4a8fd9?style=flat-square" alt="版本"></a>
  <img src="https://img.shields.io/badge/平台-Windows%2010%20%7C%2011-4a8fd9?style=flat-square" alt="平台">
  <img src="https://img.shields.io/badge/游戏-ETS2-4a8fd9?style=flat-square" alt="游戏">
  <a href="https://github.com/NullPointerExceptionCN/ETS2-Save-Editor/releases"><img src="https://img.shields.io/github/downloads/NullPointerExceptionCN/ETS2-Save-Editor/total?style=flat-square&label=%E4%B8%8B%E8%BD%BD&color=4a8fd9" alt="下载量"></a>
  <a href="https://github.com/NullPointerExceptionCN/ETS2-Save-Editor/stargazers"><img src="https://img.shields.io/github/stars/NullPointerExceptionCN/ETS2-Save-Editor?style=flat-square&color=4a8fd9" alt="Stars"></a>
</p>

<p align="center">
  <a href="https://github.com/NullPointerExceptionCN/ETS2-Save-Editor/releases/latest"><b>下载最新版</b></a>
  　·　<a href="#功能一览">功能一览</a>
  　·　<a href="#常见问题">常见问题</a>
  　·　<a href="#更新日志">更新日志</a>
</p>

---

## 简介

直接读取《欧洲卡车模拟 2》的本地存档文件，所见即所得地修改金钱、经验、车库、地图探索、车辆状态等核心数据。所有改动都在本机完成 —— 不联网、不碰游戏本体文件、不改动账号。

- **免安装**：一键安装即用，不写注册表、不留后台进程
- **改前自动备份**：每次写档前自动快照，每个存档槽保留最近 15 份，随时回滚
- **写前安全校验**：结构异常、数组错位、悬空引用在落盘前拦截
- **现代 Web 界面**：扁平暗色设计，17 张功能卡 + 生涯数据面板

<p align="center">
  <img src="docs/screenshots/01-main.png" width="820" alt="界面预览">
</p>

---

## 功能一览

| 分类 | 支持的功能 |
|---|---|
| **经济数据** | 修改金币（安全上限内一步到位）、修改经验值（可填目标等级，自动换算） |
| **地图解锁** | 购买所有车库、探索所有城市、解锁所有经销商、全图探索（内置全量数据集，并集合并不覆盖个人进度） |
| **车辆维护** | 更换卡车、更换挂车（含双挂整体切换）、修理卡车、加满油、无限油量 |
| **进阶功能** | 设置技能等级、瞬移玩家、开发者模式、整档案备份、备份还原、存档解密 |

打开存档即见**生涯数据面板**：账户余额、经验等级、城市 / 经销商 / 车库解锁进度，以及完成货次、累计里程、游戏时间、车队与卡车品牌等运营统计。

---

## 安全与可靠性

- **修改即备份**：每次写档前自动快照，保留最近 15 份，随时回滚
- **写前校验**：结构完整性、数组配平、悬空引用三重检查，只拦截本次修改新引入的问题
- **原子落盘**：临时文件写入 → 回读校验 → 原子替换，中途断电也不会留下半截存档
- **本地运行**：不联网、不上传任何数据、不修改游戏本体文件
- **签名更新**：更新包经数字签名与 SHA-256 双重校验后才会安装

---

## 快速开始

1. 从 [Releases](https://github.com/NullPointerExceptionCN/ETS2-Save-Editor/releases/latest) 下载安装包并安装
2. 启动程序，顶部选择游戏（ETS2）与档案，再选择要修改的存档（列表只列手动存档）
3. 左侧导航选分类，点功能卡片，按提示填写数值后应用
4. 改完进入游戏读档即可生效

> 修改前请先完全退出游戏；首次使用建议先跑一次「整档案备份」。

**环境要求**：Windows 10 / 11（64 位）；无需 .NET 或额外运行库，联网仅用于检查更新。

---

## 常见问题

<details>
<summary><b>会不会封号？</b></summary>

不会。工具只读写本机的单人存档文件，不联网、不注入游戏进程、不修改游戏本体，与账号无关。
</details>

<details>
<summary><b>存档列表里看不到我要的存档？</b></summary>

列表默认只显示**手动存档**，自动存档（autosave）不会列出。快速存档会显示为「快速存档」。
</details>

<details>
<summary><b>改完进游戏怎么没变化？</b></summary>

《欧卡 2》1.50 起引擎多了一层按路径索引的存档缓存。换车 / 换挂车默认会**另存为一个新存档**，回到游戏在存档列表里载入那条新存档即可生效，原存档不受影响。
</details>

<details>
<summary><b>改坏了怎么办？</b></summary>

每次修改前都会自动备份。「备份还原」里可以回滚到任意一份历史快照（保留最近 15 份），也可以用「整档案备份」还原整个档案。
</details>

---

## 交流与反馈

- 问题反馈：[提交 Issue](https://github.com/NullPointerExceptionCN/ETS2-Save-Editor/issues)
- 官方交流群：Q群 `1076878297`（[点击加入](https://qm.qq.com/q/haEUDNPFPG)）

---

## 更新日志

### v1.0.30

- 车辆维护新增「更换卡车」：原地切换到车队里的另一辆卡车，无需开回车库
- 车辆维护新增「更换挂车」：原地更换 / 挂上 / 卸下拖车，支持双挂（B-double、台车式）整体切换
- 换车 / 换挂车默认另存为新存档，改完载入即生效，原存档不受影响

### 更早版本

- 全新 Web 界面：扁平暗色设计语言，功能卡 + 生涯数据面板
- 内置全图探索数据集，支持自定义数据集合并
- 写档安全体系：写前校验 / 原子落盘 / 自动备份
- 自动更新：程序内下载，签名 + SHA-256 双重校验

---

## 免责声明

本工具仅供单人游戏体验、学习与存档备份用途，请勿用于联机对战或任何破坏他人游戏体验的场景，亦请勿用于商业用途。使用本工具产生的存档问题可用「备份还原」回滚，作者不对游戏账号状态负责。

<p align="center">
  <sub>© 2026 NullPointerExceptionCN · 保留所有权利</sub>
</p>
