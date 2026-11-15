<div align="center">

# HyperGo

**把 Tab 键变成 Hyper 键 · 按住 Tab + 字母，瞬间唤起任意应用**

macOS 键盘效率工具 · 桌面上还有一只会陪你工作的小猫

[![版本](https://img.shields.io/badge/版本-1.2.0-blue)](../../releases)
[![平台](https://img.shields.io/badge/macOS-13%2B-lightgrey)](../../releases)
[![架构](https://img.shields.io/badge/Apple%20Silicon%20%7C%20Intel-通用-orange)](../../releases)

[下载最新版](../../releases/latest) · [使用说明](#使用说明) · [常见问题](#常见问题)

<!-- 建议在这里放一张演示 GIF：按住 Tab → 小猫拍爪 → Finder 弹出 -->
<!-- ![demo](docs/demo.gif) -->

</div>

---

## 这是什么

**HyperGo** 做两件事：

**① Hyper 键** —— 按住 `Tab`（或 `\`）再按一个字母，直接跳转到你指定的应用。
比如 `Tab + F` 一秒切到 Finder，`Tab + S` 切到 Safari。不用 Cmd+Tab 翻找，不用 Mission Control，不用碰鼠标。

**② 桌面小猫** —— 一只趴在你桌面右下角的小猫，陪你工作。
它会呼吸、眨眼、伸懒腰。你按住 Tab 的时候它会睁眼，成功唤起应用时它会拍爪庆祝。20 秒不理它，它会自己起身走出屏幕去休息——零打扰，零资源占用。

<div align="center">

<!-- 截图占位：截好后放 docs/screenshot-cat.png，并取消下一行注释 -->
<!-- ![cat](docs/screenshot-cat.png) -->

</div>

## 功能特性

- ⌨️ **Hyper 键**：Tab 或 `\` + 任意字母，唤起或切换到你设定的应用
- 🖱️ **一秒添加快捷键**：选字母 → 选 App，完事
- 🐱 **桌面小猫**：陪你工作的小伙伴——你打字时它呼吸眨眼，唤起应用时它拍爪庆祝
- 🚶 **懂事的小猫**：20 秒不理它就自己走出屏幕休眠，屏幕睡眠时自动暂停，唤醒后自动回来
- 🔇 **完全静默**：无网络请求、无数据上传、无遥测，所有数据只存在本地
- 🚀 **开机自启**：登录项自动启动，监听自动开启，配置自动加载
- 💤 **不挡熄屏**：不会阻止屏幕正常休眠

## 下载安装

前往 [**Releases 页面**](../../releases/latest) 下载 `HyperGo-1.2.0.dmg`。

<details>
<summary><b>首次打开方法（重要，请看这里）</b></summary>

当前版本未做苹果公证，首次打开需要多一步操作（仅需一次）：

1. 打开 DMG，将 **HyperGo** 拖入 **Applications** 文件夹
2. 在启动台或 Applications 中**右键点击 HyperGo → 打开 → 打开**
3. 如果提示"无法验证"，请打开 **系统设置 → 隐私与安全性**，滚动到下方点击 **仍要打开**

或者，在终端执行一条命令后正常双击打开：

```bash
xattr -cr /Applications/HyperGo.app
```

首次启动会请求**辅助功能**权限（监听键盘必需），请在系统设置中允许。

</details>

## 使用说明

### 设置快捷键

打开 HyperGo → 点「Add Shortcut」→ 按一个字母键 → 选择目标应用 → 完成。
之后 **按住 Tab + 字母** 即可瞬间唤起。可随时修改或删除。

### 桌面小猫

- **打招呼**：Hyper + 字母唤起应用成功时，它会拍爪回应你
- **让它走开**：放着不管 20 秒，它自己起身走出屏幕休眠（时长可在菜单栏 Auto Leave 调整：10s / 20s / 30s / 60s / 永不）
- **召唤回来**：菜单栏 → Pet: On
- **拖动**：直接用鼠标拖到喜欢的位置，靠近屏幕边缘会自动贴边

### 菜单栏图标

| 菜单项 | 作用 |
|---|---|
| Open HyperGo | 打开快捷键配置窗口 |
| Listener: On/Off | 临时开关 Hyper 键监听 |
| Show Tutorial | 重新播放新手教程 |
| Pet: On/Off | 召回/隐藏桌面小猫 |
| Auto Leave | 小猫闲置自动离场的时长 |
| Quit HyperGo | 退出 |

## 系统要求

- macOS 13.0 及以上
- Apple Silicon (M 系列) 或 Intel 芯片
- 辅助功能权限（监听键盘必需，本工具不读取按键内容，只识别 Tab 和快捷键字母）

## 常见问题

<details>
<summary><b>重启电脑后 Hyper 键失效？</b></summary>

新版本已修复（配置随启动自动加载、监听自动开启）。如果仍遇到，点菜单栏 Listener 关闭再打开即可，并欢迎提 Issue。
</details>

<details>
<summary><b>屏幕无法熄屏？</b></summary>

旧版本存在此问题（视频播放阻止熄屏），新版本已修复。若仍遇到，请提 Issue 并注明 macOS 版本。
</details>

<details>
<summary><b>会读取我的键盘输入吗？</b></summary>

不会。HyperGo 只使用系统事件监听识别"Tab/反斜杠按下"和"哪个字母键按下"，不记录、不存储、不上传任何按键内容。应用完全离线运行，无任何网络请求。
</details>

<details>
<summary><b>如何卸载？</b></summary>

1. 菜单栏 → Quit HyperGo
2. 系统设置 → 登录项 → 移除 HyperGo
3. 删除 /Applications/HyperGo.app
4. （可选）删除配置：`~/Library/Application Support/HyperGo/`
</details>

## 已知限制

- 未做苹果公证，首次打开需手动允许（见上方安装说明）
- 暂不支持自定义修饰键（目前固定为 Tab / `\`）
- 桌面小猫的透明边缘在部分壁纸下可能略有不自然

## 技术栈

SwiftUI + AppKit · AVFoundation · CGEvent Tap · Vision · 无第三方依赖

---

## 赞助支持 ☕

如果 HyperGo 帮你省下了时间，可以考虑请作者喝杯咖啡——每一杯都是继续更新的动力：

<!-- 发布前把 docs/sponsor.png 替换为你的赞赏码海报（微信 + 支付宝合成图，make_sponsor_poster.py 生成），然后取消下方注释 -->
<p align="center">
  <!-- <img src="docs/sponsor.png" width="300" alt="赞赏码"> -->
</p>

---

<div align="center">

**如果觉得好用，请给个 Star ⭐**

*HyperGo · 让每个按键都有归属*

</div>
