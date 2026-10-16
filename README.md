<p align="center">
  <img src="assets/assistant.png" width="160" height="160" alt="紫色的 Meshpalier 小助手" />
</p>

<h1 align="center">你好，我是 Meshpalier</h1>

<p align="center"><strong>你的模型材质绘制小助手，陪你把模型一层层画到满意。</strong></p>

把模型带来，我们一起给它画上材质。你可以在三维表面和 UV 贴图上直接绘画，也可以让我借助 AI 生成候选，再挑出合适的作为图层，接着精修。

- **模型和贴图一起看**：在三维表面与 UV 之间联动观察和绘画。
- **每一层都能接着改**：人工笔触和已采用的 AI 结果分层保存，可以撤销、修改和继续绘制。
- **作品带进下一步**：保存可编辑工程，按需要导出模型和 PBR 贴图。

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
3. 连接本人 AI 账号后，在 AI 材质中选择通道、填写要求并添加参考图。我会参考当前模型和已经绘制的材质，生成候选供你挑选。
4. 预览后点击“采用为图层”再修改作品，可撤销和继续绘画。保存修订保留图层与通道；按需要导出可编辑工程、模型或 PBR 贴图。

“当前通道”查看正在编辑的贴图，“材质效果”查看已启用通道的组合。关闭通道效果不会删除数据。AI 使用本人账号与额度，生成会带上已采用的 AI 图层和人工笔触。

## 保存与更新

工程、模型、材质图层和账号独立于应用安装目录。更新前先保存作品并正常退出旧实例。

Windows 在“设置 → 检查更新”中点击“更新并重启”，完成下载验签、保存协调、安装和重新启动。Mac 检查并保存更新 DMG 后手动替换应用。

旧版如果无法完成自动安装交接，手动运行本页当前安装器覆盖升级一次。升级保留原工程与账号；另存可创建独立工程副本。

[返回工具目录](https://github.com/EspalierLin/ai-tool-releases)
