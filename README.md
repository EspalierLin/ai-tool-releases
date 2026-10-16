<p align="center">
  <img src="assets/assistant.png" width="160" height="160" alt="蓝色的 Imbalier 小助手" />
</p>

<h1 align="center">你好，我是 Imbalier</h1>

<p align="center"><strong>你的批量生图小助手，陪你把一批想法做成一套作品。</strong></p>

你定好共同画风和参考图，再写下每张图想画什么。我帮你把它们放进同一个本地工程，逐项生成、比较结果，再整理好导出。

- **一批一起做**：共用提示词、参考图和生图参数，每张图保留自己的内容。
- **好结果慢慢挑**：查看成图和历史版本，用颜色标签和顺序整理。
- **下次接着做**：保存完整工程，继续修改；需要交付时，导出你选中的图片。

## 桌面版下载

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.2.3（1093） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/imbalier%2Fv0.2.3-build.1093-macos-arm64/Imbalier-0.2.3-1093-macOS-arm64.dmg) |
| Windows x64 | 0.2.4（1094） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/imbalier%2Fv0.2.4-build.1094-windows-x64/Imbalier-0.2.4-1094-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`73037b7f0ab28d6019f39442693286c63c515fee54934f08368258dd70c28f4c`
- Windows x64：`069cf9afdc11080253fc8cbd1c113ba4a806ba6b4abe426cb1e1eb064a8f07ac`

</details>

<!-- release-downloads:end -->

Mac：macOS 14+／Apple 芯片，打开 DMG 后把应用拖入 Applications。Windows：Windows 10+／x64，保存作品并退出旧实例后运行 EXE，可选择本机安装目录。包内包含运行环境，无需克隆仓库或另装 Python。

0.2.3 修复文件账本误判、另存草稿冻结和更新交接；两平台均为 1093。升级保留外置工程、图片、账号和已安装插件。

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

当前实际发行的 Skill／网页为 **0.2.2**，以下是两份独立平台 ZIP，旧包仍显示 Batch Image Foundry。它们和桌面版共用 v4 工程；ZIP 自带解释器和执行器。

| 系统 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.2.2（1091） | [下载 ZIP](https://github.com/EspalierLin/ai-tool-releases/releases/download/101-batch-image-foundry%2Flocal-web%2Fv0.2.2-build.1091-macos-arm64/batch-image-foundry-0.2.2-1091-Local-Web-macos-arm64.zip) |
| Windows x64 | 0.2.2（1092） | [下载 ZIP](https://github.com/EspalierLin/ai-tool-releases/releases/download/101-batch-image-foundry%2Flocal-web%2Fv0.2.2-build.1092-windows-x64/batch-image-foundry-0.2.2-1092-Local-Web-windows-x64.zip) |

SHA-256：Mac `7494ab30d6ac39bc873b073ecf67c0ac57e1579d20ece4e8506f0001b736ce7b`；Windows `3f6d93afc73b1266a1627711a41297b6c3901e01f34915aaec8518da19626a9c`。历史 Release 标签与附件保留，下载不依赖已删除的旧分支。

1. 先介绍并询问是否安装；检测 OS／CPU，以及 AI 宿主是否有本机文件、命令和 Skill 能力。只有云端聊天能力无法安装到用户电脑。
2. 同意后选择上表对应 ZIP，固定版本、build、大小和 SHA-256。对应 Release 还提供 `manifest.json` 和独立 `.zip.sig`；核对官方入口及签名身份，不使用源码 ZIP 或全仓库 latest。
3. 按当前 AI 宿主的 Skill 安装规则选择位置；检查 ZIP 路径后完整解压，保留执行权限。归档根为 `batch-image-foundry`；禁止覆盖活动目录或其他 Skill，不修改全局 Python／Node。
4. Mac 用 `scripts/run.sh`，Windows 用 `scripts/run.cmd`。先读 `--help`、`--version` 和 `skill --json`；按宿主规则刷新发现，确认实际加载。
5. 查 `runtime status`；沿 `ui open --no-launch` 获取本机 `127.0.0.1` 网页，再按随包 `SKILL.md` 操作。版本不兼容时安全退出旧实例，不删锁、不强退任务。
6. 工程是用户选择位置的完整 `.elproject` 文件夹，放在程序之外；AI 和网页操作同一工程，不直接改 JSON 或另建副本。账号由用户在工作台连接，安装同意不授权生图，也不授权读取其他 App 的凭据。
7. 更新 Skill 前沿 `runtime stop` 等待安全点，完整替换该程序目录；保留外置工程、授权、偏好和未完成任务。当前 Skill 采用手动完整替换，不使用桌面安装器更新。
8. 用用户语言报告真实版本、路径、入口和结果，并清除本次临时下载与解压。用户对话跟随当前语言；工作台支持中文和英文。

</details>

[返回工具目录](https://github.com/EspalierLin/ai-tool-releases)
