# Blueprint Role Marketplace

Blueprint 官方角色的 GitHub 仓库索引。每个角色在自己的仓库维护源码、版本和 Releases。

[marketplace.json](marketplace.json) 是机器可读索引。每个条目包含三个字段。

| 字段 | 含义 |
| --- | --- |
| `packageId` | 角色包清单中的稳定包 ID |
| `repository` | 角色仓库的 GitHub `owner/repo` |
| `repositoryId` | GitHub API 返回的稳定数字仓库 ID |

读索引时可固定到一个 Git 提交。需要安装角色时，从对应仓库读取已发布的稳定 Release，并下载该包的 `<packageId>-<version>.blueprint` 附件。版本和文件校验信息由角色 Release 提供。

新增官方角色时，先用 [角色模板](https://github.com/agentofreef/blueprint-role-template) 准备源码，手动发布并下载验证 `.blueprint`，再提交索引条目。
