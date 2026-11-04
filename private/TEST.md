# PaperWeave Local Workflow Test

- date: 2026-11-04
- scope: 本次真实Agent读取本地论文并执行精简MD流程；不是在所有模型或平台上的自动化保证。
- public_files: 7；无Python代码、JSON schema或虚构示例。
- main_size: 36 lines。
- sample: [EIR paper](papers/Equilibrium_Analysis_of_Energy_Imbalance_Reserve_in_Day-Ahead_Electricity_Markets.pdf)

| step | actual result |
| --- | --- |
| input | 在docs识别到14页EIR accepted manuscript；从首页核实标题、作者和DOI。 |
| source placement | 移至private/papers；移动前后SHA-256一致，文件名不变。 |
| map | 生成8节点地图，明确市场问题、三阶段模型、结果与适用限制。 |
| deepen | 重走市场/时间线、两结算减日前量、命题推论证明链三个既有问题；记录PDF页和公式号。 |
| judgment | 沿用用户原句：建模全面、方法不复杂、写作优雅，是未来Trans范本。没有生成新的用户评价。 |
| save | 写入一份[Markdown记录](notes/tempr_2026_ent_eir_equilibrium.md)，包含来源、回忆钩子、地图、深入、判断、标签与历史。 |
| library | [LIBRARY.md](LIBRARY.md)能打开记录、DOI和原文。 |
| tags | [TAGS.md](TAGS.md)保留17个已确认、4个建议、6个警示和2个非主要标签，分类与旧存档一致。 |
| recall | 按“Trans写作范本”、“Proposition Corollary”、DOI、原始文件名，均能唯一找到本地记录。 |
| privacy | PDF、记录和索引都被子仓库忽略；git add --dry-run只包含7个工具文件。 |

## Recall Test Output

输入：“找那篇Proposition Corollary写得优雅、之后写Trans参考的论文。”

结果：[Equilibrium Analysis of Energy Imbalance Reserve in Day-Ahead Electricity Markets](notes/tempr_2026_ent_eir_equilibrium.md)。
已确认writing_reference、transactions_writing_template、proposition_corollary_structure；建议标签没有被当作用户确认。

## Checks and Boundaries

- 先检查并修复了空白模板中两个不能在模板位置解析的假链接，改成填写说明。
- 已验证工具和个人记录中的文件链接、标签锚点与原文哈希。
- 没有运行GAMS/PATH或复现论文数值实验；本次测试的是阅读、记录与回忆流程。
- DOI从论文首页取得；没有声称测试了外网DOI解析。
- 结果需要Agent执行文件操作；加载MAIN本身不是后台程序。
- 原私人仓库的历史记录没有修改；这份测试输出也不会上传公开工具仓库。

## Subsequent Policy Change

- 2026-11-04: 用户要求由最终使用者自行决定笔记版本管理。工具包已取消对private/的忽略，保留PDF忽略。上面的隐私检查描述的是改动前测试状态，不代表当前Git规则；本次没有上传任何内容。
