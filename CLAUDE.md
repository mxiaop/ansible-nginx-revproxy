# 项目 AI 规范


---

## 文件命名规范（跨仓统一 · Peter 2026-07-11）

- **新建文件一律英文命名**（`type_topic.md` / `topic-desc.md`，小写 + `-`/`_`，不含中文 / 空格 / `$ , !` 等特殊字符）；**内容可中文**（正文 / 标题 / frontmatter 随意）。
- **存量中文名文件不回改**（改名会断 Notion 一文一页幂等键、乱 git 历史 / blame）；仅在文件本就大改且未推 Notion 时逐个评估。
- 摄入数据（转录 / 抓取等）用**稳定 ASCII 键**命名（如 `<日期>_<平台>-<ID>.md`），不用中文标题当文件名；中文标题保 frontmatter。
- 完整规则见总控仓 `chuhaiji/dev-control` 的 `docs/ops/NAMING_CONVENTION.md`。
