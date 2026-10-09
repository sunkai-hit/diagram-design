# 制造业 ERP 采购到入库 · 脱敏泳道图

- 在线仓库源文件：[HTML](erp-procurement-swimlane.html) / [独立 SVG](erp-procurement-swimlane.svg)
- 类型：Swimlane；尺寸：slide-16x9，`viewBox="0 0 1280 720"`；受众：业务负责人/产品经理；细节：7 节点简化流程。
- 使用方法：下载 HTML 后用浏览器打开（无构建、无 JavaScript、无网络字体依赖）。SVG 可以用矢量工具打开或插入文档；离线中文字体按系统字体回退。
- 规则依据：`skills/diagram-design/SKILL.md`、`references/type-swimlane.md`、`references/output-spec.md`、`references/primitives-core.md`。

## 流程说明（非客户确认）

1. 需求部门发起采购需求。
2. 采购部门进行供应商选择、采购拟单。
3. **普通流程**：无涨价时直接发送采购订单。
4. **条件流程**：发生涨价时走审批分支，审批通过再发送订单。
5. 到货后进入质量检验，检验通过再进行验收入库。

> 为遵守视觉密度，这张总览图不展示供应商退换货、审批拒绝、价格补差、财务付款及特殊物料计量。**不应据此认定这些规则不存在。**
> “发生涨价时须审批”等表述来自需求讨论背景的抽象化呈现；公开示例没有附带私有客户原件，也没有对正式客户需求作核验或批准。

## 图片与源码校验

- HTML 是主源文件，独立 SVG 从其中的 `<svg>` 节点提取，与内联内容一致。
- SVG 使用 `<title>` / `<desc>` / `aria-labelledby`；节点文字含简体中文系统字体回退。
- 单图最多 9 个节点、横向 5 泳道、直角连线、只强调 2 个节点。
- 这次仅提供 HTML + SVG；如需要 PNG，请按 `skills/diagram-design/references/export.md` 通过浏览器渲染再导出，不能把尚未生成的 PNG 当成已交付结果。

## 安全说明

此文件所在仓库是 **Public**。图中的名称、字段、数值全部是演示用抽象信息；客户正式业务文档应放在对应的私有项目，按审批状态治理。
