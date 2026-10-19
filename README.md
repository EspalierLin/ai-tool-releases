<p align="center">
  <img src="assets/assistant.png" width="160" height="160" alt="绿色的游戏场景小助手" />
</p>

<h1 align="center">你好，我是 Scenalier</h1>

<p align="center"><strong>你的游戏场景搭建小助手，陪你把一个个模块拼成完整世界。</strong></p>

你准备好墙、地板、屋顶和家具等模块，我帮你查看、摆放和整理它们。楼层、材质和遮挡联动关系一起留在本地工程里；独立桌面、Rhino 和 UE 版都叫 Scenalier，围绕同一份工程接着编辑。

- **先看模块，再放进场景**：浏览真实模型缩略图，搜索筛选，旋转查看后再确认放置。
- **整座房子一起理顺**：选择实例、调整位置角度、管理楼层，用打组／解组按钮或快捷键建立视觉联动关系。
- **走进去看看**：在工作台里漫游，观察不同楼层，以及屋顶和近相机墙体的遮挡效果。
- **换软件接着做**：用同一份 `.elproject` 保存模块、实例、FBX 和贴图，支持打开、保存、另存和工程历史。

## 下载

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.7.0（24） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/scenalier%2Fv0.7.0-build.24-macos-arm64/Scenalier-0.7.0-24-macOS-arm64.dmg) |
| Windows x64 | 0.6.0（19） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fv0.6.0-build.19-windows-x64/rs-building-preview-0.6.0-19-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`1a76b7cac05aee14a2c81ae04ab0e89a691da84dba34c8e3b1b010182dd41965`
- Windows x64：`e7b407005e8a3dc014883499831861d3de7b90e9eaeb72f1327fda7840d45132`

</details>

<!-- release-downloads:end -->

Mac：macOS 14+／Apple 芯片，打开 DMG 后把应用拖入 Applications。Windows：Windows 10+／x64，运行 EXE 安装。包内包含运行环境，不必克隆仓库或另装 Python。

## 开始搭建

1. 下载下方“山坡小屋”示例，完整解压到可写位置，从“文件 → 打开”选择其中的 `.elproject` 工程目录。
2. 左侧切换模块和场景实例；选模块会高亮全部引用，选实例会高亮实际选择集，右侧查看模块详情。
3. 多选实例后按 **Ctrl+G 打组、Ctrl+Shift+G 解组**，Mac 使用 **⌘**；也可以点击实例编辑区的对应按钮。保存后，各版本读取同一套联动关系。

## Rhino、UE 与示例

Scenalier 的 Rhino 和 UE 版都是正式工具目标。原生扩展目录只是宿主加载形式；新版正式包由 Package 准备完整共同运行时，无需先装桌面版。

| 运行版本 / 内容 | 当前状态与下载 | 怎样用 |
|---|---|---|
| Scenalier · Rhino 8 · Mac Apple 芯片 | **0.7.0 / build 24** · [下载正式 ZIP](https://github.com/EspalierLin/ai-tool-releases/releases/download/scenalier%2Fv0.7.0-build.24-rhino-8-macos-arm64/Scenalier-Rhino-0.7.0-24-macOS.zip) | 保存退出 Rhino，解压运行安装 macOS.command，再执行 RSStudio；已包含共同运行时 |
| Scenalier · Rhino 8 · Windows | 新版已完成交叉编译与正式 ZIP 校验，待 Windows Rhino 实机验证，尚未发布；[此前 1.4.1 材料](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fplugins%2Frhino-v1.4.1/RS-Rhino-1.4.1.zip) 只作为旧版兼容入口 | 旧版需要匹配的旧运行时，不表示已具备本轮新的独立交付与登记流程 |
| Scenalier · UE 5.4 · Windows | 当前正式工具包待实际 Windows UE 5.4 UAT 编译及宿主验证；[此前开发源码](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fplugins%2Fue-v0.3.1/RS-SceneDocument-0.3.1-UE5.4-source.zip) | 源码 ZIP 属于开发材料，不能直接当作新版正式工具安装 |
| 山坡小屋 · FBX 示例 | [下载完整示例](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fexamples%2Fv0.6.0/RS-Hillside-House-v0.6.zip) | 完整解压到可写位置，打开其中的 .elproject 目录；原工程与历史保留 |
| v0.6 数据合同 | [读取已公开的数据合同](https://github.com/EspalierLin/ai-tool-releases/releases/download/rs-building-preview%2Fexamples%2Fv0.6.0/SCENE_DATA_SPEC.md) | 数据格式保持兼容；本轮新登记、加载与新导出统一使用 FBX，不再生成或依赖 3dm 作者源 |

Rhino Mac 正式 ZIP SHA-256：`cc47749605d1e4d11fab14fc28f0567469df79b7a37a3cf538c9cefe3c9db0eb`。

独立版可导入外部 FBX、按槽关联 PNG 并预览确认。Rhino 可从选中几何／Block 登记、更新或新增变体；新模块先入库，再明确放置。模块删除会保护全部场景引用，可通过工程撤销恢复。`.elproject` 是完整目录工程，移动时带走整个目录，独立副本使用「另存为」。

Windows 桌面下载表暂保留已发布的 0.6.0 / build 19；新的 0.7.0 / build 24 已完成交叉构建和安装包完整性检查，实际 Windows 安装启动尚未验证，保留为内部候选。当前先交付已验证的 Mac 版，旧 Windows 下载不冒充本轮改造。

## 更新

工作台 **设置 → 检查更新**：检查版本，下载并验签。Windows 支持交给安装器更新并重启；Mac 保存 DMG 后手动替换 App。build 15 及更早版本需从本页安装新版一次，此后可使用软件内检查更新。

Rhino／UE 版从本页选择对应目标的正式包分别安装，先保存并退出宿主；桌面更新不替换宿主版本。当前未提供的目标按表格标明。工程、账号与私有状态保存在程序外，更新保留它们。历史 rs-building-preview 地址继续提供同 UID 的兼容更新头。

[查看全部工具](https://github.com/EspalierLin/ai-tool-releases)
