# Concept To Visual Card · 概念图解卡

一个 AI 技能（Skill）：把抽象的概念、理论、学习笔记、论文观点或产品机制，变成**可控的视觉知识卡**——知识卡片、寓言漫画、分镜图、类比图解、信息图、公众号封面等。

适合给 **小红书 / 朋友圈 / 公众号 / PPT** 做知识配图。

> 核心原则：**先确认，后出图。** AI 会先把「最终生图 Prompt」给你确认，你点头之后才会生成图片，避免反复抽卡。

## 它是怎么工作的

```
1. 一次性收集约束   → 场景、受众、风格、语言、比例、抽象程度、禁忌……（已说清楚的不再问）
2. 提炼概念结构     → 概念名、核心机制、去术语化解释、结构类型
3. 选择画面形式     → 知识卡 / 寓言漫画 / 分镜图 / 类比图 / 信息图 / 封面图 / PPT 概念页
4. 输出确认稿       → 概念理解 + 视觉路线 + 图中文字 + 英文生图 Prompt
5. 你确认后才出图   → 调用可用的图像生成工具
```

没有指定时的默认值：朋友圈/小红书场景、单页知识卡、中文、2:3 竖版、清爽编辑感风格、轻度比喻。

## 安装

这个仓库本身就是一个完整的技能文件夹（根目录就是 `SKILL.md`），克隆到对应 AI 工具的技能目录即可。

**Claude Code**

```bash
git clone https://github.com/xiongweijin/concept-to-visual-card ~/.claude/skills/concept-to-visual-card
```

**Codex**

```bash
git clone https://github.com/xiongweijin/concept-to-visual-card ~/.codex/skills/concept-to-visual-card
```

`agents/openai.yaml` 提供了 Codex 界面里的显示名称、简介和默认提示词。

## 怎么用

装好后直接用自然语言说，比如：

- 「把『边际效用递减』做成一张小红书知识卡」
- 「用寓言图解释一下什么是幸存者偏差，给朋友圈用」
- 「把这段论文观点做成 16:9 的 PPT 概念图，先只给我 prompt」

触发词包括：概念图、知识卡片、小红书知识图、朋友圈知识图、公众号配图、概念可视化、寓言图、分镜图、论文观点可视化、学习笔记图解、concept visual card、knowledge card 等。

## 文件结构

| 文件 | 作用 |
|---|---|
| `SKILL.md` | 技能主说明：工作流程、默认值、质量规则 |
| `references/confirmation-form.md` | 一次性确认约束的问题模板与默认值 |
| `references/concept-extraction.md` | 如何提炼概念结构 |
| `references/visual-formats.md` | 各种画面形式及适用场景 |
| `references/style-presets.md` | 风格预设 |
| `assets/prompt-template.md` | 最终生图 Prompt 模板 |
| `agents/openai.yaml` | Codex 界面配置 |

## 版本

当前版本 `0.1.0`。
