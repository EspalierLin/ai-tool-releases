# Meshpalier

在模型表面和 UV 贴图上联动绘画，用 AI 准备或修改材质，再通过普通图层继续精修。工作工程保存在你选择的位置。

## 下载安装

本页提供预览版。安装包内含运行环境、几何核心和可编辑拱门 Demo，不需要另装 Python 或 Blender。

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.4.3（1010） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/meshpalier%2Fv0.4.3-build.1010-macos-arm64/Meshpalier-0.4.3-1010-macOS-arm64.dmg) |
| Windows x64 | 0.4.4（1019） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/meshpalier%2Fv0.4.4-build.1019-windows-x64/Meshpalier-0.4.4-1019-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`bdb6af325006e9efa322ef264de1eadb2e0500c5ff6fd927550ae93e0522d2f7`
- Windows x64：`3c2cf6a091c3458ec811f1139448ee379ee65e651e2aaa777ae8811f4e6dfd09`

</details>

<!-- release-downloads:end -->

Mac：下载 Apple Silicon DMG，打开后将应用安装到 Applications；声明最低 macOS 14，最低系统实机验收尚未完成。

Windows：下载 x64 安装 EXE，退出旧实例后运行安装器，可自行选择本机安装目录。1019 已在 Windows 11 x64 实际安装，并验证连续两次应用内升级；Windows 10 最低系统验收尚未完成。

## 开始绘画

1. 从文件库打开“AI 拱门材质 · 可编辑成品”，或导入 GLB、glTF、FBX、OBJ 及其附件。临时示例需要另存普通项目，修改才长期保留。
2. 在模型与 UV 上绘制，使用图层、选区、填充、仿制、图案图章修改；两处写入同一份作品。
3. 在 AI 材质中选通道、填提示词或放参考图。底色经过六正交展开绘制和原 UV 补绘；辅助通道接收 Base Color、当前通道贴图及模型结构参考。每次生成都带上当前已采用 AI 图层与人工笔触，可直接写修改要求。
4. 预览候选后点“采用为图层”才修改作品，可撤销；保存修订后可继续绘画，或导出模型和贴图。

“当前通道”看正在编辑的原图；“材质效果”显示已启用通道的组合。各通道可单独开关，关闭效果不会删除数据。AI 使用本人连接的账号；底色流程通常调用两次，辅助通道一次。重新处理尺寸复用原图，不重新调用 AI。

## 更新

Windows 0.4.4 / 1019 修复正常请求账本被误判损坏导致示例无法打开的问题，保留原账本和已有作品。未保存绘画可以直接另存工程；中文和空格路径、取消另存、普通保存、冷重开及 GLB 导出已经安装版实测。原设备状态下的示例正常退出、同版本冷重启和再次打开也已验证。

Windows 在“设置 → 检查更新”中点击“更新并重启”，自动下载验签、协调保存、退出旧实例、安装并重新启动；健康确认后回收本次安装备份、更新助手和已消费下载。已实际通过 1017 → 1018 → 1019 连续两次升级，保存的工程保持完整。Mac 检查并下载 DMG 后仍需手动替换应用。

旧 Windows 版本若提示安装取消或交接未完成，请运行本页最新安装器完成一次覆盖升级；旧版自身的更新缺陷无法靠下载新清单修复。1007/1008 缺少完整更新接线，也需先手动安装对应平台的当前包。升级保留工程与账号命名空间，更新前先保存作品。

## 预览范围

Mac 使用 ad-hoc 签名、未公证；Windows 安装器未签名。本版不标记为公开稳定版。发行清单和安装包另有本工具独立的 Ed25519 签名，它与系统发行者证书不同。

本轮完成 Windows 原状态示例冷重启、实际绘画保存/另存/重开、GLB 导出及连续一键更新和回收验收。Mac 保持原 1010 发布，本轮未重新构建或运行；未进行新的真实 AI 生图，也不把本机结果扩大到全部系统、磁盘类型或模型。完整范围见[桌面交付记录](https://github.com/EspalierLin/ai-tool/blob/102-pixel-texture-painter/docs/DESKTOP_DELIVERY.md)。保留既有分层 Demo。
