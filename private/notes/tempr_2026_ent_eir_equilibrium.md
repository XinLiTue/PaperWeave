# Equilibrium Analysis of Energy Imbalance Reserve in Day-Ahead Electricity Markets

## Identity

- paper_id: tempr_2026_ent_eir_equilibrium
- authors: Ryan Ent; Golbon Zakeri; Jinye Zhao; Tongxin Zheng
- year: 2026
- source: IEEE Transactions on Energy Markets, Policy and Regulation
- doi: [10.1109/TEMPR.2026.3722773](https://doi.org/10.1109/TEMPR.2026.3722773)
- version: accepted author manuscript, 14 PDF pages; not the final edited publication
- reading_date: 2026-09-29 (original conclusion); reviewed again 2026-11-04
- reading_status: archived
- source_filename: Equilibrium_Analysis_of_Energy_Imbalance_Reserve_in_Day-Ahead_Electricity_Markets.pdf
- source_path: ../papers/Equilibrium_Analysis_of_Energy_Imbalance_Reserve_in_Day-Ahead_Electricity_Markets.pdf
- source_sha256: 08db146a3d1edc44eebdbd7a436ff55dd68ec25d615d6de707fdb7a19653d52b
- original: [Local PDF](../papers/Equilibrium_Analysis_of_Energy_Imbalance_Reserve_in_Day-Ahead_Electricity_Markets.pdf)
- provenance: 本次按用户要求重新走精简工具包流程；结论与标签沿用此前已确认记录。原私人阅读库未修改。

## Recall

- one_sentence_memory: 那篇建模全面、方法不复杂，但Proposition-Corollary与结果机制解释非常优雅的EIR市场论文，是未来Transactions写作范本。
- why_saved: 用户明确认可建模、理论组织和结果分析写作，希望写Trans时能找回来。
- best_use: 市场参与者与时间线建模；日前/实时两结算；KKT加出清构成MCP；Proposition-Corollary的理论组织；数值结果的经济机制解释。
- not_suitable_for: 实证证明ISO-NE可靠性改善；网络约束备用调度；新求解算法或战略市场力分析。
- search_hooks: EIR; EMO EMIR; 那篇很优雅的市场论文; Trans写作范本; Proposition Corollary; 提前采购燃料; 3722773。

## Understanding Map

| node | gist |
| --- | --- |
| background | 燃气机组缺乏提前锁定燃料的激励，日前承诺与实时需求存在缺口。 |
| problem | EIR这个日前期权式产品是否改变燃料采购，风险偏好怎样影响其效果？ |
| approach | 三阶段：先购气，后日前市场，再实时情景；参与者KKT加出清形成MCP，外层比较投资策略。 |
| effect | 风险中性下两种市场有条件等价；风险厌恶时EIR可能提高提前采购，消费者成本也可能上升。 |
| innovation | 核心价值在新市场规则的行为均衡分析与机制解释，不是新MCP或CVaR算法。 |
| limitations | 单节点、无机组组合和跨时约束；无成本虚拟套利；可靠性用提前购气代理。 |
| user_fit | 高优先级Transactions写作参考与全面市场建模参考。 |
| recall_hooks | 那篇Proposition-Corollary写得优雅的EIR论文。 |

## Selected Deepening

### Question 1: 什么市场，何时生效，谁参与，如何出清？

- EIR是日前采购、按实时能量价格与strike price的差额进行期权close-out的产品。
- Stage 1: 发电商选择提前燃料合同；小算例枚举0、25%、50%容量的合同量。
- Stage 2: 日前能量、EIR与虚拟交易共同形成均衡价格和数量。
- Stage 3: 实时需求和燃料价格实现，机组生产、现货购气或转售剩余燃料。
- 参与者包括发电商、代表性需求代理和虚拟套利者；ISO通过出清约束出现。
- 内层将各参与者最优条件与日前/实时平衡、FER约束一起求解，使用GAMS/PATH。
- 外层比较燃料投资收益，寻找没有单方有利偏离的均衡；不是一个总代价目标的直接最小化。
- evidence: Section III，PDF pp.3-6；Eq.(8)投资均衡；Eqs.(6)-(7)能量平衡；Eq.(13)FER条件。
- caveat: 这是竞争性价格接受者均衡，作者明确区分它与真实价格-数量报价出清流程；不能当作ISO算法逐步复现。

### Question 2: 为什么实时收入要减去日前量？

式(2)的能量收入是：

\[
\lambda^{DA}g^{DA}+\lambda_s^{RT}(g_s^{RT}-g^{DA}).
\]

日前量先按日前价格结算；实时只结算实际出力相对日前承诺的偏差。它们不是两份互不相关的生产。
示意例子：日前10 MWh、实时实际12 MWh，价格50与80，收入为500+160=660；不是500+960。
这组数字仅用于解释，不是论文算例。

- evidence: Section III-A.1，PDF p.4，Eq.(2)；EMIR现金流见p.5 Eq.(10)。
- clarification: Eq.(10)还包括FER贡献价格rho和EIR close-out，不能将EMO与EMIR现金流完全混同。

### Question 3: Proposition-Corollary为什么值得模仿？

- Proposition IV.1：在风险中性、总容量超过FER等假设下，证明rho=0；若预期close-out为正，再得到EIR量为零。
- 证明链：无成本虚拟套利约束日前价格等于预期实时价格；若FER绑定而总容量有余量，存在容量不满机组，其容量乘子为零；KKT再迫使rho为零。
- Corollary IV.1：利用上述性质构造EMIR到EMO的均衡映射，保留相关实时变量及收益。
- Proposition IV.2：将内层收益关系提升到外层提前燃料采购博弈的均衡关系。
- Proposition IV.3：实时价格唯一时得到日前价格唯一，但数量不必唯一。
- evidence: Section IV，PDF pp.6-7。
- guarantee_scope: 这些是特定假设下的解析结论；Section V风险厌恶的政策发现是数值证据，不是普遍定理。

## Judgment

- user_quote: 这篇文章我基本理解了，写的非常好，虽然方法不复杂，但是建模很全面。同时后面的结果分析写作，包括，Proposition Corollary 这种形式我第一次见，但是非常优雅。我认为这会是我之后写作trans的范本。帮我记录，并在我之后写作论文进行思考的时候帮我找出来
- user_conclusion: 写得非常好，建模全面；方法不复杂；尤其保留理论组织和结果分析，作为之后Trans写作范本。
- agent_assessment: 工具多为已有MCP、KKT、CVaR和有限策略比较，价值在将市场规则转成连贯的行为模型，并解释参数何时起作用、何时失效。
- useful_figures_or_writing: 优先参考Section III市场模型、Section IV命题到推论再到外层博弈、Section V用小算例解释机制再扩展大算例的结构；图3-6的参数敏感性可辅助参考，但不是本次用户主要确认价值。
- evidence_limits: PDF pp.11-12 Section VI明确承认运行简化，并要求后续实证评估；不能把提前购气增加直接等同实际供电可靠性已验证。

## Tags

- decided_tags: energy_imbalance_reserve; day_ahead_market; real_time_market; two_settlement_market; market_equilibrium; mixed_complementarity_problem; KKT_conditions; CVaR; fuel_security; option_settlement; virtual_bidding; comprehensive_market_model; writing_reference; transactions_writing_template; proposition_corollary_structure; elegant_results_analysis; reading_complete
- suggested_tags: reserve_market_design; subgame_perfect_equilibrium; advance_fuel_procurement; forecast_energy_requirement
- warning_tags: single_node_model; no_unit_commitment; costless_virtual_arbitrage; reliability_proxy_only; continuous_investment_in_large_case; no_market_power
- negative_tags: none confirmed
- not_primary_tags: new_optimization_algorithm; distribution_network_congestion
- tag_provenance: 严格沿用原存档；没有把建议或警示标签升级为已确认。

## History and Next Step

- 2026-09-29: 用户确认基本理解，给出上述结论，要求作为未来Trans写作范本保存。
- 2026-11-04: 按用户要求在精简PaperWeave中重读本地PDF，生成地图、重走三个既有深入问题，复用原结论及标签；不是新的用户评价。
- next_action: 今后讨论Trans论文结构、市场清算建模或命题/推论组织时检索本篇。

## Links

- [Library](../LIBRARY.md)
- [Tags](../TAGS.md)
- [Confirmed writing-reference matches](../TAGS.md#writing_reference)
- [Confirmed proposition-corollary matches](../TAGS.md#proposition_corollary_structure)
