# AI Tool Releases

工具介绍、版本说明和下载入口。当前只发布 Batch Image Foundry；main 提供入口，工具分支维护介绍与版本。后续工具须明确选择后才加入。

**仓库导航已可用。Batch Image Foundry 已接入公共更新功能；正式安装包仍需完成发行资格，没有已公开的安装包或插件附件。**

| 工具 | 用途 | 下载 | 状态 |
|---|---|---|---|
| [Batch Image Foundry](https://github.com/EspalierLin/ai-tool-releases/blob/101-batch-image-foundry/README.md) | 按任务批量生成图片，保存提示词、参考图、结果与历史，筛选后导出。 | [下载说明](https://github.com/EspalierLin/ai-tool-releases/blob/101-batch-image-foundry/downloads/README.md) | 待发布 |

## 下载与更新

进入工具分支，阅读使用条件、版本说明和下载表，选择对应系统的正式 Release 附件。GitHub 自动提供的 Source code ZIP/TAR 是本发布仓库的文档快照，不是应用安装包。

应用与可公开插件分别发布，版本互不混用。安装包不会携带作者凭据或用户作品；内部插件不属于此仓库的发布范围。

接入公共更新能力的应用可检查、下载并验签对应应用／公开插件更新。支持的平台宿主可在保存并安全退出后安装，其他宿主保存安装包后手动安装。已有无更新入口的版本需要先安装一次含该能力的新版本。

## 发布仓库组织

- main：工具导航、发布政策、目录元数据。
- 工具分支：该工具的 README、下载说明和版本索引。
- GitHub Releases：该工具标签对应的安装包与签名附件。
- 应用标签：`工具分支/v软件版本-build.构建号`；插件标签：`工具分支/plugins/插件ID/v版本`。
- 稳定版和预览版按工具分别选择；不使用整个仓库的 latest Release 作为某个工具的最新版。

[发布说明](PUBLISHING.md) · [仓库政策](repository-policy.json) · [工具目录](catalog.json) · [所有 Release](https://github.com/EspalierLin/ai-tool-releases/releases)
