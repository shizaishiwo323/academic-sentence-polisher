# SCI Writing Expert for Codex

一个面向科研论文写作的 Codex Skill，覆盖：

- 中文科研内容翻译为自然、克制、符合 SCI 习惯的英文；
- 英文句子、段落和整节润色；
- 逻辑、衔接、时态、语态、冠词、因果关系和语气强度检查；
- Introduction、Methods、Results、Discussion/Conclusion、Abstract 和 Title 的功能结构诊断；
- 全文故事线、章节排布、证据链、前后呼应和审稿人风险审查；
- 在不改变数据、引用、公式、术语和证据强度的前提下进行修改。

本仓库由原有的 `academic-sentence-polisher` 扩展而来，保留其句子级反 AI 痕迹、过度主张、术语和破折号检查，同时增加翻译、段落、章节和全文工作流。

## 核心原则

```text
科学含义与证据
> 全文故事线
> 章节功能
> 段落逻辑
> 句子清晰度
> 语法与词汇
```

流畅不能以改变科学含义为代价。Skill 不会虚构数据、引用、机制、结果或未经支持的结论。

## 主要结构

```text
.
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── workflow_router.md
│   ├── protected_content_and_evidence.md
│   ├── target_article_adaptation.md
│   ├── zh_en_translation.md
│   ├── sentence_paragraph_revision.md
│   ├── grammar_and_cohesion.md
│   ├── claim_strength_causality_modality.md
│   ├── section_introduction.md
│   ├── section_methods.md
│   ├── section_results.md
│   ├── section_discussion_conclusion.md
│   ├── section_abstract_title.md
│   ├── manuscript_architecture_audit.md
│   ├── functional_language_bank.md
│   ├── output_contracts.md
│   └── source_notes.md
├── scripts/validate_skill.py
└── tests/eval_cases.md
```

## 安装

### 用户级

```bash
git clone https://github.com/shizaishiwo323/academic-sentence-polisher.git \
  "$HOME/.agents/skills/sci-writing-expert"
```

### 项目级

```bash
mkdir -p .agents/skills
git clone https://github.com/shizaishiwo323/academic-sentence-polisher.git \
  .agents/skills/sci-writing-expert
```

安装后可显式调用：

```text
$sci-writing-expert
```

也可以直接描述任务，由 Codex 根据 `SKILL.md` 的描述自动匹配。若安装后未出现，重启 Codex。

## 示例

### 中文翻译

```text
$sci-writing-expert
把下面中文翻译为地道的 SCI 英文。保持结论强度，不增加机制：
...
```

### 段落润色

```text
$sci-writing-expert
润色下面的 Results 段落。先判断句子顺序和结果解释是否合理，再修改英文：
...
```

### 全文结构审查

```text
$sci-writing-expert
审查这篇初稿的 Introduction、Results 和 Discussion 是否前后呼应。
先给出结构诊断和优先级，不要立即逐句改写。
```

### 摘要和标题

```text
$sci-writing-expert
把 Abstract 压缩到 200 词以内，保留关键定量结果，并给出 5 个中性、可检索的标题。
```

## 建议输入

为了获得稳定结果，可同时提供：

- 目标期刊和文章类型；
- 论文所属领域；
- 文本所在章节；
- 术语表和必须保留的表达；
- 3-5 篇目标期刊近期代表性文章；
- 修改深度：轻度润色、深度重写、结构诊断或全文审查。

## 验证

```bash
python scripts/validate_skill.py
```

GitHub Actions 也会运行同一验证，检查 frontmatter、内部引用、必需文件及是否误提交 PDF/电子书等受版权保护的源文件。

## 来源与版权

该 Skill 受到 Hilary Glasman-Deal 的 *Science Research Writing for Non-Native Speakers of English* 所总结的科学写作教学框架启发，但仓库内容为独立归纳、重新组织和改写，不包含原书 PDF、章节转录、练习答案或大段原文。

详见 [NOTICE.md](NOTICE.md) 和 `references/source_notes.md`。
