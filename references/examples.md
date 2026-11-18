# 原创使用示例与行为检查

下列文本为演示性新写作，不是刘雪宇论文原句，也不声称方法由他提出。输入事实与预期结果用于检查本 skill 能否迁移逻辑、保留事实和控制范围。

## 示例一：剪枝／蒸馏摘要，尚无结果

**用户材料：** 结构化通道剪枝；已有一个跨层特征蒸馏机制；初步动机是局部通道评分忽略层间依赖；没有实验数字、数据集或方法名称。请按刘雪宇式逻辑写摘要。

**应做的决定：** 把评分局限转成结构／表示恢复问题，说明已提供的蒸馏机制；不补造“双 agent”、SAM、具体损失、SOTA 或数据。输入没有证明“剪枝必然破坏层间关系”，因此用可能性描述设计动机。

**可接受的原创草稿：**

> Structured channel pruning reduces the computational cost of deep networks by removing redundant channels. However, channel importance estimated in isolation may not capture dependencies across layers, leaving the resulting compact model without an explicit constraint on their preservation. We study a cross-layer feature distillation approach that guides the pruned network using representations from an uncompressed teacher. Rather than treating compression and representation recovery as unrelated steps, the approach introduces cross-layer guidance into the learning of the compact model. This design aims to preserve information shared across layers while reducing model cost. [Results under matched compression and training budgets remain to be supplied.]

**检查结论：** 方法内涵没有越过输入；最后一句明确缺结果。要写最终投稿稿，仍需要用户真实算法、压缩协议和结果。这是结构草稿，不是已完成实验的摘要。

## 示例二：只润色一个句子

**用户材料：** “Our method is very good and can solve all the problems of pruning.” 已知仅在两个图像分类基准的指定压缩率下优于基线。

**可接受输出：**

> Our method improves classification performance over the evaluated baselines on two image classification benchmarks under the specified compression ratios.

不要求用户先提供整篇论文，不输出六章大纲，不添加“首次”“显著”“任意模型”。若用户希望更有说服力，建议补具体指标与预算，而不是追加修饰语。

## 示例三：规划引言和方法图

**用户材料：** 已有模型用一个评分同时决定删除哪些通道，但用户观察到局部特征保留与跨层信息传递的要求不总一致。新方法有两个已有的评分项与一个权重调度机制。请求大纲与 Figure 1 规划，尚无定量实验。

**可接受结构：**

1. 压缩部署需求与通道剪枝操作。
2. 单一评分的实际失效条件，以用户已观察的例子说明。
3. 两个保留要求的关系及单一评分难以协调的原因，区分观察与待验证解释。
4. 引入双评分与调度，说明每项对应哪个要求。
5. 列出与真实机制一致的贡献；实验能力留待验证。

**Figure 1 建议：** 左侧是相同网络在一个已观察案例中的局部／跨层冲突；右侧是两个评分项与调度机制怎样形成最终选择。若左侧只是概念推演，标注为示意；不写虚构准确率。方法总览可在下一张图展开输入模型、评分、调度、剪枝掩码及恢复训练。

这里迁移的是 PPO／PromptPilot“把矛盾讲清再解释分工”的叙事功能。它不授权把方法改成强化学习或要求恰好有两个分支。

## 示例四：用户要求“按他所有论文的统一模板写”

**应做的决定：** 先按目标体裁选择已有全文支持的结构。说明不同论文有不同布局：GBM、IFP、PromptPilot 无独立 Related Work，PPO、PPD 有，DSAGL 有独立 Discussion。当前语料不能证明存在一个全论文统一模板。

不应声称已读完所有论文；不为满足措辞而凭综述题目捏造综述分类。若用户给出综述全文，则补读并蒸馏，不因当前语料缺口拒绝其他可完成的工作。

## 示例五：能力标签与结果边界

**用户材料：** 基础模型冻结；额外的提示优化器提前训练；新任务推理不更新参数。性能平均最好，但一个数据集落后。

**可接受表达：**

> The pretrained optimizer refines prompts for new tasks without updating the foundation model or retraining the optimizer. It achieves the highest average performance across the evaluated datasets, with gains varying by dataset.

不能写整个系统从未训练、每个数据集都最佳或已统计显著。允许用户进一步要求压缩句子，但这些事实限定保留。

## 示例六，满页规划与验证边界

**用户材料** 为 8 页双栏正文的会议稿，参考文献不计入，已有方法、真实实验及完整图表，但只提供纯文本。要求写满页数，每段不要留一两个词独占一行。

**应做的决定** 使用 page-budget 中的 8 页方案，列出预计章节起点与图表空间，执行正文标点规则。由于没有最终模板中的编译结果，不能声称已经达到 8 页或消除了物理短行。可先压缩明显冗余句，但不能为了减少行数删去真实条件。

**验收重点** 预算之和为 8 页，图表已算在各节空间中，未另加一份图表预算。末行问题保持待编译验证，不把纯文本里的自然换行当成最终页面行宽。

## 示例七，正文无破折号和冒号

**用户材料** 一段通过冒号引出方法、再用破折号插话的英文方法说明，同时包含数学公式、URL 和参考文献题名。

**应做的决定** 把说明改写成完整句子或准确从句，在生成的正文中不用破折号、冒号和分号。保留公式、URL 及参考文献的正确符号，不对文件进行全局标点替换。精确引用或固定题名需要原样保留时按 language-guide 的例外处理。

**可接受的原创正文**

> We refine the prompt set using feedback from the segmentation model. The refinement policy operates on the graph while the foundation model remains frozen. During inference, only the modules required for prompt refinement are retained.

这段示例仅在用户确实具有对应方法时使用。修改不能把“基础模型冻结”扩大成“整个系统从未训练”。

## 使用提示

调用形式示例：

```text
$snow-rain 请根据下面的真实方法和结果，先提炼核心矛盾，再重写英文 Introduction。保留已有引用，不编造实验。
```

```text
$snow-rain 检查这篇论文的“问题—机制—实验”是否闭合，并规划 Figure 1 和方法总览图。
```

```text
$snow-rain 只润色下面这一段，参考其论文中的逻辑推进方式，保持技术内容和结论强度。
```

```text
$snow-rain 按 8 页双栏正文规划这篇论文，列出各节篇幅、起始页和图表位置。正文不用破折号、冒号和分号，编译后处理段末一两个词独占行，并把最后一页排满。
```
