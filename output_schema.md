# `output_schema.md`

本文件定义标题匹配系统的标准输出格式。

目标不是生成“解释性散文”，而是输出：

- 可复用
- 可校验
- 可回溯
- 可继续生成标题

的结构化结果。

---

## 1. 输出原则

### 1.1 先判断，再生成

输出必须先完成分类判断，再给出标题方向。

禁止直接跳到标题生成，不经过主类、主方法、信号命中说明。

### 1.2 输出必须能解释“为什么是这个方法”

每次输出都必须保留：

- 命中了什么信号
- 为什么选这个主类
- 为什么没选相邻类

否则无法用于后续优化规则。

### 1.3 输出必须区分“判断结果”和“创作结果”

判断结果解决：

- 这条内容属于什么方法
- 为什么属于它

创作结果解决：

- 应该生成什么标题
- 不同强度下怎么写

两者不能混在一个字段里。

### 1.4 输出要兼容 AI 和人工复盘

字段既要足够结构化，便于后续程序调用，也要足够可读，便于人工检查误判。

---

## 2. 标准输出结构

每条内容的标准输出建议为：

```yaml
input_snapshot:
  topic:
  content_summary:
  target_audience:
  core_promise:
  available_evidence:

classification:
  primary_category:
  primary_method:
  secondary_category:
  secondary_role:
  confidence:

signal_analysis:
  matched_signals:
  optional_signals_used:
  negative_signals_checked:
  evidence_dependency:
  evidence_status:

reasoning:
  primary_reason:
  secondary_reason:
  rejected_candidates:
  boundary_notes:

generation_strategy:
  title_strength:
  abstraction_level:
  core_tension:
  promise_focus:
  audience_lock:
  wording_constraints:

template_matching:
  best_template:
  template_family:
  rewrite_reason:
  slot_mapping:
  backup_templates:

title_directions:
  - strength:
    formula:
    draft_title:
    length_count:
    length_pass:
    why_this_direction:

quality_control:
  risk_flags:
  anti_pattern_checks:
  final_recommendation:
```

---

## 3. 字段定义

## 3.1 `input_snapshot`

作用：保留本次匹配所依据的输入快照，防止后续只看到结果，看不到原始上下文。

字段：

- `topic`
  内容主题或领域。
  例：`情感关系`、`女性成长`、`职场`

- `content_summary`
  对正文核心观点的压缩表达。
  不是全文摘要，而是“这条内容到底在说什么”。

- `target_audience`
  目标用户。
  例：`普通女性`、`25+打工人`、`关系中高敏感用户`

- `core_promise`
  内容最终承诺给用户的核心收益。
  例：`看清关系中的注意力机制`

- `available_evidence`
  内容当前可支撑标题的证据。
  例：`个人经历`、`权威来源`、`案例`、`观察结论`

---

## 3.2 `classification`

作用：输出最终分类结果。

字段：

- `primary_category`
  一级主类。
  必填。

- `primary_method`
  二级主方法。
  必填。

- `secondary_category`
  一级辅类。
  可为空。

- `secondary_role`
  辅类承担的作用。
  必须来自 `rules.md` 中允许的角色集合：
  - `credibility`
  - `audience_lock`
  - `urgency`
  - `curiosity`
  - `efficiency`
  - `emotional_relief`
  - `tension`

- `confidence`
  本次分类置信度。
  建议区间：`0.00 - 1.00`

建议解释：
- `0.85+`：边界清晰，匹配稳定
- `0.70-0.84`：基本稳定，但存在相邻类竞争
- `0.50-0.69`：可用，但需要人工复核
- `<0.50`：不建议自动强生成

---

## 3.3 `signal_analysis`

作用：记录这次匹配到底命中了哪些信号。

字段：

- `matched_signals`
  明确命中的主信号。
  必填。

- `optional_signals_used`
  使用了哪些非必要信号增强判断。

- `negative_signals_checked`
  检查了哪些禁用信号，以及是否被排除。

- `evidence_dependency`
  当前方法对证据的依赖强度。
  建议枚举：
  - `高`
  - `中`
  - `低`

- `evidence_status`
  当前输入是否真的满足该证据要求。
  建议枚举：
  - `充足`
  - `一般`
  - `不足`

---

## 3.4 `reasoning`

作用：保留分类判断理由，支持后续复盘。

字段：

- `primary_reason`
  为什么这个主类最成立。

- `secondary_reason`
  为什么辅类成立。
  若无辅类，可为空。

- `rejected_candidates`
  被排除的相邻候选类。
  建议格式：

```yaml
rejected_candidates:
  - category:
    method:
    reject_reason:
```

- `boundary_notes`
  该样本最容易被误判的点。

---

## 3.5 `generation_strategy`

作用：把分类结果转译成生成标题时的约束条件。

字段：

- `title_strength`
  本次推荐的标题强度。
  建议枚举：
  - `strong`
  - `balanced`
  - `soft`

- `abstraction_level`
  标题表达抽象程度。
  建议枚举：
  - `high`
  - `medium`
  - `low`

说明：
- `high`：更像判断句、哲学句、抽象观点
- `medium`：有观点，也有一定场景
- `low`：更具体、更生活化、更动作化

- `core_tension`
  这条标题最核心的冲突轴。
  例：
  - `主流判断 vs 新判断`
  - `低成本路径 vs 传统高成本路径`
  - `表面现象 vs 真实规则`
  - `自我归因 vs 结构归因`

- `promise_focus`
  这条标题主要在承诺什么。
  例：
  - `重新看清`
  - `少走弯路`
  - `获得资格`
  - `修复自我解释`

- `audience_lock`
  是否需要显式点名某类用户。
  建议枚举：
  - `explicit`
  - `implicit`
  - `none`

- `wording_constraints`
  语言层约束。
  例：
  - `避免过度攻击用户`
  - `不要使用虚假权威词`
  - `避免悬浮鸡汤`
  - `避免同时使用两个主判断句`
  - `标题总长度不得超过21字`

---

## 3.6 `template_matching`

作用：把分类结果进一步连接到可仿写的参考母版，降低自由生成不确定性。

字段：

- `best_template`
  最推荐调用的模板 ID。
  应来自：
  - [reference_templates.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/reference_templates.md)

- `template_family`
  所属模板家族。
  例：
  - `判断重写型`
  - `预设反转型`
  - `归因重击型`
  - `缺失知识补位型`

- `rewrite_reason`
  为什么这个模板最适合当前内容。
  应说明：
  - 它与 `primary_method` 的对应关系
  - 它比相邻模板更合适的原因

- `slot_mapping`
  当前内容如何映射进模板槽位。
  建议格式：

```yaml
slot_mapping:
  A: 用户默认理解
  B: 新判断
```

- `backup_templates`
  备选模板。
  建议保留 1-3 个。

建议格式：

```yaml
backup_templates:
  - template_id:
    reason:
```

使用原则：

- 优先先找模板，再改写
- 模板匹配失败时，才允许更自由生成
- 若无高相似模板，应在 `quality_control` 中标记风险

---

## 3.7 `title_directions`

作用：真正给生成模块使用的标题输出区。

建议每次至少输出 3 个方向：

- `strong`
- `balanced`
- `soft`

字段：

- `strength`
  当前方向强度。

- `formula`
  本方向使用的标题构型。
  例：
  - `不是A，是B`
  - `某类人 + 真正问题`
  - `X之后，才知道Y`

- `draft_title`
  当前方向下的候选标题。

- `length_count`
  当前标题总字数，包含标点。

- `length_pass`
  当前标题是否通过长度约束。
  建议枚举：
  - `pass`
  - `fail`

- `why_this_direction`
  为什么这样写，和主方法有什么对应关系。

---

## 3.8 `quality_control`

作用：在输出标题前做最后一轮自检。

字段：

- `risk_flags`
  本条标题可能存在的风险。
  例：
  - `证据不足`
  - `过度抽象`
  - `冒犯用户`
  - `像标题党`
  - `主辅策略打架`

- `anti_pattern_checks`
  对照 `anti_patterns.md` 的检查结果。
  建议格式：

```yaml
anti_pattern_checks:
  fake_scarcity: pass
  fake_contrarian: pass
  forced_authority: fail
  empty_emotion: pass
```

- `final_recommendation`
  最终建议采用哪一条标题方向，为什么。

---

## 4. 最小可用输出

如果场景需要极简输出，最小可用版本为：

```yaml
primary_category:
primary_method:
secondary_category:
secondary_role:
confidence:
matched_signals:
rejected_candidates:
reasoning:
best_template:
slot_mapping:
title_directions:
```

适用场景：

- 快速人工试跑
- 小规模调试
- 临时调用 skill

不适用场景：

- 大规模批量标注
- 后续做模型评估
- 要做误判分析的调用

---

## 5. 失败输出格式

当输入信息不足，或多个候选类竞争过强时，必须允许系统输出失败态。

建议格式：

```yaml
status: insufficient_information
missing_fields:
  - target_audience
  - core_promise
  - evidence
uncertain_candidates:
  - category:
    method:
reason:
next_best_action:
```

字段说明：

- `status`
  当前不能稳定匹配。

- `missing_fields`
  缺了哪些关键输入。

- `uncertain_candidates`
  当前最接近但无法稳定确认的候选。

- `reason`
  为什么不能稳定判断。

- `next_best_action`
  下一步应该补什么信息，或降级到什么强度。

---

## 6. 推荐枚举值

为了减少输出漂移，建议部分字段使用固定枚举值。

### 6.1 `title_strength`

- `strong`
- `balanced`
- `soft`

### 6.2 `abstraction_level`

- `high`
- `medium`
- `low`

### 6.3 `evidence_dependency`

- `高`
- `中`
- `低`

### 6.4 `evidence_status`

- `充足`
- `一般`
- `不足`

### 6.5 `audience_lock`

- `explicit`
- `implicit`
- `none`

---

## 7. 推荐输出示例

```yaml
input_snapshot:
  topic: 情感关系
  content_summary: 感情中真正该守住的不是形式上的底线，而是自己的注意力分配
  target_audience: 关系中容易过度投入的人
  core_promise: 重排感情中的关注重点
  available_evidence:
    - 关系观察
    - 认知判断

classification:
  primary_category: 认知颠覆
  primary_method: 价值观反转型
  secondary_category: 路径捷径
  secondary_role: efficiency
  confidence: 0.77

signal_analysis:
  matched_signals:
    - 感情中的重要性排序被重排
    - 默认答案被替换为反直觉答案
  optional_signals_used:
    - 注意力作为可操作抓手
  negative_signals_checked:
    - 无明确人群点名，不判身份归属主类
    - 无明显处境安顿，不判解释重构主类
  evidence_dependency: 中
  evidence_status: 一般

reasoning:
  primary_reason: 标题核心点击力来自对感情重要性判断的反转
  secondary_reason: 注意力可被理解为更省力、更有效的关系抓手
  rejected_candidates:
    - category: 解释重构
      method: 负面信号重定义型
      reject_reason: 标题不是重写痛苦意义，而是在重排价值优先级
    - category: 身份归属
      method: 关系角色型
      reject_reason: 标题没有点名某类特定人群
  boundary_notes:
    - 容易被误判为解释重构，因为“注意力”有安顿感

generation_strategy:
  title_strength: balanced
  abstraction_level: medium
  core_tension: 主流关系重点 vs 真正该守住的东西
  promise_focus: 重新看清
  audience_lock: implicit
  wording_constraints:
    - 不要过度哲学化
    - 不要引入额外权威
    - 标题总长度不得超过21字

template_matching:
  best_template: tpl_not_a_b
  template_family: 判断重写型
  rewrite_reason: 当前内容核心是替换默认答案，且“底线/注意力”之间存在清晰对撞，最适合用“不是A，是B”模板显化反转
  slot_mapping:
    A: 底线
    B: 注意力
  backup_templates:
    - template_id: tpl_x_is_not_a_b
      reason: 也可做概念重定义，但冲击力略弱
    - template_id: tpl_you_think_a_b
      reason: 可用来做更解释型版本

title_directions:
  - strength: strong
    formula: 不是A，是B
    draft_title: 感情中最该守住的，不是底线，是注意力
    length_count: 18
    length_pass: pass
    why_this_direction: 显化默认答案，增强反转冲击
  - strength: balanced
    formula: 场景 + 真正重点
    draft_title: 感情中最该守住的，是注意力
    length_count: 13
    length_pass: pass
    why_this_direction: 保留观点锋利度，同时不过度拉高冲突
  - strength: soft
    formula: 比起A，更该B
    draft_title: 比起输赢和对错，感情里更该守住的是注意力
    length_count: 21
    length_pass: pass
    why_this_direction: 降低攻击性，提高可接受度

quality_control:
  risk_flags:
    - 稍微抽象，正文需要尽快落到场景
  anti_pattern_checks:
    fake_scarcity: pass
    fake_contrarian: pass
    forced_authority: pass
    empty_emotion: pass
  final_recommendation: balanced，因其兼顾锋利度与可展开性
```

---

## 8. 与其他文件的关系

本文件负责：

- 定义最终输出长什么样
- 规定哪些字段必须保留
- 规定模板匹配结果如何输出
- 规定失败态怎么输出
- 规定标题长度检查如何输出

本文件不负责：

- 定义分类树
- 定义方法卡内容
- 决定某个标题属于哪一类

这些内容分别由以下文件负责：

- 分类规则：`rules.md`
- 方法定义：`method_cards/`
- 强样本校准：`references/strong_titles.md`
- 边界误判校准：`references/boundary_cases.md`
- 模板母版：`references/reference_templates.md`
