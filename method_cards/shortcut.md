# `路径捷径` 方法卡

## 方法卡：低成本替代型

```yaml
id: shortcut_low_cost_substitute
name: 低成本替代型
category: 路径捷径
definition: 强调原本高门槛、高成本的目标，其实可以通过更轻的方式达成。
trigger_condition:
  - 内容中存在高成本旧路径和低成本新路径
required_signals:
  - 存在旧路径
  - 存在成本更低的新路径
optional_signals:
  - 零基础
  - 不花钱
negative_signals:
  - 没有真正替代关系
  - 只是偷换目标
applicable_topics:
  - 创业
  - 技能
  - 表达
  - 内容生产
applicable_intents:
  - 降低行动门槛
  - 提高可执行感
target_emotions:
  - 轻松感
  - 如释重负
promise_type:
  - 用更低成本的方式达成目标
evidence_requirement: 高
title_formula:
  - "你以为要X，其实不用X也能Y"
lexicon:
  - 不花钱
  - 零基础
  - 低成本
  - 不靠X
examples:
  - 创业就该不花钱才能成功
counter_examples:
  - 省掉关键环节却还说结果一样
similar_methods_diff:
  - 与新路径发现型不同，本方法更强调成本替代
allowed_secondary_categories:
  - 权威借信
  - 认知颠覆
forbidden_secondary_categories:
  - 路径捷径
```

## 方法卡：杠杆加速型

```yaml
id: shortcut_leverage_acceleration
name: 杠杆加速型
category: 路径捷径
definition: 强调通过结构、工具或方法调整，让同样投入产出更大。
trigger_condition:
  - 内容存在明显的效率放大机制
required_signals:
  - 存在放大结构
  - 存在产出差距
optional_signals:
  - AI
  - 自动化
  - 复利结构
negative_signals:
  - 没有真正放大，只是更努力
applicable_topics:
  - AI
  - 效率
  - 赚钱
  - 学习
applicable_intents:
  - 提速
  - 放大产出
target_emotions:
  - 兴奋
  - 想超车
promise_type:
  - 用同等投入获得更大产出
evidence_requirement: 高
title_formula:
  - "普通人如何一年顶三年"
  - "用X在Y天内达到Z"
lexicon:
  - 一年顶三年
  - 杠杆
  - 加速
  - 放大
examples:
  - 普通人如何一年顶三年
  - 7天用AI装成内行
counter_examples:
  - 没有方法结构，只是喊加速
similar_methods_diff:
  - 与低成本替代型相比，本方法更强调速度与倍率
allowed_secondary_categories:
  - 权威借信
  - 焦虑损失
forbidden_secondary_categories:
  - 路径捷径
```

## 方法卡：新路径发现型

```yaml
id: shortcut_new_path
name: 新路径发现型
category: 路径捷径
definition: 强调你以为只有一条路，但其实还有另一条更优路径。
trigger_condition:
  - 内容存在旧路径认知
  - 内容能提供另一条可行路线
required_signals:
  - 存在旧路径
  - 存在替代路径
optional_signals:
  - 路线反直觉
negative_signals:
  - 没有真正的新路径
applicable_topics:
  - 职业
  - 赚钱
  - 成长
  - 决策
applicable_intents:
  - 打开选择
  - 降低路径依赖
target_emotions:
  - 新鲜感
  - 被打开
promise_type:
  - 看见另一条更优的路
evidence_requirement: 中
title_formula:
  - "不是只有X这条路，Y也能到达Z"
lexicon:
  - 不是只有
  - 换条路
  - 另一条路
examples:
  - 感情里最该守住的，不是底线，是注意力
counter_examples:
  - 只是换个说法，不是换路径
similar_methods_diff:
  - 与认知顺序重排型相比，本方法更强调路线替换，不是顺序调整
allowed_secondary_categories:
  - 权威借信
  - 认知颠覆
forbidden_secondary_categories:
  - 路径捷径
```

## 方法卡：动作拆解型

```yaml
id: shortcut_action_breakdown
name: 动作拆解型
category: 路径捷径
definition: 把目标压缩成少数几个动作，让用户产生“我现在就能做”的感觉。
trigger_condition:
  - 内容具备明确步骤
  - 标题适合强调可执行性
required_signals:
  - 明确动作
  - 目标与动作存在关系
optional_signals:
  - 数字化步骤
negative_signals:
  - 动作不具体
  - 只是清单，不构成方法
applicable_topics:
  - 教程
  - 实操
  - 技能
  - 效率
applicable_intents:
  - 强化执行
  - 降低启动成本
target_emotions:
  - 可控感
  - 立刻去做
promise_type:
  - 拿到清晰可执行动作
evidence_requirement: 中
title_formula:
  - "3步/4个动作 + 达成结果"
lexicon:
  - 3步
  - 4个动作
  - 照着做
  - 拿来就用
examples:
  - 3步判断一个创业机会能不能赚钱
counter_examples:
  - 标题说有步骤，正文没有动作
similar_methods_diff:
  - 与信息壁垒型不同，本方法卖的是执行结构，不是稀缺入口
allowed_secondary_categories:
  - 权威借信
  - 信息稀缺
forbidden_secondary_categories:
  - 路径捷径
```
