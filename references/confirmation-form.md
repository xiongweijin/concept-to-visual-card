# Confirmation Form

Use this as a single consolidated question when the user has not provided enough constraints.

## Minimal Question

```markdown
我需要一次性确认这些约束，然后给你最终 prompt：

1. 概念来源：概念名 / 一段文字 / 截图 / 论文观点 / 学习笔记？
2. 使用场景：朋友圈 / 小红书 / 公众号 / PPT / 论文汇报 / 纯学习？
3. 输出类型：知识卡 / 寓言漫画 / 分镜图 / 类比图解 / 信息图 / 封面图？
4. 受众：普通读者 / 学生 / 专业人士 / 同事 / 投资人 / 自己复习？
5. 风格偏好：素描 / 水墨 / 扁平 / 复古漫画 / 赛博科技 / 极简信息图？
6. 语言：中文 / 英文 / 中英双语？
7. 比例：竖版 2:3 / 横版 16:9 / 正方形 1:1？
8. 抽象程度：直白解释 / 轻度比喻 / 完全寓言化 / 强故事化？
9. 禁忌：不要出现哪些元素、风格或表达？
```

## Defaults

If the user gives partial constraints, fill missing fields with:

| Field | Default |
|---|---|
| 使用场景 | 朋友圈 / 小红书 |
| 输出类型 | 单页知识卡 |
| 受众 | 有一定知识兴趣的普通读者 |
| 风格 | 清爽编辑感知识卡 |
| 语言 | 中文 |
| 比例 | 2:3 竖版 |
| 抽象程度 | 轻度比喻 |
| 禁忌 | 不幼稚、不堆字、不炫技 |

## When To Ask Again

Ask again only when:
- The core concept is unclear.
- The requested output has mutually conflicting constraints.
- The user asks for a sensitive or factual claim that needs source confirmation.
