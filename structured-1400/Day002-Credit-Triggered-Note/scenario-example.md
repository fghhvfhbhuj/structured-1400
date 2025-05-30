# Scenario Example — Credit-Triggered Note

## 📈 场景 1：正常到期路径

### 初始设定：

* 用户投入本金 ￥100,000
* 标的为某高收益债券，观察期为15天
* 总期限 1 年，年票息 10%，季度支付（共4期）

### 路径演化：

1. 用户进入结构票据，冻结期开始（第0\~15天）
2. 未触发敲出 → 第15天释放观察期贴现补偿金（约￥123）
3. 每季度获得票息：￥2,500，共四次
4. 到期获得本金返还：￥100,000

### 总结：

* 总收益 = ￥10,000 票息 + ￥123 补偿 = ￥10,123
* 年化收益率 ≈ 10.1%
* 结构安全运行，无违约事件

---

## 🚨 场景 2：信用评分触发敲出

### 初始设定：

* 同上，用户投入 ￥100,000
* 第30天，公司披露财报，ICR 和流动比率急剧下降

### 风控路径：

1. 评分函数输出连续 3 天评分 < 50 → 触发敲出
2. 系统计算：剩余3期票息 + 本金贴现 = ￥96,820
3. 加入保费补偿（π = ￥5,000）→ 总赔付 = ￥101,820
4. 用户自动获得赔付，结构终止，不再参与后续波动

### 总结：

* 用户本金未损失，获得接近原期望的赔付
* 结构在信用风险暴露前主动熔断，锁定结果

---

## 💬 场景解读建议

| 路径   | 用户体验          | 对应结构优势            |
| ---- | ------------- | ----------------- |
| 正常路径 | 获得所有票息，收益封闭可期 | 观察期返还提升认知合理性      |
| 敲出路径 | 无需主动操作，自动触发赔付 | 风控机制透明、可调、用户信任感增强 |

---

> 本示例用于教学说明结构票据的两类典型演化路径
> 实际使用中，参数、票息、评分函数可据真实数据调整
