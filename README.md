<p align="center">
  <img src="assets/assistant.png" width="160" height="160" alt="绿色的游戏场景小助手" />
</p>

<h1 align="center">你好，我是游戏模块化场景工作</h1>

<p align="center"><strong>你的游戏场景搭建小助手，陪你把一个个模块拼成完整世界。</strong></p>

你准备好墙、地板、屋顶和家具等模块，我帮你查看、摆放和整理它们。楼层、材质和遮挡联动关系一起留在本地工程里；配套 Rhino 与 UE 5.4 插件，围绕同一份工程接着编辑。

- **先看模块，再放进场景**：浏览真实模型缩略图，搜索筛选，旋转查看后再确认放置。
- **整座房子一起理顺**：选择实例、调整位置角度、管理楼层，用打组／解组按钮或快捷键建立视觉联动关系。
- **走进去看看**：在工作台里漫游，观察不同楼层，以及屋顶和近相机墙体的遮挡效果。
- **换软件接着做**：用同一份 `.elproject` 保存模块、实例、FBX 和贴图，支持打开、保存、另存和工程历史。

## 下载

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.6.0（17） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fv0.6.0-build.17-macos-arm64/RS-Scene-Workbench-0.6.0-17-macOS-arm64.dmg) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`cae2b955057da49bd1a684a34eabc960505903241dfd99e763061738542f10a4`

</details>

<!-- release-downloads:end -->

Mac：macOS 14+／Apple 芯片，打开 DMG 后把应用拖入 Applications。Windows：Windows 10+／x64，运行 EXE 安装。包内包含运行环境，不必克隆仓库或另装 Python。

## 开始搭建

1. 下载下方“山坡小屋”示例，完整解压到可写位置，从“文件 → 打开”选择其中的 `.elproject` 工程目录。
2. 左侧切换模块和场景实例；选模块会高亮全部引用，选实例会高亮实际选择集，右侧查看模块详情。
3. 多选实例后按 **Ctrl+G 打组、Ctrl+Shift+G 解组**，Mac 使用 **⌘**；也可以点击实例编辑区的对应按钮。保存后，配套插件读取同一套联动关系。

## Rhino、UE 与示例

先安装上方对应系统的最新版工具，它同时为插件提供本地文件服务。随后选择需要的插件：

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
