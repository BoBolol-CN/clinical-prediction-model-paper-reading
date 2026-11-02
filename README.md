# Clinical Prediction Model Paper Reading

一个用于精读临床预测模型论文的AI技能。按12步还原作者的研究流程，核查证据与关键方法引文，默认保存含研究流程图的中文Markdown阅读报告。

适用研究：预测模型开发、更新、外部验证及新增预测因素价值评估，涵盖回归与机器学习，以及连续、二分类、生存和竞争风险结局。

## 📚 阅读框架

1. 明确目标、文献背景与研究计划。
2. 开发新模型，还是验证／更新现有模型。
3. 结局定义、预测时间窗、竞争事件与删失。
4. 候选预测因素与测量方法。
5. 数据质量与特征工程。
6. 样本量与模型复杂度。
7. 缺失数据处理。
8. 模型拟合、筛选、调参与假设。
9. 性能评价与验证设计。
10. 最终模型选择与再校准。
11. 决策曲线与临床用途。
12. 单个预测因素的预测能力与解释。

框架改编自BMJ教程的前12步；模型公开、复现和工具可用性检查放在阅读收尾。原教程共13步。[^1]

## 📋 文件结构

```text
clinical-prediction-model-paper-reading/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   └── twelve-step-framework.md
└── README.md
```

- [SKILL.md](SKILL.md)：技能入口、执行流程与判断原则。
- [详细12步框架](references/twelve-step-framework.md)：阅读问题、报告模板及参考文献。
- [界面元数据](agents/openai.yaml)：技能显示名和默认提示语。

## 📥 安装到Codex

在Codex对话中复制并发送以下内容，让内置的Skill Installer完成安装：

```text
请使用 $skill-installer 安装以下GitHub仓库中的技能：

https://github.com/BoBolol-CN/clinical-prediction-model-paper-reading

SKILL.md 位于仓库根目录。
安装名称：clinical-prediction-model-paper-reading
```

Codex支持从其他GitHub仓库安装技能，并自动识别新安装的技能。如果安装完成后仍未显示，重启Codex再试。[^2]

## ✍️ 使用示例

安装完成后，提供论文正文、文件或链接，并在Codex中发送：

```text
$clinical-prediction-model-paper-reading

请按12步精读这篇论文，重点拆解特征处理、建模与验证，
核查关键方法引文，并总结方法学启示及适用条件。
绘制论文实际研究流程图，保存为Markdown文件并提供链接。
```

也可以只阅读某一步：

```text
$clinical-prediction-model-paper-reading

请只展开第9步，说明作者怎样区分调参、内部验证与外部验证，
并核查支持其验证方法的关键参考文献。
```

## 🎯 输出特点

默认交付一份实际保存的 `.md` 文件，包含：

- 文献信息、实际阅读范围及材料缺口。
- 全文路线概述与Mermaid研究流程图，展示本文的数据处理、建模和验证关系。
- 分层的12步拆解，重点方法详细解释，结合必要的数据用途、变量处理和性能表。
- 关键引文增加的信息、方法学启示、适用条件及待核查问题。

对话中提供可点击的文件链接和简短要点。无需每次补充“给流程图、做成md”；只读指定步骤时也默认保存该范围的笔记并给相关局部流程图。用户明确要求仅在对话回答或其他格式时，按其要求执行。

每一步分别记录作者做法、证据位置、方法学评价、可迁移条件与待核查问题。未报告、未获取和阅读者推断会明确标注。

技能不内置任何特定疾病、患者队列、预测终点或拟投稿研究的方案。详细方法依据及实际论文之间的差异，按当次材料核查。

## 🔗 参考依据

[^1]: Efthimiou O, Seo M, Chalkou K, et al. Developing clinical prediction models: a step-by-step guide. *BMJ*. 2024;386:e078276. https://doi.org/10.1136/bmj-2023-078276
[^2]: OpenAI. Build skills — Install curated skills for local use. https://learn.chatgpt.com/docs/build-skills#install-curated-skills-for-local-use
