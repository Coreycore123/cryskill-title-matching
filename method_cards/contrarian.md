# `认知颠覆` 方法卡

## 方法卡：价值观反转型

```yaml
id: contrarian_value_reversal
name: 价值观反转型
category: 认知颠覆
definition: 挑战被主流赞美、默认正确或具有道德光环的判断，制造不安与松绑感。
trigger_condition:
  - 内容中存在一个被默认正确的价值观
  - 作者能给出一个反直觉但成立的新判断
required_signals:
  - 存在主流价值判断
  - 存在明确反转结论
  - 反转后仍有可解释性
optional_signals:
  - 更低成本的新路径
  - 给用户心理许可
negative_signals:
  - 只有态度，没有理由
  - 纯挑衅，没有成立基础
  - 反转后无法展开正文
applicable_topics:
  - 女性成长
  - 人生选择
  - 关系
  - 成长认知
applicable_intents:
  - 松绑
  - 改变判断标准
  - 打破自我规训
target_emotions:
  - 意外
  - 不安
  - 被解放
promise_type:
  - 推翻一个以为正确的判断
evidence_requirement: 中
title_formula:
  - "被赞美的X + 反而/其实/不能 + Y"
  - "一定要做看起来不对的事，才会得到X"
lexicon:
  - 不能以X为荣
  - 学会合理X
  - 一定要做X
  - X反而Y
examples:
  - 一定要做看起来low的事，才会成功
  - 女生要先探索人生，而不是只过日子
  - 顶着一张累脸是挣不到钱的
counter_examples:
  - 努力很重要，大家都要努力
similar_methods_diff:
  - 与常识纠偏型不同，本方法挑战的是价值判断，不是知识错误
  - 与自我许可型相邻，但本方法主卖点是反转，不是安抚
allowed_secondary_categories:
  - 解释重构
  - 身份归属
forbidden_secondary_categories:
  - 认知颠覆
```

## 方法卡：因果质疑型

```yaml
id: contrarian_causal_challenge
name: 因果质疑型
category: 认知颠覆
definition: 质疑用户默认成立的因果关系、成功逻辑或公平假设，制造归因危机。
trigger_condition:
  - 内容中存在普遍默认的因果判断
  - 作者能指出该因果关系不成立或方向相反
required_signals:
  - 存在默认因果
  - 存在反结论
  - 存在可解释原因
optional_signals:
  - 公平假设
  - 身份落差
  - 结果反差
negative_signals:
  - 只是吐槽现实，不是质疑因果
  - 没有反证或解释
applicable_topics:
  - 职场
  - 赚钱
  - 情感
  - 成长
applicable_intents:
  - 重新归因
  - 反思努力方向
  - 打破默认认知
target_emotions:
  - 错愕
  - 危机感
  - 警醒
promise_type:
  - 重新理解结果为什么会发生
evidence_requirement: 中
title_formula:
  - "你以为A会带来B，但现实恰好相反"
  - "为什么A的人，反而更难得到B"
lexicon:
  - 反而
  - 越...越...
  - 为什么不如你的人
  - 真的是因为A吗
examples:
  - 情商越高，越无法向上社交
  - 为什么不如你的人，升职比你快？
counter_examples:
  - 多提升情商一定会更好
similar_methods_diff:
  - 与价值观反转型不同，本方法主打的是因果关系挑战
  - 与隐藏规则型不同，本方法更强调“你理解错因果”，不一定揭示系统规则
allowed_secondary_categories:
  - 身份归属
  - 解释重构
forbidden_secondary_categories:
  - 认知颠覆
```

## 方法卡：常识纠偏型

```yaml
id: contrarian_common_sense_fix
name: 常识纠偏型
category: 认知颠覆
definition: 纠正用户常见理解错误，重点不是挑衅，而是校正认知方向。
trigger_condition:
  - 内容里存在高频误解
  - 作者能给出更准确的解释
required_signals:
  - 存在常见误区
  - 存在更正版本
optional_signals:
  - 场景化例子
  - 低冒犯表达
negative_signals:
  - 观点不够明确
  - 更正内容依旧抽象
applicable_topics:
  - 方法论
  - 学习
  - 决策
  - 认知提升
applicable_intents:
  - 纠偏
  - 降低误判
  - 提高理解准确度
target_emotions:
  - 清醒感
  - 被纠正
promise_type:
  - 搞明白真正的问题在哪里
evidence_requirement: 中
title_formula:
  - "你不是不会X，你是搞错了Y"
  - "真正的问题不在A，在B"
lexicon:
  - 你不是
  - 真正的问题
  - 搞错了
  - 误区
examples:
  - 你不是不会表达，你是没有先讲利益
counter_examples:
  - 我来说一个大家都懂的概念
similar_methods_diff:
  - 与价值观反转型相比，本方法冲击性更低，纠偏性更强
allowed_secondary_categories:
  - 路径捷径
  - 权威借信
forbidden_secondary_categories:
  - 认知颠覆
```

## 方法卡：认知顺序重排型

```yaml
id: contrarian_sequence_reorder
name: 认知顺序重排型
category: 认知颠覆
definition: 不是说认知内容错，而是说理解顺序错了，强调先后关系决定结果。
trigger_condition:
  - 内容里存在先后次序差异
  - 先后顺序变化会明显改变结果
required_signals:
  - 存在顺序问题
  - 存在更优顺序
optional_signals:
  - 人生阶段
  - 经验迟得感
negative_signals:
  - 只是普通建议，没有顺序性
applicable_topics:
  - 赚钱
  - 成长
  - 决策
  - 人生阶段
applicable_intents:
  - 避免走弯路
  - 提前知道关键顺序
target_emotions:
  - 后知后觉
  - 惋惜
  - 想补课
promise_type:
  - 提前知道本应更早知道的顺序
evidence_requirement: 中
title_formula:
  - "做到X之后，才知道Y"
  - "不是你不知道，是你知道得太晚"
lexicon:
  - 之后才知道
  - 先...再...
  - 知道得太晚
examples:
  - 赚到一百万之后，才知道为什么赚不到
  - 35岁还是小孩，当然可以改变人生
counter_examples:
  - 我来按顺序讲一下流程
similar_methods_diff:
  - 与路径捷径不同，本方法主要卖认知顺序，不一定给具体动作
allowed_secondary_categories:
  - 路径捷径
  - 解释重构
forbidden_secondary_categories:
  - 认知颠覆
```
