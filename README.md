# 你好，我是 RS 场景工作台

我是你的场景搭建小助手。把房屋拆成可复用的模块，我帮你预览、摆放、整理楼层和材质；同一份工程还可以在 Rhino 中建模，在 UE 5.4 中加载和继续布置。

- **模块库**：看真实模型缩略图，搜索和筛选模块，旋转预览后再放进场景。
- **场景编辑**：选择实例、调整位置和角度，管理楼层与联动范围；用 Ctrl/Cmd+G 打组、Ctrl/Cmd+Shift+G 解组，或点击对应按钮；保存、另存、撤销和重做沿同一份工程。
- **一份文件，多处接着做**：正式模型采用 FBX，贴图和模块配表跟着工程走，Rhino 不必另存完整场景 3dm。

## 工作台下载

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.6.0（17） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fv0.6.0-build.17-macos-arm64/RS-Scene-Workbench-0.6.0-17-macOS-arm64.dmg) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`cae2b955057da49bd1a684a34eabc960505903241dfd99e763061738542f10a4`

</details>

<!-- release-downloads:end -->

Mac：macOS 14+，Apple 芯片。打开 DMG 后把 App 放入「应用程序」。Windows：Windows 10+，x64，运行 EXE 安装。包内包含运行环境，不必拉取源码或安装 Python。

## Rhino、UE 与示例

先安装 build 17 或更新版本的对应系统工作台，它同时为插件提供本地文件服务。随后选择需要的插件：

| 内容 | 下载 | 怎样用 |
|---|---|---|
| Rhino 8 · RSRhino 1.4.1 / OctoWalker 1.2.1 | [下载 Mac / Windows 插件 ZIP](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fplugins%2Frhino-v1.4.1/RS-Rhino-1.4.1.zip) | 保存并退出 Rhino，运行包内对应安装脚本；重新打开空白 Rhino，执行 RSStudio |
| UE 5.4 · 场景插件 0.3.1 | [下载源码插件 ZIP](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fplugins%2Fue-v0.3.1/RS-SceneDocument-0.3.1-UE5.4-source.zip) | 放入项目 Plugins/RSSceneDocument，用 UE 5.4 编译并启用；Window → RS 场景工程 |
| 山坡小屋 · FBX 示例 | [下载完整示例](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fexamples%2Fv0.6.0/RS-Hillside-House-v0.6.zip) | 完整解压到可写位置，打开其中的 .elproject 目录 |
| 场景数据合同 | [读取合同 Markdown](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fexamples%2Fv0.6.0/SCENE_DATA_SPEC.md) | 对接模块、实例、材质通道和跨软件保存规则 |

UE ZIP 包含源码、安装说明和 BuildPlugin 脚本，Windows 编译需要 Visual Studio 2022 的 C++ 游戏开发工具。新建 C++ Blank 项目、空关卡，打开插件面板选择工程，实例会挂到一个普通根 Actor 下；移动根 Actor 属于 UE 关卡操作。

`.elproject` 是完整目录工程。移动时带走整个目录；要独立副本时使用「另存为」。请从上面的链接下载，GitHub 的 Source code ZIP 是页面源码快照。

## 更新

工作台 **设置 → 检查更新**：检查版本，下载并验签。Windows 支持交给安装器更新并重启；Mac 保存 DMG 后手动替换 App。build 15 及更早版本需从本页安装新版一次，此后可使用软件内检查更新。

Rhino 和 UE 插件从本页下载新版后分别安装：Rhino 先保存并退出；UE 先退出并重新编译项目插件。更新工作台不会自动覆盖这些宿主插件。工程和账号保存在程序外，更新保留它们。

[查看全部工具](https://github.com/EspalierLin/ai-tool-releases)
