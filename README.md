# Batch Image Foundry · 批量生图

把一批图片的制作、整理和导出放在同一个本地工程里。共享提示词和参考图统一画风，逐项生成；用图库、表格、颜色标签和图片历史筛选结果，再按任务比例导出成图。

可以安装桌面 App，也可以让 AI 安装 **Skill＋本地网页**。两种形式共用同一套工程格式；纯 AI 用户也能随时打开完整工作台查看和接手。网页、后台、工程和授权都在当前电脑上，不需要配置服务器。

## 通过 AI 使用

点击下面代码块右上角的复制按钮，粘贴给能操作你电脑文件和命令的 AI。它会先按你的语言介绍，再询问是否安装；同意后才安装。

```text
Read https://raw.githubusercontent.com/EspalierLin/ai-tool-releases/refs/heads/101-batch-image-foundry/README.md. Reply in the language of our conversation. Explain Batch Image Foundry's local Skill and browser mode, requirements, supported downloads, project ownership and account use, then ask whether I want to install it. Do not install, sign in or generate images before I agree. After I agree, follow this README's AI installation instructions for my operating system and AI host, verify the exact published archive, and report the actual result.
```

需要本机文件／命令能力；只有云端聊天能力的 AI 无法替你安装到电脑。AI 对话跟随用户语言，工作台目前提供中文和英文。

## 下载

**App 安装包**用于独立桌面应用；**本地 Skill／网页 ZIP**自带 Python 和必要执行器，不需要先装桌面 App、Python、Node 或 Git。请按系统选择，均无需克隆仓库。

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 · 本地 Skill / 网页 | 0.2.2（1091） · 预览版 | [下载 ZIP](https://github.com/EspalierLin/ai-tool-releases/releases/download/101-batch-image-foundry%2Flocal-web%2Fv0.2.2-build.1091-macos-arm64/batch-image-foundry-0.2.2-1091-Local-Web-macos-arm64.zip) |
| Windows x64 · 本地 Skill / 网页 | 0.2.2（1092） · 预览版 | [下载 ZIP](https://github.com/EspalierLin/ai-tool-releases/releases/download/101-batch-image-foundry%2Flocal-web%2Fv0.2.2-build.1092-windows-x64/batch-image-foundry-0.2.2-1092-Local-Web-windows-x64.zip) |
| Mac · Apple 芯片 | 0.2.1（1089） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/101-batch-image-foundry%2Fv0.2.1-build.1089-macos-arm64/Batch-Image-Foundry-0.2.1-1089-macOS-arm64.dmg) |
| Windows x64 | 0.2.1（1089） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/101-batch-image-foundry%2Fv0.2.1-build.1089-windows-x64/Batch-Image-Foundry-0.2.1-1089-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片 · 本地 Skill / 网页：`7494ab30d6ac39bc873b073ecf67c0ac57e1579d20ece4e8506f0001b736ce7b`
- Windows x64 · 本地 Skill / 网页：`3f6d93afc73b1266a1627711a41297b6c3901e01f34915aaec8518da19626a9c`
- Mac · Apple 芯片：`c4ae888f17a95b087d18cd2ff6c5d0be5ba38b7bb792e9c925e37bffb7a465d0`
- Windows x64：`6fa7796900a60f5cebaa0dcdc5fed27753843c5d15f630d941eae732247febbd`

</details>

<!-- release-downloads:end -->

支持范围：Mac 为 macOS 14+／Apple 芯片，Windows 为 Windows 10+／x64。两份本地 ZIP 使用完全相同的网页资源。Mac ZIP 已实际启动并验证浏览器／AI 联动、保存与重新打开；Windows ZIP 已校验材料、完整性和网页一致性，尚未做 Windows 实机运行。Linux、Intel Mac 和手机的完整本地版本次不提供。

当前均为公开预览。桌面 Mac 尚未完成 Developer ID 公证，Windows 安装包尚未代码签名；Windows 最新安装／升级仍待实机验收。没有把包校验或界面打开等同于真实在线生图验收。

## 安装与继续使用

桌面版：Windows 运行 EXE；Mac 打开 DMG，将应用拖入“应用程序”。Mac 被系统阻止时，先核对本页校验值，再按 [Apple 官方说明](https://support.apple.com/zh-cn/102445)处理。桌面更新入口为“设置 → 检查更新”；Mac 保存更新 DMG 后手动安装。

Skill 版：安装下面所述的完整 ZIP 后，由 AI 读取 SKILL.md 并调用随包脚本；无参数即可打开本机浏览器工作台。生图使用你本人连接的账号和额度，首次安装不自动登录或生图。

工程是用户选择位置的完整 .elproject 文件夹，含任务、图片、设置和历史；图片 ZIP 只是成图交付。程序目录、工程和设备授权分开。切换入口前安全关闭不兼容的运行实例，不强退活跃任务。私人公司插件按自己的授权另行安装，不包含在公开包里。

本地 Skill ZIP 当前采用**安全退出后完整替换程序目录**的更新方式，保留外置工程、授权和偏好；未接入桌面 EXE／DMG 自动更新，不只替换网页。桌面 App 的原有更新渠道继续有效。

<details>
<summary>给 AI 的安装规则</summary>

1. 未获同意时只读说明并介绍，询问是否安装。检测当前 OS／CPU，以及 AI 宿主能否在当前电脑执行命令、写文件和加载 Skill；不要声称纯云端 AI 能安装到用户电脑。
2. 同意后固定本页发布的对应 Local-Web ZIP、版本、build 和 SHA-256；不要选择 Source code ZIP、桌面安装包、插件或全仓库 latest。下载到临时目录，核对 manifest.json 中的大小和本页摘要。Release 中另有 manifest.json 和独立 ZIP.sig；首次信任以用户选择的本官方入口为基础，不信任包内任意新公钥。
3. 按当前 AI 宿主正式的 Skill 安装规则确定用户目录，不改全局 Python／Node，不现场编译。ZIP 只有一个 batch-image-foundry 根；检查路径不越界后完整解压，保留可执行权限。已有同名目录先核对来源和版本，禁止覆盖活跃运行材料或其他 Skill。
4. macOS 使用该目录 scripts/run.sh，Windows 使用 scripts/run.cmd。完整引用路径，支持空格和非 ASCII 字符。先读 --help、--version 和 skill --json；这些静态操作不创建工程或连接账号。需要发现新 Skill 的宿主按其规则刷新，不把目录存在当已成功加载。
5. 通过 runtime status 核对已有实例。版本／界面不兼容时请其所有者安全关闭，不删锁、不杀进程。用 ui open --no-launch 检查本机完整网页入口，只连接返回的 127.0.0.1；不改为远程服务器或局域网服务。
6. 创建工程前确定用户希望的本机位置，独立于程序目录。接下来按随包 SKILL.md 查询真实命令，AI 和网页操作同一工程，不直接改工程 JSON、不另建 AI 数据副本。
7. 账号登录或本人授权文件导入由用户在原工作台完成；不得读取其他 App 的登录、收集聊天里的 token 或自动使用别人的额度。安装同意不授权生图，原有人工确认仍有效。
8. 成功后用用户语言说明安装位置、实际版本和使用入口；报告真实失败与平台限制，清除本次临时下载／解压。更新前沿 runtime stop 等待安全点，再完整替换该 Skill 的程序目录；保留外置状态、工程及未完成任务。

</details>

[返回工具目录](https://github.com/EspalierLin/ai-tool-releases)
