# 无线麦【Win版】（多方案定制 Fork）

> **本仓库说明**
>
> 本项目是 [ZSTDJan/windows-remote-mic-app](https://github.com/ZSTDJan/windows-remote-mic-app) 的 Fork，基于 v1.0.87 修改。
>
> 原始项目版权归原作者所有，协议为 **GPL v3**。本 Fork 继续沿用 GPL v3 协议。
>
> **本 Fork 相对原版的修改：**
> 1. **多套按键方案切换**：按键映射页新增方案下拉框，支持创建多套按键方案（方案A/B/C…），可软件内一键切换、复制、重命名
> 2. **快速切换快捷键**：新增 `Ctrl+Alt+P` 快捷键，按下后自动循环切换方案（A→B→C→A），可在按键映射里把遥控器某个键映射为此组合键
> 3. **界面优化**：加宽方案下拉框、调整窗口初始高度，使按键页一屏完整显示
>
> 详细修改记录见下方"修改历史"章节。

无线麦把蓝牙语音遥控器的按键和麦克风变成 Windows 快捷操作与语音输入工具，可远距离控制应用、输入文字和触发 Quicker 动作。支持按键单击、双击、长按映射，适配小米蓝牙语音遥控器 2 Pro 和谷歌 TV Chromecast 遥控器，可配合搜狗、微信、豆包输入法使用。QQ 群：89641716。

| 谷歌遥控器按键映射 | 小米遥控器按键映射 |
| --- | --- |
| ![谷歌遥控器按键设置界面](docs/screenshots/google-buttons.jpg) | ![小米遥控器按键设置界面](docs/screenshots/xiaomi-buttons.jpg) |

![图示谷歌与小米遥控器实物对比](docs/images/remote-comparison.png)

设备参考：<br>1. 小米遥控器约 65-99 元 Type-C充电（录音功能有限制——仅支持按住型，单次录音限制 60 秒内）；<br>2. 图示谷歌遥控器约 15 元（录音功能无限制——支持按住型&开关型，录制超 60 秒）；<ins><strong>谷歌遥控器版本较多，图示款购自某多多平台「IN数码配件」，仅作型号参考，无利益关联；<br>购买谷歌遥控时注意看遥控版本差别（电池仓内）！以免买来不能用。。。</strong></ins>

## 下载与版本

**[下载正式版 1.0.87](https://github.com/ZSTDJan/windows-remote-mic-app/releases/download/v1.0.87/RemoteMicRC003-1.0.87-portable-unsigned.zip)** · [版本说明](https://github.com/ZSTDJan/windows-remote-mic-app/releases/tag/v1.0.87) · [SHA256SUMS.txt](https://github.com/ZSTDJan/windows-remote-mic-app/releases/download/v1.0.87/SHA256SUMS.txt)

当前正式版为 **1.0.87**，支持小米蓝牙语音遥控器 2 Pro 和图示谷歌 Chromecast 遥控器。修复元素导航确认及右键的输入冲突，补齐点击诊断，并改进音频采样、更新检查和日志导出；保留豆包输入法 0.9.1.22、B 款微信、连接兼容、Chatterfly 及快捷键支持。具体功能与界面以下载的版本为准。

旧正式版和测试版保留在 [历史版本](https://github.com/ZSTDJan/windows-remote-mic-app/releases)。实体遥控器、宿主点击、44.1k 音频、文字上屏、久置／休眠恢复和异机仍按各自项目实测，原微信久置反馈电脑已按用户要求取消验收。

完整解压 ZIP 后运行其中的 `无线麦 win版 <版本号>.exe`，不要只取出 EXE。程序未签名，Windows 可能弹出安全提示；请从本仓库下载。

## 能做什么

- 给遥控器按键设置方向、确认、音量、快捷键、鼠标操作或 Quicker 动作；同一按键可分别设置单击、双击和长按。
- 用遥控器话筒键说话，在文字输入框中使用搜狗、微信或豆包输入法输入文字。
- 在通知区域保持运行；关闭设置窗口通常会隐藏，结束程序请从通知区域选择“完全退出”。

## 第一次使用

### 先让遥控器按键可用

1. 在 Windows 蓝牙设置中配对遥控器，再打开无线麦。
2. 在“设备”页点“选择设备”，选中刚配对的遥控器并点“使用此设备”；然后点“启动服务”。按页面提示处理未就绪的项目，直到显示已连接。
3. 按一次方向键确认能控制电脑。要改按键动作，到“按键”页选择按键，设置单击、双击或长按动作，点“完成”即保存。

![设备选择与连接状态教程](docs/screenshots/device-ready-status.jpg)

<sub>设备教程图来自旧版界面；新版按钮位置可能略有变化，操作顺序相同。</sub>

### 再设置语音输入

1. 在“语音”页安装音频组件。无线麦的输出端点选 `CABLE Input`，输入法的麦克风选 `CABLE Output`。
2. 选择搜狗、微信或豆包输入法，核对无线麦“语音按键”与输入法对应模式的快捷键一致；自动读取失败时可手动录入。小米使用按住型；谷歌还可选择开关型。
3. 先在记事本中用电脑键盘试这个快捷键，确认能打开语音输入。再把光标留在文字框里试遥控器：按住型是按住说话、松开结束；开关型是按一次开始、再按一次结束。

![输入法快捷键与虚拟麦克风配置教程](docs/screenshots/voice-configuration-example.jpg)

<sub>语音教程图以豆包输入法为例，重点是两边快捷键一致，并在输入法中选择 `CABLE Output`；新版界面位置可能略有变化。</sub>

**快捷键注意：**避开 Windows 和其他软件正在使用的组合键。按住说话期间，这组快捷键会一直保持按下，松开话筒键才释放；这段时间不要同时操作其他键或鼠标。

首次配对、音频安装和故障排查的详细步骤见 [使用说明](apps/windows/rc003/README.md)。

## 界面介绍

| 1. 设备：选择遥控器、查看连接状态 | 2. 谷歌按键映射：设置单击、双击、长按 |
| --- | --- |
| ![无线麦设备界面](docs/screenshots/device-overview.jpg) | ![谷歌遥控器按键设置界面](docs/screenshots/google-buttons.jpg) |
| 3. 小米按键映射：设置单击、双击、长按 | 4. 语音：选择输入法和快捷键 |
| ![小米遥控器按键设置界面](docs/screenshots/xiaomi-buttons.jpg) | ![无线麦语音界面](docs/screenshots/voice-overview.jpg) |

## 交流与反馈

无线麦 QQ 群：**89641716**

<img src="docs/images/qq-group-89641716.png" alt="无线麦 QQ 群 89641716 二维码" width="320">

<details>
<summary>开发与技术资料</summary>

Windows 客户端的运行、构建和技术说明见 [开发者文档](apps/windows/rc003/README.md)。
元素导航的独立项目 OrthoFocus 见 [项目说明](apps/windows/orthofocus/README.md)。

从源码运行设置界面：

```powershell
Set-Location apps/windows/rc003
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements-dev.txt
$env:PYTHONPATH = Join-Path (Get-Location) 'src'
.\.venv\Scripts\python.exe -m ovb_rc003 --settings
```

</details>

## 开源与安全

代码按 [GPL-3.0-only](LICENSE.md) 发布；第三方组件和素材按各自的许可与授权使用，见 [第三方说明](THIRD_PARTY_LICENSES/README.md) 和 [素材授权](ASSET_LICENSES.md)。普通问题与建议见 [参与说明](CONTRIBUTING.md)，安全漏洞请通过 [私密报告入口](SECURITY.md) 提交。

---

## 本 Fork 修改历史

### v1.0.87-custom.1（2026-10-10）

基于原版 v1.0.87 新增以下功能：

**1. 多套按键方案切换**
- 按键映射页顶部新增方案下拉框，显示当前激活方案
- 支持"复制为新方案"：把当前方案复制成新方案（自动命名方案A、方案B…）
- 支持"重命名"：给方案取有意义的名字（如"写代码"、"控播放器"）
- 软件内一键切换方案，即时生效，两套按键互不影响
- 向后兼容：原版单套配置自动视为"方案A"

**2. 快速切换快捷键**
- 新增 `Ctrl+Alt+P` 快捷键（P=Profile）
- 按下后自动循环切换方案（A→B→C→A）
- 可在按键映射里把遥控器某个键（如"输入源"）映射为 `key_combo=Ctrl+Alt+P`，按遥控器键即可切换方案
- 注意：此快捷键为窗口级，软件窗口聚焦时生效

**3. 界面优化**
- 加宽方案下拉框（200px），方案名完整显示
- 调整窗口初始高度（560→600px），加了方案行后按键页一屏完整显示

**修改涉及文件：**
- `src/ovb_rc003/remote_settings.py`：新增 `cycle_mapping_profile()` 函数
- `src/ovb_rc003/key_mapping.py`：新增 `CYCLE_MAPPING_PROFILE` 动作枚举
- `src/ovb_rc003/settings_ui.py`：新增"循环切换按键方案"动作标签
- `src/ovb_rc003/qt_settings_app.py`：新增方案切换相关 Property/Slot
- `src/ovb_rc003/qml/ButtonsPage.qml`：方案切换 UI、Ctrl+Alt+P 快捷键
- `src/ovb_rc003/qml/main.qml`：窗口高度调整
