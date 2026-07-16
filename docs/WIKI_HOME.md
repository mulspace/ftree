# fTree 项目说明

欢迎来到 fTree Wiki。

fTree 是面向个人和家族资料维护场景的家谱服务。私人空间版无需注册，家谱默认保存在当前浏览器；用户可以下载加密的 `.tree` 备份，或授权 Google Drive、GitHub、GitLab 保存云端副本。

## 网站入口

- 私人空间版：<https://ftree.dpdns.org>
- Git 仓库：<https://github.com/mulspace/ftree>
- 完整用户指南：<https://github.com/mulspace/ftree/blob/main/docs/USER_GUIDE.md>
- 隐私说明：<https://github.com/mulspace/ftree/blob/main/docs/PRIVACY.md>
- 数据操守与操作手册：<https://github.com/mulspace/ftree/blob/main/docs/HANDBOOK.md>

团队协作版当前未开放公开注册。相关开放信息以网站和本 Wiki 公告为准。

## 项目能力

- 创建和维护多个家谱。
- 编辑成员姓名、性别、状态、备注和 GPS。
- 维护父母、配偶、子女及子女顺序。
- 指定开山祖并从任意成员查看家谱分支。
- 关联不同家谱中的同一成员。
- 通过地图查看已设置位置的成员。
- 导出家谱图片。
- 下载和导入加密 `.tree`。
- 同步全部家谱至个人授权的第三方云服务。

## 数据保存方式

### 浏览器本地

私人空间版默认把完整工作区作为加密、压缩档案保存在当前浏览器。没有服务端用户账户，也不会因为在另一台设备打开同一网址而自动出现原资料。

清理站点数据、使用无痕模式、删除浏览器配置、设备损坏或重装系统都可能造成数据丢失。必须定期下载 `.tree` 并保存到独立介质。

### Google Drive

备份保存为 Google Drive 隐藏应用数据目录中的 `default.tree`。该文件通常不显示在普通云盘目录中。

### GitHub

备份保存为包含 `default.tree` 的 Secret Gist。Secret Gist 不会正常进入公开搜索，但并非严格私有；获得链接的人可能访问，因此不得公开 Gist URL。

### GitLab

备份保存为包含 `default.tree` 的 Private Snippet。用户应定期检查可见性，并保护 GitLab 账户和双重验证设备。

### 服务端

Cloudflare Worker 负责 OAuth 和加密档案转发。应用不建立用户数据库，也不把家谱正文或用户 OAuth Token持久化到应用存储。第三方平台及网络基础设施仍可能依据各自条款处理请求元数据。

## 隐私保护要点

1. `.tree` 包含全部家谱、成员、关系、备注、GPS 和家谱关联，不是只包含当前页面。
2. 档案虽然使用压缩和加密，但当前没有用户独享密码，只能作为一般隐私屏障。
3. 不要把真实 `.tree`、Secret Gist URL、Cookie、Token 或 Client Secret 放到 Issue、Wiki、群聊或截图中。
4. 在世人员资料应遵循知情、最少收集和限制共享原则。
5. 在世人员通常不应记录住宅精确 GPS。
6. 成员头像和地图功能会访问额外第三方服务，可能产生姓名、IP、浏览器和地图区域相关请求。
7. 退出云端授权不会自动删除已经保存的 `default.tree`。
8. 删除资料时，应分别检查浏览器、下载备份和所有第三方云端副本。

详细内容请阅读[隐私说明](https://github.com/mulspace/ftree/blob/main/docs/PRIVACY.md)。

## 推荐操作流程

1. 使用现代浏览器打开正式 HTTPS 网站。
2. 新建家谱并填写堂号、开山祖、制作者和版本。
3. 逐个添加成员和亲属关系，每个家庭单元完成后核对连线。
4. 重要修改前后都下载 `.tree`。
5. 需要跨设备时，选择一个个人云服务并确认同步方向。
6. 在新设备恢复后核对家谱数量、成员数量和主要关系。
7. 每月至少执行一次备份恢复验证。

完整步骤见[用户操作指南](https://github.com/mulspace/ftree/blob/main/docs/USER_GUIDE.md)。

## 数据操守

- 只录入家谱目的所必需的信息。
- 录入在世人员资料前取得适当同意。
- 对争议资料记录来源和不确定性，不把推测写成事实。
- 不在备注中保存密码、完整证件号、医疗资料或敏感评价。
- 分享图片前检查所有在世成员信息。
- 支持人员不得要求用户提供真实档案或任何凭据。

资料整理者和维护人员应遵循[数据操守与操作手册](https://github.com/mulspace/ftree/blob/main/docs/HANDBOOK.md)。

## 备份建议

采用 3-2-1 原则：至少三份副本、两种介质、一份离线或异地副本。建议同时保留浏览器工作副本、个人云端副本和离线日期备份。

备份只有成功恢复并完成核对后，才能视为有效。

## 支持与反馈

所有事项统一通过 GitHub 分类提交并持续追踪：

| 类型 | 提交入口 | 追踪列表 |
| --- | --- | --- |
| 新功能、体验改进 | [提交需求 Issue](https://github.com/mulspace/ftree/issues/new?template=feature_request.yml) | [需求列表](https://github.com/mulspace/ftree/wiki/需求列表) |
| 页面错误、数据异常、同步故障 | [提交问题 Issue](https://github.com/mulspace/ftree/issues/new?template=bug_report.yml) | [问题列表](https://github.com/mulspace/ftree/wiki/问题列表) |
| 使用咨询、文档讨论、其他事项 | [在 Wiki 登记](https://github.com/mulspace/ftree/wiki/其他列表) | [其他列表](https://github.com/mulspace/ftree/wiki/其他列表) |

需求必须写清背景、目标、场景、验收标准、范围、替代方案及隐私影响。问题必须写清环境、前置条件、复现步骤、实际结果、期望结果、频率、影响和已尝试方法。

公开反馈不得提交：

- 真实 `.tree` 文件。
- OAuth Token 或 Cookie。
- Client ID、Client Secret 或服务密钥。
- 完整成员名单和私人备注。
- 在世人员精确 GPS。

请先查阅[支持与反馈填写规范](https://github.com/mulspace/ftree/blob/main/SUPPORT.md)、[用户操作指南](https://github.com/mulspace/ftree/blob/main/docs/USER_GUIDE.md)和[隐私说明](https://github.com/mulspace/ftree/blob/main/docs/PRIVACY.md)。
