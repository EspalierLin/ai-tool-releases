# Meshpalier

在模型表面和 UV 贴图上联动绘画，用 AI 生成或修改材质，再通过普通图层精修。工程保存在你选择的位置。

## 下载安装

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.4.4（1019） | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/meshpalier%2Fv0.4.4-build.1019-macos-arm64/Meshpalier-0.4.4-1019-macOS-arm64.dmg) |
| Windows x64 | 0.4.4（1019） | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/meshpalier%2Fv0.4.4-build.1019-windows-x64/Meshpalier-0.4.4-1019-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`f500baeddee7d6628d44ec5b8d9e99bd071930187e6663cd8e8f0be02828b37a`
- Windows x64：`3c2cf6a091c3458ec811f1139448ee379ee65e651e2aaa777ae8811f4e6dfd09`

</details>

<!-- release-downloads:end -->

Mac：macOS 14+／Apple 芯片，打开 DMG 后把 Meshpalier 拖入 Applications。Windows：Windows 10+／x64，退出旧实例后运行安装 EXE，可选择本机安装目录。

安装包自带运行环境、几何核心和可编辑拱门 Demo，无需另装 Python 或 Blender。

## 开始绘画

1. 从文件库打开“AI 拱门材质 · 可编辑成品”，或导入 GLB、glTF、FBX、OBJ 及其贴图附件。另存为自己的工程后继续编辑。
2. 选择材质通道和图层，在模型或 UV 上绘制；画笔、选区、填充、仿制和图案图章操作同一份纹理。
3. 连接本人 AI 账号后，在 AI 材质中选择通道、填写要求并添加参考图。底色通过六正交投影与原 UV 补绘处理；辅助通道接收当前通道、Base Color 和模型参考。
4. 预览后点击“采用为图层”再修改作品，可撤销和继续绘画。保存修订保留图层与通道；按需要导出可编辑工程、模型或 PBR 贴图。

“当前通道”查看正在编辑的贴图，“材质效果”查看已启用通道的组合。关闭通道效果不会删除数据。AI 使用本人账号与额度，生成会带上已采用的 AI 图层和人工笔触。

## 保存与更新

工程、模型、材质图层和账号独立于应用安装目录。更新前先保存作品并正常退出旧实例。

Windows 在“设置 → 检查更新”中点击“更新并重启”，完成下载验签、保存协调、安装和重新启动。Mac 检查并保存更新 DMG 后手动替换应用。

旧版如果无法完成自动安装交接，手动运行本页当前安装器覆盖升级一次。升级保留原工程与账号；另存可创建独立工程副本。

[返回工具目录](https://github.com/EspalierLin/ai-tool-releases)
