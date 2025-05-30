# Adaptive Margin-Control Note

## Term Sheet（结构条款说明书）

### 产品名称

Adaptive Margin-Control Note（自适应保证金控制票据）

### 产品类型

结构化衍生品票据（路径依赖 + 内嵌资金池 + 用户可控补仓）

### 标的资产

沪深300指数 / 黄金期货 / 铜期货（任选一种，具体产品中明示）

### 投资币种

人民币（CNY） / 美元（USD）

### 投资期限

12个月（可变，按产品设计）

### 最小投资金额

￥100,000 起步（或等值美元）

### 收益结构

* 标的资产涨幅 $R_t$ = $(S_t - S_0)/S_0$
* 若 $R_t < 20%$，按实际涨幅线性分配
* 若 $R_t \geq 20%$，则触发敲入

  * 收益封顶为 30%
  * 超过 30% 的部分进入风险补偿资金池（Protection Pool）

### 敲入条款（Knock-In）

* 触发条件：标的资产累计涨幅超过 20%
* 效果：自动启动收益封顶机制（30%）
* 同时将超额收益转入资金池，可用于后续补仓

### 资金池机制（Protection Pool）

* 起始为空
* 敲入后超额收益转入
* 客户可选择：

  * 不动用
  * 一次性注入保证金账户
  * 部分提取用于“续命”

### 保证金机制与自动补仓

* 初始保证金为投资本金的10%
* 维持保证金线为本金的5%
* 若账户权益跌破维持保证金线：

  * 系统将自动调用资金池进行补仓
  * 若资金池不足，则补至最大能力
  * 若补仓后仍低于维持线，则触发敲出

### 敲出条款（Knock-Out / Termination）

* 触发条件：权益低于维持保证金线 且 资金池为空
* 效果：产品终止，结算时返还剩余权益

### 用户控制权

* 用户可在系统平台或指定界面：

  * 查看资金池余额
  * 发起注入请求
  * 配置自动或手动补仓策略

### 风险提示（简要）

* 本产品非资本保证，最大亏损可能达本金全额
* 涉及杠杆机制、期货标的、资金池动态结构
* 投资者需具备衍生品投资经验与风险承受能力

### 定价方式

* 使用蒙特卡洛模拟对标的资产路径进行仿真
* 计算最终收益期望，作为理论发行价格参考
* 可根据实际市场波动、利率等参数校准发行价

### 示例场景图（可附图）

1. 正常上涨 → 敲入 → 收益封顶 + 池子注满
2. 市场反转 → 接近强平 → 客户主动或自动补仓
3. 市场震荡 → 最终仍持仓到期 → 按实际路径结算

### 项目状态

模拟设计，用于结构设计作品展示与GitHub项目发布。
非真实发行产品，仅用于教学与研究用途。

---

（此Term Sheet可配合白皮书、定价模型、风险说明一起提交）
