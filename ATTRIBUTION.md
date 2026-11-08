# 署名与授权说明 / Attribution & Licensing

本文件用于满足 **CC BY 4.0**（Creative Commons Attribution 4.0 International）第 3(a) 条对署名、许可声明与修改标注的要求。

## 1. 原作品信息

| 项目 | 内容 |
| --- | --- |
| 作品名称 | Reme 雷米 |
| 作品类型 | Yes Steve Model（YSM）Minecraft Java 版模型包 |
| 原作者 | 是Reme |
| 作者角色 | 单人完成（模型、动画、贴图） |
| 参与人员 | 木土光军76（Bilibili UID 689067975），角色：指导与提供参考 |
| 作者主页 | https://space.bilibili.com/3546650257656003 |
| 作者爱发电 | https://afdian.com/a/ysmmod |
| 模组页面 | https://modrinth.com/mod/yes-steve-model |
| 原作品声明的许可 | CC BY（见 `ysm.json` → `metadata.license.type`） |
| 本仓库采用的许可 | CC BY 4.0，全文见 [LICENSE](LICENSE) |

## 2. 授权情况

本仓库由原作者授权整理并公开发布。`ysm.json` 中已载明原作者与协作人员信息及 CC BY 许可声明，本仓库在此基础上补充许可证全文与署名文件。如对授权范围有疑问，请先联系原作者确认。

## 3. 本仓库对原作品所做的修改

依据 CC BY 4.0 第 3(a)(1)(B) 条，公开再分发时须标注修改。本仓库相对于原始模型包的改动**仅限仓储层面的整理**：

1. 删除 macOS 元数据文件 `.DS_Store`。
2. 将两张作者头像重命名，并同步 `ysm.json` 中的引用路径：
   - `avatar/_20260804192555_14_12.png` → `avatar/author-reme.png`（原作者头像）
   - `avatar/69518a7114bbb96c87fb9a2a14a98be2.png` → `avatar/author-2.png`（协作人员头像）
3. 新增仓库文档与配置：`README.md`、`ATTRIBUTION.md`、`LICENSE`（CC BY 4.0 官方全文）、`.gitignore`、`.gitattributes`。

模型几何（`models/*.json`）、动画（`animations/*.json`）、贴图（`textures/**`）与其余 `ysm.json` 内容**未作任何修改**。

## 4. 再分发时的署名样例

```
Reme 雷米 — Yes Steve Model 模型包
原作作者：是Reme（https://space.bilibili.com/3546650257656003）
参与人员：木土光军76（指导与提供参考）
原作品以 CC BY 授权，本仓库以 CC BY 4.0 发布：https://github.com/linxiting890/YSM-Reme
许可证全文：https://creativecommons.org/licenses/by/4.0/legalcode
修改说明：仅做仓储整理（清理 .DS_Store、重命名作者头像文件并同步 ysm.json 引用、补充文档），未改动模型 / 动画 / 贴图内容。
```

CC BY 4.0 允许复制、再分发、修改乃至商业使用，但必须：

- 保留原作者署名与上述链接（可删除的要求除外）；
- 附上许可证全文或链接；
- 标注你是否修改过，并保留此前修改的说明；
- 不得以原作者名义为你的版本背书。

## 5. 第三方素材

本仓库不包含 Minecraft 原版游戏素材；Yes Steve Model 模组的代码与内置资源版权归模组作者所有，本仓库仅提供与其格式兼容的模型源文件。
