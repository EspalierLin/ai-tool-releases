# Meshpalier

在模型表面和 UV 贴图上联动绘画，用 AI 准备或修改材质，再通过普通图层继续精修。工作工程保存在你选择的位置。

## 下载安装

本页提供预览版。安装包内含运行环境、几何核心和可编辑拱门 Demo，不需要另装 Python 或 Blender。

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.4.3（1010） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/meshpalier%2Fv0.4.3-build.1010-macos-arm64/Meshpalier-0.4.3-1010-macOS-arm64.dmg) |
| Windows x64 | 0.4.3（1010） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/meshpalier%2Fv0.4.3-build.1010-windows-x64/Meshpalier-0.4.3-1010-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`bdb6af325006e9efa322ef264de1eadb2e0500c5ff6fd927550ae93e0522d2f7`
- Windows x64：`e9612defc75d53d50242d8d949e70051f3d4d951bc84052aa1e2c2fdeaade293`

</details>

<!-- release-downloads:end -->

Mac：下载 Apple Silicon DMG，打开后将应用安装到 Applications；声明最低 macOS 14，最低系统实机验收尚未完成。

Windows：下载 x64 安装 EXE，退出旧实例后运行安装器；本轮未在 Windows 电脑实际安装联网。

## 开始绘画

1. 从文件库打开“AI 拱门材质 · 可编辑成品”，或导入 GLB、glTF、FBX、OBJ 及其附件。临时示例需要另存普通项目，修改才长期保留。
2. 在模型与 UV 上绘制，使用图层、选区、填充、仿制、图案图章修改；两处写入同一份作品。
3. 在 AI 材质中选通道、填提示词或放参考图。底色经过六正交展开绘制和原 UV 补绘；辅助通道接收 Base Color、当前通道贴图及模型结构参考。每次生成都带上当前已采用 AI 图层与人工笔触，可直接写修改要求。
4. 预览候选后点“采用为图层”才修改作品，可撤销；保存修订后可继续绘画，或导出模型和贴图。

“当前通道”看正在编辑的原图；“材质效果”显示已启用通道的组合。各通道可单独开关，关闭效果不会删除数据。AI 使用本人连接的账号；底色流程通常调用两次，辅助通道一次。重新处理尺寸复用原图，不重新调用 AI。

## 更新

1010 修复旧版覆盖更新后再次打开示例或工程时报 `mutation_policy declaration is invalid`：打开时自动升级旧 AI 字段声明，保留已有模型、图层和生成记录，无需清缓存或重建工程。

当前版本已接上工具内的更新入口、公开签名渠道和安装包校验。Mac 检查并下载新 DMG 后手动替换应用；Windows 通过原生安装器交接，需要先保存作品并退出旧实例。不会因为下载完成就把版本伪记为已安装。

1007/1008 缺少完整更新接线，需要先从本页手动安装当前 1010 一次。升级保留工程与账号命名空间，更新前仍应先保存当前作品。Windows 自动安装交接尚待真实 Windows 机器验收。

## 预览范围

Mac 使用 ad-hoc 签名、未公证；Windows 安装器未签名。本版不标记为公开稳定版。发行清单和安装包另有本工具独立的 Ed25519 签名，它与系统发行者证书不同。

本轮已用真实旧版示例和工程验证升级与连续重启，核对两平台最终安装包及签名更新来源；没有完成 Windows 实机安装联网、本轮原生窗口视觉或真实 AI 新生成的验收。保留已接受的分层 Demo，未重新绘制其艺术素材。
