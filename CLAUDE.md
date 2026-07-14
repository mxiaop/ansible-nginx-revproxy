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
- **AI 会话**：本仓 `.claude/settings.json` 已订阅 **devstd 频道**（`devstd@dev-control`，跨仓开发标准技能：命名/治理/铁律/UI 探针/提示词/安全红线等，改动只在 dev-control 一处，全仓自动更新）并启用 superpowers（随仓走，云端会话亦加载）；个人/本机专属设置请放 `.claude/settings.local.json`（不提交）。

> 本段由 dev-control 的 `sync-claude.sh` 统一维护，改动请到母本 `templates/claude/CLAUDE.block.md`，勿在本仓手改。

<!-- DEVSTD:END -->
