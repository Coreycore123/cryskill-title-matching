---
name: cryskill-title-matching
description: CoreySkill title matching system. Match content to the most suitable title mechanism, retrieve high-performing title templates, and generate or optimize titles under a 21-character limit. Use for topic-to-title, content-to-title, title optimization, and reference-title analysis.
version: 0.1.0
---

# 标题匹配 Skill

## 目标

根据一条内容的主题、观点、用户对象和可用证据，匹配最合适的标题方法，并输出多条不同强度的候选标题。

本 Skill 的核心任务不是“润色标题”，而是：

1. 判断这条内容最适合激活哪一种点击驱动力
2. 选择最合适的标题方法
3. 输出结构化匹配结果
4. 生成可用标题候选

---

## 适用场景

使用本 Skill 的典型场景包括：

- 需要为一条内容匹配标题方法
- 需要判断一个现有标题属于哪种方法
- 需要基于内容生成 3 条不同强度标题
- 需要复盘某条高数据标题为什么有效
- 需要在相邻方法之间做边界判断

---

## 使用模式

本 Skill 默认支持 4 种调用模式：

```yaml
use_mode:
  - topic_to_title
  - content_to_title
  - optimize_existing_title
  - analyze_reference_title
```

### 1. `topic_to_title`

适用输入：

- 行业话题
- 趋势判断
- 命题方向
- 一句话观点

任务目标：

- 先把抽象话题压缩成清晰命题
- 再匹配标题方法
- 再匹配 reference template
- 最后输出可用标题

注意：

- 该模式输入通常更抽象
- 更依赖模板匹配，不宜过度自由生成

### 2. `content_to_title`

适用输入：

- 正文
- 文章
- 口播稿
- 观点展开内容

任务目标：

- 提炼内容核心承诺
- 提炼目标用户和主冲突
- 匹配主类和主方法
- 输出标题候选

注意：

- 这是最稳定的模式
- 因为输入信息最完整，匹配精度最高

### 3. `optimize_existing_title`

适用输入：

- 已有标题
- 初稿标题
- 想优化但不想完全重写的标题

任务目标：

- 先判断现标题命中了什么方法
- 再判断问题出在哪
- 再基于相近模板做压缩、增强或改写

注意：

- 不默认推翻原标题
- 优先做结构优化，而不是重写一切

### 4. `analyze_reference_title`

适用输入：

- 高数据标题
- reference 样本
- 需要归因分析的标题

任务目标：

- 做方法归类
- 拆主驱动力
- 判断为什么有效
- 必要时补入 `references/` 或模板库

注意：

- 该模式偏分析和入库，不以立刻生成新标题为首要目标

---

## 输入

优先输入以下信息：

- 内容主题
- 内容摘要
- 目标用户
- 核心观点
- 核心承诺
- 可用证据
- 若已存在：原始标题、封面标题、开头文案

如果输入不完整，也可以先运行，但必须在输出中标记信息不足项。

---

## 输出

标准输出应遵循：

- [output_schema.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/output_schema.md)

最少应包含：

- `primary_category`
- `primary_method`
- `secondary_category`
- `secondary_role`
- `confidence`
- `matched_signals`
- `rejected_candidates`
- `reasoning`
- `title_directions`

---

## 工作流

每次调用按以下顺序执行：

1. 读取 [rules.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/rules.md)
目的：
确定一级分类树、二级分类树、主辅分类规则、边界规则、禁用规则。

2. 读取相关方法卡
位置：
- [method_cards](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/method_cards)

目的：
根据候选一级类，定位对应二级方法，并检查：
- `trigger_condition`
- `required_signals`
- `negative_signals`
- `similar_methods_diff`

3. 如需校准表达强度或边界，读取 reference
位置：
- [strong_titles.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/strong_titles.md)
- [boundary_cases.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/boundary_cases.md)

用途：
- `strong_titles.md` 用于校准“强标题长什么样”
- `boundary_cases.md` 用于处理容易误判的相邻方法

4. 输出结构化判断结果
要求：
- 先分类，再生成
- 保留命中信号和排除理由

5. 生成标题候选
要求：
- 默认输出 `strong / balanced / soft` 三档
- 标题必须和主方法一致
- 辅类只能增强，不能改写主承诺

---

## 模式分流

4 种使用模式的前置处理不同，但中段判断系统一致。

### `topic_to_title`

流程：

1. 抽取核心命题
2. 判断主类和主方法
3. 匹配 reference template
4. 输出标题

### `content_to_title`

流程：

1. 提炼核心承诺
2. 提炼用户对象和主冲突
3. 判断主类和主方法
4. 匹配 reference template
5. 输出标题

### `optimize_existing_title`

流程：

1. 判断原题当前命中的方法
2. 判断原题弱点
3. 匹配更优模板
4. 输出优化版标题

### `analyze_reference_title`

流程：

1. 归类
2. 拆解 why it works
3. 判断是否属于边界案例
4. 需要时补入 `references/`

---

## 共用中段

无论使用哪种模式，中段都统一调用：

- [rules.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/rules.md)
- [method_cards](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/method_cards)
- [boundary_cases.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/boundary_cases.md)
- [reference_templates.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/reference_templates.md)

---

## 核心原则

### 1. 先判心理驱动，再选句式

不要从表面词汇、语气和句子结构直接反推方法。

### 2. 主类只选一个

每条内容只允许：

- `1个主一级类`
- `1个主二级方法`

辅类最多一个，而且必须是增强角色。

### 3. 宁可单一清晰，不要混合过度

如果两个方法同时成立，优先选择点击第一驱动力最强的那个。

### 4. 不为了冲击牺牲可信度

如果证据不足，不要硬上：

- 假信息差
- 假反常识
- 假权威

### 5. 标题长度必须过检

所有最终候选标题都必须满足：

- 包括标点在内不超过21个字

超出后必须压缩，不允许直接保留超长版本。

### 6. 输出必须可复盘

每次匹配都要能回答：

- 为什么是这个方法
- 为什么不是另一个相邻方法
- 这个标题方向的风险是什么

---

## 失败策略

如果出现以下任一情况，不要强行生成高冲击标题：

- 内容主题不清
- 核心承诺不清
- 用户对象不清
- 证据不足
- 多个候选类竞争过强

应改为：

1. 输出失败态或低置信度结果
2. 标记缺失信息
3. 降级为 `balanced` 或 `soft`

---

## 调用建议

### 当用户给的是“内容”

优先做：

- 方法匹配
- 输出结构化判断
- 生成标题

### 当用户给的是“已有标题”

优先做：

- 标题归类
- 分析命中机制
- 判断是否属于强样本

### 当用户给的是“高数据 reference”

优先做：

- 标注主类和主方法
- 记录边界说明
- 如有必要补入 `references/`

### 当用户只给“行业话题”

优先做：

- 抽取命题
- 匹配模板
- 输出更像标题而不是像结论的话术

---

## 文件分工

本 Skill 的文件分工如下：

- [rules.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/rules.md)
负责系统级分类规则、主辅规则、边界规则、禁用规则。

- [method_cards](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/method_cards)
负责提供每种标题方法的定义、信号、触发条件和差异说明。

- [strong_titles.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/strong_titles.md)
负责校准强样本。

- [boundary_cases.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/boundary_cases.md)
负责处理相邻类误判。

- [output_schema.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/output_schema.md)
负责定义最终输出格式。

---

## 默认执行模板

如果没有额外说明，默认按这个顺序输出：

1. 内容简述
2. 主类判断
3. 主方法判断
4. 辅类判断
5. 命中信号
6. 排除的相邻方法
7. 3 条标题候选
8. 最终推荐及风险提示

---

## 一句话定义

这个 Skill 不负责“写一个好听的标题”。

它负责的是：

`判断一条内容为什么值得被点开，并把这种点击驱动力翻译成可复用的标题方法。`
