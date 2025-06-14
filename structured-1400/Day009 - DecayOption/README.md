# DecayOption 模型说明书

## 模型概述
DecayOption 是一种基于高阶导数贡献衰减率的结构化衍生品模型。它通过定义新的标的变量 `DecayIndex`，捕捉组合在结构复杂性维度上出现“非线性风险释放”前的预兆行为。

## 核心功能
1. **生成高阶导数贡献序列**：通过扰动路径模拟价格变化，计算 2~5 阶导数贡献。
2. **计算 DecayIndex**：对贡献序列进行加权归一化，判断是否触发敲入条件。
3. **模拟结构爆发场景**：敲入后模拟组合 VAR、Delta、Gamma 等指标，定义赔付逻辑。
4. **Monte Carlo 定价**：通过多路径模拟，计算触发率与期望赔付。

## 可视化
模型生成的图表包括：
- 原始价值函数图
- 各阶导数贡献图
- DecayIndex 与阈值对比图
- Monte Carlo 模拟结果直方图

## 风险说明
- 模型依赖于高阶导数估计，适用于高频多路径模拟。
- 不适用于极端事件预测，仅作为结构行为信号的放大器。

## 文件结构
- `pricing_model.py`：模型实现代码。
- `simulation_charts/`：存储生成的可视化图表。
- `risk-disclosure.md`：风险披露。
- `scenario-examples.md`：场景示例。
- `term-sheet.md`：条款说明。
- `whitepaper.md`：白皮书。
- `说明.md`：中文说明文档。