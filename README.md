<p align="center">
  <img src="assets/assistant.png" width="160" height="160" alt="蓝色的 Imbalier 小助手" />
</p>

<h1 align="center">你好，我是 Imbalier</h1>

<p align="center"><strong>你的批量生图小助手，陪你把一批想法做成一套作品。</strong></p>

你定好共同画风和参考图，再写下每张图想画什么。我帮你把它们放进同一个本地工程，逐项生成、比较结果，再整理好导出。

- **一批一起做**：共用提示词、参考图和生图参数，每张图保留自己的内容。
- **好结果慢慢挑**：查看成图和历史版本，用颜色标签和顺序整理。
- **下次接着做**：保存完整工程，继续修改；需要交付时，导出你选中的图片。

## 下载

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 / Windows x64 · 本地 Skill / 网页 | 0.2.4（1094） · 预览版 | [下载 ZIP](https://github.com/EspalierLin/ai-tool-releases/releases/download/imbalier%2Flocal-web%2Fv0.2.4-build.1094-universal/imbalier-0.2.4-1094-Skill.zip) |
| Mac · Apple 芯片 | 0.2.4（1097） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/imbalier%2Fv0.2.4-build.1097-macos-arm64/Imbalier-0.2.4-1097-macOS-arm64.dmg) |
| Windows x64 | 0.2.4（1094） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/imbalier%2Fv0.2.4-build.1094-windows-x64/Imbalier-0.2.4-1094-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片 / Windows x64 · 本地 Skill / 网页：`d102661ac3fbadf17f6183f1c52530a05ca0e1329bb68ce66442e5a758f396bb`
- Mac · Apple 芯片：`84b1e7b391ea2f469a6e2592e3f0dbc19b63e0c1cb1b4635fd03d47d36511ffa`
- Windows x64：`069cf9afdc11080253fc8cbd1c113ba4a806ba6b4abe426cb1e1eb064a8f07ac`

</details>

<!-- release-downloads:end -->

Mac：macOS 14+／Apple 芯片，打开 DMG 后把应用拖入 Applications。Windows：Windows 10+／x64，保存作品并退出旧实例后运行 EXE，可选择本机安装目录。包内包含运行环境，无需克隆仓库或另装 Python。

0.2.4（1094）统一桌面版和通用 Skill 的业务与工程格式，并支持按参考图自动匹配的插件批次参数。升级保留外置工程、图片、账号和已安装插件。

## 更新

在“设置 → 检查更新”中检查、下载并验签。Windows 新宿主支持“更新并重启”；Mac 保存更新 DMG 后手动替换应用。

旧版本若无法在软件内完成更新，请从本页手动安装新版一次；之后继续使用软件内的检查更新。原工程和账号继续保留。

## 通过 AI 使用本地 Skill／网页

复制下面一段给能操作本机文件和命令的 AI。它先用你的语言介绍并询问是否安装，同意后才安装。网页在本机运行，不需要服务器。

```text
Read https://raw.githubusercontent.com/EspalierLin/ai-tool-releases/refs/heads/imbalier/README.md. Reply in the language of our conversation. Explain Imbalier's local Skill and browser mode, supported downloads, local project ownership and account use, then ask whether I want to install it. Do not install, sign in or generate images before I agree. After I agree, follow this README's AI installation instructions for my operating system and AI host, verify the exact published archive, and report the actual result.
```

<details>
<summary>Skill 下载与 AI 安装规则</summary>

当前通用 Skill／网页与桌面版同为 **0.2.4（1094）**。上方的一个 Skill ZIP 同时包含 Mac Apple 芯片和 Windows x64 的运行环境，启动脚本自动选择本机材料，无需安装桌面 App、Python 或 Node。网页在你的电脑里运行。

通用 ZIP 大小为 **438238444 字节**，SHA-256 见上方校验栏。支持 macOS 14+／Apple 芯片和 Windows 10+／x64；Intel Mac、Windows ARM、Linux／WSL 和手机不在本包范围。

1. 先介绍并询问是否安装；检测 OS／CPU，以及 AI 宿主是否有本机文件、命令和 Skill 能力。只有云端聊天能力无法安装到用户电脑。
2. 同意后下载上方唯一的 Skill ZIP，核对版本、build、大小和 SHA-256。对应 Release 提供两个平台清单 `manifest-darwin-arm64.json`、`manifest-windows-x86_64.json` 和独立 `.zip.sig`；核对官方入口及签名，不使用源码 ZIP 或全仓库 latest。当前更新入口是本分支 `channels/preview/` 下对应系统的签名头。
3. 按当前 AI 宿主的 Skill 安装规则选择位置；检查 ZIP 路径后完整解压，保留执行权限。归档根为 `imbalier`；禁止覆盖活动目录或其他 Skill，不修改全局 Python／Node。
4. Mac 用 `scripts/run.sh`，Windows 用 `scripts/run.cmd`。先读 `--help`、`--version` 和 `skill --json`；按宿主规则刷新发现，确认实际加载。
5. 查 `runtime status`；沿 `ui open --no-launch` 获取本机 `127.0.0.1` 网页，再按随包 `SKILL.md` 操作。版本不兼容时安全退出旧实例，不删锁、不强退任务。
6. 工程是用户选择位置的完整 `.elproject` 文件夹，放在程序之外；AI 和网页操作同一工程，不直接改 JSON 或另建副本。账号由用户在工作台连接，安装同意不授权生图，也不授权读取其他 App 的凭据。
7. 更新 Skill 前沿 `runtime stop` 等待安全点，完整替换该程序目录；保留外置工程、授权、偏好和未完成任务。Skill 使用自己的更新源检查和下载通用 ZIP；下载完成后协助用户完整替换，不使用桌面安装器覆盖 Skill。旧分支版请从本页手动更新一次。
8. 用用户语言报告真实版本、路径、入口和结果，并清除本次临时下载与解压。用户对话跟随当前语言；工作台支持中文和英文。

</details>

[返回工具目录](https://github.com/EspalierLin/ai-tool-releases)
