# Diagram Design · 中文实践入口

> 维护位置：个人 Fork `sunkai-hit/diagram-design` 的社区扩展目录（非上游官方中文版本）。  
> 适用范围：ChatGPT、普通浏览器、兼容 Agent Skills 的 IDE。  
> 依据：仓库 `skills/diagram-design/SKILL.md`（2026-10-09 检查时元数据版本 2.6，44 种图表类型）。

## 先读这里

- [不使用 Codex，如何在 ChatGPT 中工作](CHATGPT_WORKFLOW.zh-CN.md)
- [中文技术图表设计规范](DIAGRAM_GUIDE.zh-CN.md)
- [制造业 ERP 采购到入库·脱敏泳道图（HTML）](examples/erp-procurement-swimlane.html)
- [示例业务边界及校验说明](examples/erp-procurement-README.md)

## 三句话理解

1. **Fork 不是安装**：此仓库保存原始 Skill 规范和模板；ChatGPT 并不会因为 Fork 而自动、永久装载 Skill。
2. **浏览器即可打开成果**：生成的自包含 HTML + 内联 SVG 不依赖 Codex；下载 HTML 后直接双击打开。
3. **复用靠流程约定**：每次生成应先加载 `SKILL.md`、选定的 `references/type-*.md`、`references/output-spec.md`、`references/style-guide.md`，再选尺寸、受众和图表复杂度。

## 文件和版权边界

- 原项目核心内容、README 和模板**保持原样**，扩展文件集中在 `community/sunkai-hit/`，方便未来同步上游。
- 本目录为补充说明及自制示例，不表示得到了上游作者的官方认可；遵守仓库 MIT 许可证。
- **公开仓库只放脱敏示例**。不得从私有 ERP/其他客户项目直接复制需求说明书、真实供应商、采购价格、客户身份、业务数据、内部系统路径或商业秘密。
- 具体客户流程是否正确，以客户已经确认的需求和项目仓库中的审批状态为准；示例文件不得当作验收证据。
