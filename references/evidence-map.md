# 证据地图

核对日期：2026-11-18。下面以原文功能和定位说明依据，不转载长段原文。页码均指下载 PDF 的文件页；章节／图表编号优先于页码。XML 全文使用 section 标题定位。

章节物理起始页和图表组合已另行核对，见 [page-budget.md](page-budget.md) 及 [figures-and-layout.md](figures-and-layout.md)。其中实际页码和图表编号属于语料观察，满页、段末行饱满以及不用破折号冒号属于用户要求，不据此声称作者本人始终如此写作。

## 跨篇规则对应

| 规则 | 直接依据 | 适用程度／反例 |
|---|---|---|
| 从实际困难收束到明确设计要求 | GBM §1；PPO §1；PPD §1；PromptPilot §1 | 多篇支持；具体困难因任务而异 |
| 让方法表述回应核心缺口 | PPO §1、§3；PPD §1、§3；PromptPilot §1、§2 | 多篇支持；不代表每篇都有可宣称的新范式 |
| 方法开头先总览输入、表示与流程 | GBM §2；PPO §3；PPD §3；PromptPilot §2 | 多篇支持，长稿可先补任务定义 |
| 特征与空间等互补条件驱动机制分工 | GBM §2.2；PPO §3；PromptPilot §2.1–2.3 | 提示分割工作中强；非领域通用架构要求 |
| 消融与条件变化回应设计主张 | GBM §3.3；PPO §4.3；PPD §4.2；PromptPilot §3.4–3.5 | 不能因此说 IFP 也做了相同消融 |
| 第一张图解释动机或核心概念 | PPO Fig.1；PPD Fig.1；PromptPilot Fig.1；BI-Cap Fig.1 | GBM 和 IFP 的 Fig.1 是总览，明确例外 |
| 不固定独立 Related Work | PPO／PPD 有；GBM／IFP／PromptPilot 没有 | 体裁、篇幅和叙事依赖决定 |
| 训练与推理需分清 | PPO §3；PPD §3.2–3.3；PromptPilot §2；IFP §2 | 四篇协议不同，不能互换 training-free 含义 |
| 结果不能超出证据 | 各文结果与主张对照 | 这是本 skill 的准确性约束，不声称原文始终无过度表述 |
| 不复制模板残留或英语问题 | PPD v1 页眉与 Index Terms；多稿表达差异 | 属编辑纠错，不能蒸馏成作者习惯 |

## 第一／共同第一作者全文

### GBM：Feature-prompting GBMSeg，MICCAI 2024

- 来源：[arXiv 2406.16271v1](https://arxiv.org/abs/2406.16271v1)；[正式论文 DOI](https://doi.org/10.1007/978-3-031-72114-4_27)。本次读到的是标注录用于 MICCAI 的预印本全文，不声称逐字核过出版社版本。
- 角色：刘雪宇第一作者，作者单位可从第一页核实。
- 结构：Introduction → Methodology（Patch-level feature extraction、Automatic prompt engineering）→ Experimental Results（数据、实现、消融、比较）→ Conclusion。
- 摘要：临床对象和自动分割需求；一张标注参考引导；特征对应、提示优化、基础分割模型；数据与数值证据；后续测量方向。
- 引言：从 GBM 评估与已有自动方法走到标注和泛化负担，再引入基础模型能力与自动提示。
- 方法：§2 总览先给三个环节；§2.2 按前向匹配、反向匹配、空间采样等解释提示改进；反向匹配的必要性来自前向错误。
- 图表：文件第4页 Fig.1 总览，第5页 Fig.2 提示流程；§3.3 消融连接具体机制。
- 可迁移：把应用约束直接落实到模块；对每一步说明“剩余问题是什么”。
- 不迁移：把其 TEM 数据量／DSC 当作用户结果；强制每篇仅需一张参考或完全无需训练。

### PPO：Plug-and-Play PPO，CVPR 2025

- 来源：[CVF 正式录用版](https://openaccess.thecvf.com/content/CVPR2025/html/Liu_Plug-and-Play_PPO_An_Adaptive_Point_Prompt_Optimizer_Making_SAM_Greater_CVPR_2025_paper.html)。正式页码 4332–4342。
- 角色：刘雪宇、Rui Wang 共同第一作者。
- 结构：Introduction → Related Work → Methodology → Experiments → Conclusion。
- 论证：SAM 的提示依赖；错误或拥挤提示影响输出；提出语义关系与空间分布要求；构建图环境并用策略优化。
- 方法：§3 总览先给两类距离矩阵、图环境、训练和推理；§3.1–3.3 展开。
- 证据：§4.3 双空间消融；比较与不同初始提示实验对应性能和即插即用主张。
- 图表：Fig.1 把失效类型可视化；Fig.2 展示流程。
- 可迁移：把“质量不好”拆成可操作的设计条件，再检验条件。
- 不迁移：优化器经过训练，不能据“新任务不再训练”说整个系统未训练；首创性表述须另行核实。

### PPD：Attack for Defense，CVPR 2026

- 来源：[CVF 正式录用版](https://openaccess.thecvf.com/content/CVPR2026/html/Liu_Attack_for_Defense_Adversarial_Agents_for_Point_Prompt_Optimization_Empowering_CVPR_2026_paper.html)；[早期 arXiv v1](https://arxiv.org/abs/2509.18891v1)。正式版优先，早期版仅用于版本比较。
- 角色：正式版刘雪宇、Xiaoyi Zhang 共同第一作者。Lead Contact 不是刘雪宇，不能凭第一作者身份编造通讯角色。
- 结构：Introduction → Related Work → Method → Experiments → Conclusion，含运行效率与局限说明。
- 论证：静态／启发提示与已有优化中的反馈及初始条件问题；通过攻防训练制造并修复失效；推理保留防御者。
- 方法：§3.1 环境，§3.2 对抗训练，§3.3 推理；真值初始化与奖励属于训练说明。
- 证据：§4.2 消融，§4.3 SAM 方法比较，§4.4 效率。
- 图表：Fig.1 概念分工；Fig.2 训练／测试流程；图注用不同线型说明阶段。
- 版本差异：v1 使用旧期刊模板与模板词条；正式版作者表、栏式、部分编码器说明改变。不能用早期页眉推断正式发表期刊，也不将两个版本算成两个独立风格样本。
- 可迁移：核心想法先可视化，方法段落清楚区分学习过程和最终使用方式。

## 通讯作者全文

### PromptPilot，ICML 2026

- 来源：[PMLR 306 / shi26p](https://proceedings.mlr.press/v306/shi26p.html)，正式论文 PDF 11页。
- 角色：刘雪宇为通讯作者之一及 Lead Contact，第一页明确列出。
- 结构：Introduction → Method → Experiments → Conclusion；没有独立 Related Work。
- 论证：按适配、启发式、单 agent 等路径梳理；把瓶颈明确为目标冲突、优化与最终分割反馈的错配、单点贡献难以分配。
- 方法：§2.1 建图，§2.2 actor，§2.3 manager；分工直接对应问题拆解。
- 证据：§3.3 整体比较，§3.4 消融，§3.5 即插即用；正文对每类证据交代用途。
- 图表：Fig.1 概念，Fig.2 总览。
- 可迁移：把多目标冲突写清后再介绍协调机制；贡献列表是四项，不是固定三项。
- 同名排除：arXiv 2510.00555 的另一篇 PromptPilot 是其他作者的 LLM 交互工作，未纳入。

### IFP，CVPR Findings 2026

- 来源：[CVF 正式录用版](https://openaccess.thecvf.com/content/CVPR2026F/html/Xia_Instruction-Focus-PromptSemantics-Driven_Structural_Prompts_for_Universal_SAM_Segmentation_CVPRF_2026_paper.html)，6页。
- 角色：刘雪宇通讯作者／Lead Contact；稿件另有全作者贡献声明，不据姓名顺序推断独立执笔。
- 结构：Introduction → Methodology → Experimental Results → Conclusion。没有独立 Related Work。
- 论证：局部视觉对应和文本全局语义分别有不足；从文本、语义焦点、局部结构之间的连接构成方法。
- 方法：§2.1 跨模态焦点对齐，§2.2 结构一致性；每种约束对应一个明确的不完整／不稳定来源。
- 图表：Fig.1 为总览；Table 1 按视觉类与文本类方法分组；Fig.2 定性比较。
- 可迁移：技术名称、方法小节与比较对象按问题分类对齐。
- 不迁移：对齐模块有训练，不因基础模型未微调就称整个流程完全免训练；表中平均值优势不等于所有数据集全优。

### DSAGL，2026修订预印本

- 来源：[arXiv 2505.23341v3](https://arxiv.org/abs/2505.23341v3)，28页；[作者主页](https://xueyuliu.github.io/#publications)列为 EAAI 2026。本次未核对期刊排版全文。
- 角色：刘雪宇通讯作者之一。
- 结构：Introduction → Related Work → Method → Experiment and Results → Discussion → Conclusion。
- 特征：任务定义在框架前；分别展开 teacher／student、注意力、损失与训练；含符号汇总。
- 证据：§4.5 分析骨干、部件、训练、损失、超参数；§4.6 可视化；§5 讨论优点、弱监督边界和未来方向。
- 可迁移：长稿允许更细的定义、分层实验与讨论。
- 不迁移：不能据此强制其他论文单列 Discussion；文中对某基准的长篇解释不作为所有稿件的写作要求。

## 合作论文全文：作为体裁补充

### MSA-MIL，2020预印本

- 来源：[arXiv 2007.00858v2](https://arxiv.org/abs/2007.00858v2)，25页；刘雪宇为合作作者。
- 观察：从肾小球棘突识别的临床难点出发，摘要按区域提取、实例学习、分类／可视化说明处理链。方法与应用对象关系直接。
- 用途：早期医学算法的流程叙事参照。题录中的2024分类／量化论文与它主题接近，但未在没有版本证据时强行合并为同一工作。

### D4PM，2025预印本

- 来源：[arXiv 2509.14302v1](https://arxiv.org/abs/2509.14302v1)，5页；刘雪宇为合作作者。
- 观察：摘要先交代干扰去除需求与两类不足，再给双分支和联合后验采样；方法分为模型与采样；实验包括整体比较、消融、波形展示。
- 用途：紧凑技术稿的互补信息建模和步骤解释。
- 准确性提示：查看原表可见并非每项指标均最优。不要把原文强表述蒸馏成无条件的写作规则。

### BI-Cap，2026预印本

- 来源：[arXiv 2604.17927v1](https://arxiv.org/abs/2604.17927v1)，11页；刘雪宇为合作作者。
- 观察：从系统性与随机性鸿沟提出机制模拟及不确定性表示；方法先问题定义；结尾单列局限，说明检索任务与跨被试差异。
- 用途：把不同误差来源对应到不同机制，以及不确定性／跨模态写作。
- 版本边界：PDF 的 IEEE 期刊页眉不是已正式录用的独立证明。

### Life，多模态肾病分类，2023

- 来源：[正式全文 XML](https://www.ebi.ac.uk/europepmc/webservices/rest/PMC9960995/fullTextXML)；[DOI](https://doi.org/10.3390/life13020399)。
- 观察：从多显微方式和医生工作负担引出处理链、模态互补与分类结果；讨论涉及样本与图像条件。
- 作者角色限制：贡献声明把刘雪宇列为 Software，把原稿写作列为 Fang Hao。只作为“其参与论文的应用体裁参照”，不能证明他的个人措辞偏好。

### RA，低剂量 IL-2 临床合作，2021

- 来源：[正式全文 XML](https://www.ebi.ac.uk/europepmc/webservices/rest/PMC8107675/fullTextXML)；[DOI](https://doi.org/10.1177/1759720X211011370)。
- 身份：论文中的 Xue-Yu Liu 单位为太原理工大学 College of Data Science；有数据库关联支持，未把临床措辞归为其独立写作。
- 观察：结构式摘要；引言围绕免疫细胞数量／比例与治疗证据缺口；方法、结果和讨论围绕研究对象、治疗与终点组织。
- 用途：保留不同体裁，不强制所有署名论文使用算法论文框架。2020预印本和2021期刊版按同题归并。

## 只有题录／摘要的论文能支持什么

SAT、MSMTSeg、SemHyperSurv、GLMKD、综述等已进入题录清单，但本次没有获得可用的完整论文正文。作者仓库 README 只能提供身份、项目与公开概述线索，不能冒充论文正文。

它们可用于：确认题名、主题、发表线索、作者角色或补充检索。它们不能用于：断言具体章节安排、图序、实验解释方式、英语句法习惯，或“所有论文都如此”。取得全文后再补相应证据卡。
