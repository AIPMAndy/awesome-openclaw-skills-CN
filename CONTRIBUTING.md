# 参与贡献（Awesome OpenClaw Skills CN）

这是一个面向中文开发者的 OpenClaw Skills 精选列表。我们只整理指向 [OpenClaw 官方 skills 仓库](https://github.com/openclaw/skills/tree/main/skills) 的链接。

> 本仓库是“链接索引”，不是技能代码托管库。你提交的 Skill 必须已经发布在官方仓库里，否则无法收录。

## 如何新增 Skill

### 1) 条目格式

请在 `README.md` 对应分类末尾追加：

```markdown
- [skill-name](https://github.com/openclaw/skills/tree/main/skills/author/skill-name/SKILL.md) - 一句话描述（建议 10 个英文单词以内）。
```

如果同一作者在同一领域有多个 Skill，请优先合并为作者目录入口，避免列表冗长：

```markdown
- [author-skills](https://github.com/openclaw/skills/tree/main/skills/author) - 对该作者技能集合的简要说明。
```

### 2) 放置位置

- 找到最匹配的分类，追加到该分类末尾
- 若没有完全匹配的分类，可放在最接近的分类，并在 PR 描述中说明原因

### 3) 收录要求

- **必须已经发布到 [OpenClaw 官方 skills 仓库](https://github.com/openclaw/skills/tree/main/skills)**
- 必须有 `SKILL.md` 文档
- 描述应简洁、可读
- 需有真实社区使用价值（优先收录被实际采用、经过实践的 Skill）
- 暂不收录 crypto / blockchain / DeFi / finance 类 Skill

### 4) PR 标题格式

`Add skill: author/skill-name`

## 更新现有条目

- 可通过 PR 修复失效链接、拼写错误、描述过时等问题
- 若 Skill 已下线或废弃，可提交 issue 或 PR 进行移除

## 安全策略

我们只收录在 [ClawHub](https://www.clawhub.ai/) 上未被标记为可疑的 Skill。

如果你认为当前列表中的某个 Skill 存在安全风险，请提交 [issue](https://github.com/VoltAgent/awesome-openclaw-skills-CN/issues)，我们会尽快复核并处理。

## 重要说明

- 本仓库只整理链接，Skill 本体均在 OpenClaw 官方 skills 仓库
- 提交前请自行确认链接可访问、格式正确
- 维护者会审核所有提交，不符合质量标准的条目可能被拒绝
- 请勿重复提交与现有条目功能高度重叠的 Skill

## 获取帮助

- 先查看已有 [issues](https://github.com/VoltAgent/awesome-openclaw-skills-CN/issues) 与 PR
- 有问题可新开 issue
- 具体技能用法请阅读对应 `SKILL.md`
