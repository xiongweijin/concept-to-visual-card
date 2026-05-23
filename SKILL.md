---
name: concept-to-visual-card
description: |
  Turn abstract concepts, theories, notes, research ideas, or product mechanisms into controlled visual knowledge cards,
  parable images, storyboard diagrams, social media knowledge graphics, or presentation concept visuals.
  Use when the user wants to make a concept easier to understand and share through an image.
  Triggers: 概念图, 知识卡片, 小红书知识图, 朋友圈知识图, 公众号配图, 概念可视化, 寓言图, 分镜图, 论文观点可视化,
  学习笔记图解, 把这个概念做成图, concept visual card, knowledge card, parable image, visual explainer.
metadata:
  version: "0.1.0"
  category: creative-workflow
  output_format: confirmed prompt first, image last
---

# Concept To Visual Card

把抽象内容通过一次性约束收集和最终确认，转成可控的视觉知识卡、寓言图、分镜图或社交媒体知识图。

## Core Rule

Do not generate the image until the user has confirmed the final image prompt, unless the user explicitly asks to skip confirmation.

## Workflow

### 1. Collect Constraints Once

If the user has not provided enough constraints, ask one consolidated question using `references/confirmation-form.md`.

Collect only what is needed:
- Concept source
- Usage scene
- Visual format
- Audience
- Style
- Language
- Aspect ratio
- Metaphor level
- Forbidden elements

If the user already provided enough constraints, do not ask again. Use reasonable defaults from `references/confirmation-form.md`.

### 2. Extract Concept Structure

Use `references/concept-extraction.md` to produce:
- Concept name
- Core mechanism
- Plain-language explanation without jargon
- Structural type

If the concept is ambiguous, stop and ask the user to clarify the concept before planning the image.

### 3. Choose Visual Format

Use `references/visual-formats.md` to select the best visual output type:
- Visual knowledge card
- Parable comic
- Storyboard
- Analogy diagram
- Infographic poster
- Public account cover
- Presentation concept slide

Match the format to the user's platform and audience.

### 4. Build Confirmation Draft

Before image generation, output:

```markdown
## 概念理解
- 概念名称：
- 核心机制：
- 去术语化解释：
- 结构类型：

## 视觉表达路线
- 输出类型：
- 使用场景：
- 受众：
- 推荐画面：
- 推荐风格：
- 推荐比例：

## 图中文字
- 标题：
- 副标题：
- 关键句：
- 模块文字：

## 最终生图 Prompt
[English prompt. Keep in-image text in the user's language.]

请确认是否按这个 prompt 生图。
```

### 5. Generate Image Last

After the user confirms, use the available image generation tool.

The image prompt must be in English. In-image text should follow the user's language.

## Defaults

Use these defaults when the user does not specify:
- Usage scene: 朋友圈 / 小红书
- Visual format: 单页知识卡 with light storyboard elements
- Audience: educated general readers
- Language: Chinese
- Aspect ratio: 2:3 vertical
- Style: clean editorial knowledge card, warm but restrained
- Text density: medium-low
- Metaphor level: light analogy, not fully fictional unless requested

## Quality Rules

1. One image should explain one core concept.
2. Complex topics should become a series, not one overcrowded card.
3. Prefer understanding and sharing value over decorative visual complexity.
4. Keep on-image text short and readable.
5. Do not invent facts from documents; summarize only what is provided or well-known.
6. If the user asks for prompt only, do not generate the image.
7. If the user asks for direct generation and has supplied enough constraints, skip extra questions but still show the final prompt unless they asked to skip confirmation.
