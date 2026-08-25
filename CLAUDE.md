# 项目 AI 规范


---

## 文件命名规范（跨仓统一 · Peter 2026-07-11）

- **新建文件一律英文命名**（`type_topic.md` / `topic-desc.md`，小写 + `-`/`_`，不含中文 / 空格 / `$ , !` 等特殊字符）；**内容可中文**（正文 / 标题 / frontmatter 随意）。
- **存量中文名文件不回改**（改名会断 Notion 一文一页幂等键、乱 git 历史 / blame）；仅在文件本就大改且未推 Notion 时逐个评估。
- 摄入数据（转录 / 抓取等）用**稳定 ASCII 键**命名（如 `<日期>_<平台>-<ID>.md`），不用中文标题当文件名；中文标题保 frontmatter。
- 完整规则见总控仓 `chuhaiji/dev-control` 的 `docs/ops/NAMING_CONVENTION.md`。

<!-- DEVSTD:BEGIN (由 dev-control 分发·勿手改;改动请到 dev-control/templates/claude/CLAUDE.block.md) -->

## 跨仓开发约定（dev-control 统一分发）

本仓遵循总控仓 [`chuhaiji/dev-control`](https://github.com/chuhaiji/dev-control) 的跨仓约定：

- **文件命名**：新建文件用英文名（`type_topic.md` / `topic-desc.md`，小写 + `-`/`_`，不含中文/空格/特殊字符）；**内容可中文**。存量中文名文件不回改。
- **工程工作流**：采用 `superpowers` 插件工作流 —— `/brainstorming` → `/writing-plans` → 实现（`/subagent-driven-development`）→ `/test-driven-development` → `/systematic-debugging` → `/requesting-code-review` / `/receiving-code-review`。分层适用见 dev-control `docs/ops/DEV_WORKFLOW_STANDARD.md`。
- **提交纪律**：宣称"完成"前先跑验证拿证据（`verification-before-completion`）；合并 main 前过一次 code-review。
- **★ 子代理模型分层（硬规矩·默认执行）**：搜索 / 扫描 / 审计 / 批量机械改动**派子代理去做**，且**必须显式传 `model`**——不传＝继承主会话贵模型白烧额度。搜索查证 / 多文件扫描 → `sonnet`；纯机械（改配置 / 跑脚本 / 批量替换）→ `haiku`。只有架构 / 调试 / 判断类才配 Opus，而那类活主脑自己干、不外包。详见 `devstd:token-efficient-development` §3。
- **★ 汇报只给结果（默认执行）**：汇报写**结论 / 问题 / 待拍板事项**，**不复述过程**——不列跑了哪些命令、读了哪些文件、分几步查的。工具调用用户自己看得到，不用文字再讲一遍；要细节他会问。
- **★ 所有回答先简明，解释按需给（Peter 拍板·通用规矩，不限开发中）**：**每次回复都尽量简单明了**——直接答问题 / 做了什么 / 有没有问题 / 下一步。**不要主动展开**背景、原理、方案对比、风险清单、大表格。**他要解释会问**，问了再展开。
  - 判据：默认短。他明确问「为什么 / 什么意思 / 怎么做 / 详细说」→ 才展开。一切问答都如此,不只开发进度。
  - 结论仍要**完整**：做完了就说做完了，有坑必须说坑（一句话点到即可），**不能为了短而漏问题**。
  - 落档铁律不变：实质汇报仍先写文档再汇报，**但对话里只给摘要 + 文件路径**，不把文档内容再讲一遍。
- **AI 会话**：本仓 `.claude/settings.json` 已订阅 **devstd 频道**（`devstd@dev-control`，跨仓开发标准技能：命名/治理/铁律/UI 探针/提示词/安全红线等，改动只在 dev-control 一处，全仓自动更新）并启用 superpowers（随仓走，云端会话亦加载）；个人/本机专属设置请放 `.claude/settings.local.json`（不提交）。

> 本段由 dev-control 的 `sync-claude.sh` 统一维护，改动请到母本 `templates/claude/CLAUDE.block.md`，勿在本仓手改。

<!-- DEVSTD:END -->
