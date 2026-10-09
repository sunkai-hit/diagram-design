# 在 ChatGPT 中使用 Diagram Design（无 Codex）

## 重要澄清

本方式是**读取并遵循图表 Skill 的规则**，不是把 `diagram-design` 安装为 ChatGPT 系统级插件。Fork 本身也不会令 ChatGPT 自动读取全部文件。长期复用可以把 Skill 的关键规范文件上传至一个专用 ChatGPT 项目，或者每次明确给出 GitHub 文件地址让助手读取最新版本。

## 零安装方案

1. 打开仓库 `https://github.com/sunkai-hit/diagram-design`，无需本地 Git / Node.js。
2. 在 ChatGPT 中说明要生成的业务对象、受众、图表类型、尺寸和交付格式。
3. 要求助手先读取：
   - `skills/diagram-design/SKILL.md` — 全局规则；
   - `skills/diagram-design/references/type-<类型>.md` — 图表专属规范，如 `type-swimlane.md`；
   - `skills/diagram-design/references/output-spec.md` — 16:9、节点数、字级、格式；
   - `skills/diagram-design/references/style-guide.md` — 配色与中文字体验；
   - `skills/diagram-design/references/primitives-core.md` — SVG 连线约束。
4. **第一次生成**先约定企业品牌色/字体，或者明确使用项目默认样式。这是上游 Skill 的风格入门门禁；未经选择不应假装已完成品牌配置。
5. 让助手先输出节点及业务关系摘要，标明未经确认的步骤；审阅后再做 HTML + SVG。
6. 直接打开 HTML 看排版；需要 PPT 可以进一步从 HTML **导出** PNG / SVG（查看 `references/export.md`），不要把 HTML 截图误当可编辑 PowerPoint 原生元素。

## 可直接复制的提示词

```text
请按 https://github.com/sunkai-hit/diagram-design 的 Diagram Design Skill 制图：
先读取 skills/diagram-design/SKILL.md、references/type-swimlane.md、
references/output-spec.md、references/style-guide.md、references/primitives-core.md。
类型：跨部门泳道图；受众：产品负责人和业务部门；画幅：slide-16x9（1280×720）。
语言：简体中文；字体回退：Noto Sans SC / Microsoft YaHei / PingFang SC。
先列出角色、步骤、正常路径与异常条件；客户未确认的细节标为“待确认”，不得编造。
绘图遵守不超过 9 个关键节点、直角连线、无阴影、最多 2 个强调节点，
输出自包含 HTML（内联 SVG；无需外部字体服务），必要时再导出 PNG/SVG。
请说明图表为“示例”还是“已确认业务流程”。
```

## 选图速查

| 想解释的问题 | 推荐类型 |
|---|---|
| ERP 采购、检验、入库由哪些部门交接 | Swimlane |
| IBMS / AI 平台的层次与系统关系 | Architecture 或 Layer Stack |
| 数据怎样从设备 / 外部系统流入业务平台 | Data Flow |
| 系统部署在什么网络、主机、容器 | Deployment |
| 需求实现前后拓扑怎么变 | Architecture Delta |
| 研发里程碑和交付计划 | Timeline / Gantt |
| 结构化数据库表及外键 | Database Schema / ER |

## 常见误区

- **不是**“复制仓库 URL 就能在任何对话自动执行 Skill”。
- 如果助手不能访问 GitHub，可上传 `SKILL.md` 和所选 `references` 文件；不要声称已经完整加载。
- 上游当前有 44 种图表类型，网络流传的旧截图可能仍标 42。
- 图表中的业务箭头不是审计结论；必须和项目的正式需求/流程复核。
- 开源并不意味着可以公开私人客户数据：工作文件留在各自私有仓库，本 Fork 只存脱敏样例。
