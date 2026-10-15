# 3D Asset Shader · 3D资产Shader制作

在 3D 模型和 UV 贴图上联动绘画，用 AI 生成材质，再通过图层继续精修。工程保存在你选择的位置。

## 当前版本

**0.4.0 / 1007 · Preview 预览版**。Mac Apple Silicon 和 Windows x64 分别提供安装包。

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.4.1（1008） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/pixel-texture-painter%2Fv0.4.1-build.1008-macos-arm64/3D-Asset-Shader-0.4.1-1008-macOS-arm64.dmg) |
| Windows x64 | 0.4.1（1008） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/pixel-texture-painter%2Fv0.4.1-build.1008-windows-x64/3D-Asset-Shader-0.4.1-1008-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`e37a79e9587931536836b483223f9b5296dca61bbde47bc693c73eeea2c3b45d`
- Windows x64：`074778c7c3ddb23ccd6ccb0d0bd3ffad37599d96e3f55dd04d0d1a0cd01b7ba5`

</details>

<!-- release-downloads:end -->

## 可以做什么

- 导入 GLB、glTF、FBX 或 OBJ，在模型表面与 UV 平面绘制，使用图层、选区、填充、仿制和图案图章修改。
- AI 底色按六正交立方体展开图绘制，投影回原 UV 后补绘未覆盖区域；提示词与参考图按通道保存。
- 从底色继续生成 Normal、Roughness、Metallic、AO、Emissive 和 Height；各通道分别编辑和开关预览。
- 文件库内置“AI 拱门材质 · 可编辑成品”，包含七通道图层。临时示例需要另存为普通项目，修改才长期保留。
- 保存可继续绘画的工程包，导出模型与贴图。随包提供运行环境和几何处理能力，无需另装 Python 或 Blender。

## 安装与使用

Mac：下载 DMG，打开后将应用拖入 Applications，从安装位置启动。支持 Apple Silicon，声明最低 macOS 14；最低系统实机验收尚未完成。

Windows：下载 x64 安装 EXE，运行安装器后从快捷方式打开。本批未在 Windows 机器安装运行。

打开文件库中的拱门示例即可查看效果。右侧选择正在编辑的贴图通道；“当前通道”显示该贴图，“材质效果”显示已开启通道的组合效果。关闭预览通道不会删除图层。AI 生成使用本人连接的账号，可分别填写提示词和参考图。

## 预览范围

本版保留内部签名资格：Mac 为 ad-hoc、未公证，Windows 未签名。Mac 已实际安装并打开 Demo，完成过绘画、撤销、保存和重开；正式本人账号的新版收费 AI 管线尚未实测。

通过本页手动下载更新。升级时保留用户工程；更新前先保存正在编辑的内容。
