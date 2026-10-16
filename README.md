# Imbalier

在一个本地工程中批量制作图片：统一提示词和参考图，逐项生成，筛选历史，再导出成图。工程和账号留在自己的电脑上。

## Windows 下载

<!-- release-downloads:start -->

| 系统 / 组件 | 版本 | 下载 |
|---|---|---|
| Mac · Apple 芯片 | 0.2.3（1093） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/imbalier%2Fv0.2.3-build.1093-macos-arm64/Imbalier-0.2.3-1093-macOS-arm64.dmg) |
| Windows x64 | 0.2.3（1093） · 预览版 | [下载安装包](https://github.com/EspalierLin/ai-tool-releases/releases/download/imbalier%2Fv0.2.3-build.1093-windows-x64/Imbalier-0.2.3-1093-Windows-x64.exe) |

<details>
<summary>下载文件校验（SHA-256）</summary>

- Mac · Apple 芯片：`73037b7f0ab28d6019f39442693286c63c515fee54934f08368258dd70c28f4c`
- Windows x64：`f691ce5ccf79d7e640ea786141a1cee7815ddbff66815b44967cdaac4beac1e9`

</details>

<!-- release-downloads:end -->

下载 x64 安装 EXE，保存作品并退出旧程序后运行；支持选择本机安装目录。包内包含 Python、WebView2 和必要执行器，无需克隆仓库。声明支持 Windows 10+／x64，本次新包的实际 Windows 安装与升级验收尚未完成。

0.2.3 修复 Windows 请求账本误判、另存草稿冻结，以及更新交接和深层路径处理。更新保留外置工程、图片、账号和已装插件；私人公司插件独立安装，不包含在公开包里。

## 更新和其他版本

在“设置 → 检查更新”中检查并下载验签；支持新协议的 Windows 宿主可点“更新并重启”。旧版若在安装交接处取消或失败，请手动运行本页安装器覆盖升级一次。之后读取本页对应的新更新入口。

[Mac 安装包与本地 Skill／网页下载](https://github.com/EspalierLin/ai-tool-releases/tree/101-batch-image-foundry)保留此前实际发布的版本及安装说明，旧包仍显示 Batch Image Foundry。两种入口使用同一工程格式；网页运行在本机。

当前为公开预览；Windows 安装器尚无系统代码签名。安装包和更新清单另有原产品 Ed25519 签名。本次不把源码检查或完整解包作为 Windows 实机验收；[实际验证范围](https://github.com/EspalierLin/ai-tool/blob/101-batch-image-foundry/docs/INSTALL_UPDATE_SYSTEM.md)。

[返回工具目录](https://github.com/EspalierLin/ai-tool-releases)
