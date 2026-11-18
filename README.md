# snow-rain

参照太原理工大学刘雪宇署名论文的论证方式、章节组织、语言表达与图表叙事，辅助起草、重构、润色和审查学术论文的 Codex Skill。

## 能做什么

- 从研究中的实际困难提炼核心问题，让贡献、机制、实验与图表相互对应。
- 规划摘要、引言、相关工作、方法、实验与结论，按体裁选择结构。
- 参考已读论文安排动机图、方法总览、定性结果、消融及效率比较。
- 给出章节篇幅、预计起始页，以及 8 页双栏、9 页双栏、10 页单栏的初始预算方案。
- 按用户偏好写满允许的正文页数，减少末页空白，清理段末一两个字或词独占一行的情况。
- 正文默认不用破折号、冒号和分号，保留公式、网址、参考文献及模板必需符号。

页数和末行必须在目标模板中编译后验证。预算方案不替代具体会议当届的官方计页规则。

## 安装

将本仓库克隆到个人 Codex 技能目录。

Windows PowerShell

```powershell
git clone https://github.com/wuhhuaguo/snow-rain.git "$env:USERPROFILE\.codex\skills\snow-rain"
```

macOS 或 Linux

```bash
git clone https://github.com/wuhhuaguo/snow-rain.git ~/.codex/skills/snow-rain
```

如果配置了自定义 `CODEX_HOME`，请安装到其 `skills/snow-rain` 目录。目标目录已经存在时先检查本地修改，不要直接覆盖。安装后在新对话中调用。

## 使用

```text
$snow-rain 根据下面的真实方法和结果，提炼核心问题并重写英文 Introduction。保留已有引用，不编造实验。
```

```text
$snow-rain 按 8 页双栏正文规划这篇论文，列出各节篇幅、起始页和图表位置。编译后清理段末短行并检查最后一页。
```

```text
$snow-rain 只润色下面这一段，保持技术内容和结论强度，正文不用破折号、冒号和分号。
```

## 文件

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 技能入口与执行规则 |
| [agents/openai.yaml](agents/openai.yaml) | 显示名称与默认调用提示 |
| [references/style-profile.md](references/style-profile.md) | 写作特征与迁移规则 |
| [references/section-playbook.md](references/section-playbook.md) | 各节写作与布局 |
| [references/figures-and-layout.md](references/figures-and-layout.md) | 常用图表与页面安排 |
| [references/page-budget.md](references/page-budget.md) | 实测章节起点、篇幅预算与末行优化 |
| [references/language-guide.md](references/language-guide.md) | 语言特色与正文标点 |
| [references/evidence-map.md](references/evidence-map.md) | 逐篇证据与适用边界 |
| [references/corpus.md](references/corpus.md) | 论文覆盖清单 |
| [references/bibliography.json](references/bibliography.json) | 结构化题录与来源 |
| [references/examples.md](references/examples.md) | 使用示例 |

## 语料覆盖

核对日期为 2026 年 11 月 18 日。公开检索清单包含 48 条论文与预印本记录，其中 44 条有主页、全文或作者单位索引支持，4 条归属仍待确认。当前规则基于 11 项工作的全文，共 12 个版本，并非已经读完作者所有论文。

语料观察、编辑建议与用户指定的排版偏好在文件中分别标明。共同署名不能证明具体段落由某一作者执笔。本项目是基于公开论文的写作规则整理，不是作者本人提供的官方工具，也不是模型微调。

仓库仅提供技能说明、题录、来源链接与原创示例，不包含论文 PDF 或原始全文。
