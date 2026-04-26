# `焦虑损失` 方法卡

## 方法卡：错失机会型

```yaml
id: anxiety_missed_window
name: 错失机会型
category: 焦虑损失
definition: 强调机会窗口有限，不抓住就会错过，从时间压力驱动点击。
trigger_condition:
  - 内容与窗口期、红利期、切换期直接相关
required_signals:
  - 存在时间窗口
  - 存在错过后果
optional_signals:
  - 新平台
  - 新技术
negative_signals:
  - 机会并无时效性
  - 只是制造紧迫感，没有实际窗口
applicable_topics:
  - 创业
  - 平台红利
  - AI
  - 行业变化
applicable_intents:
  - 催动决策
  - 促进行动
target_emotions:
  - 怕错过
  - 急迫
promise_type:
  - 识别应及时把握的机会
evidence_requirement: 高
title_formula:
  - "现在不做X，后面会更难"
lexicon:
  - 窗口期
  - 红利期
  - 最后机会
examples:
  - AI时代最容易被低估的窗口期
counter_examples:
  - 一切事情都要马上做
similar_methods_diff:
  - 与机会金矿型不同，本方法主卖点是时效焦虑，不是机会稀缺
allowed_secondary_categories:
  - 路径捷径
  - 信息稀缺
forbidden_secondary_categories:
  - 焦虑损失
```

## 方法卡：掉队淘汰型

```yaml
id: anxiety_fall_behind
name: 掉队淘汰型
category: 焦虑损失
definition: 强调若继续维持现状，会被环境、同龄人或系统甩开。
trigger_condition:
  - 内容与竞争、变化、适应能力相关
required_signals:
  - 存在对照群体或环境变化
  - 存在掉队后果
optional_signals:
  - 技术变迁
  - 代际差异
negative_signals:
  - 只是空喊淘汰，没有实际机制
applicable_topics:
  - 职场
  - 学习
  - AI
  - 商业变化
applicable_intents:
  - 提醒用户升级
  - 强化危机意识
target_emotions:
  - 危机
  - 紧张
promise_type:
  - 避免被变化甩开
evidence_requirement: 高
title_formula:
  - "再这样X，你会在Y上掉队"
lexicon:
  - 被淘汰
  - 掉队
  - 跟不上
examples:
  - 不会用AI的人，正在以更慢的方式掉队
counter_examples:
  - 不学这个你的人生就完了
similar_methods_diff:
  - 与错失机会型相比，本方法更偏相对竞争，而非窗口期
allowed_secondary_categories:
  - 路径捷径
  - 身份归属
forbidden_secondary_categories:
  - 焦虑损失
```

## 方法卡：选择代价型

```yaml
id: anxiety_choice_cost
name: 选择代价型
category: 焦虑损失
definition: 强调某个错误选择的长期成本，用“选错”驱动点击。
trigger_condition:
  - 内容与重大选择相关
  - 错误选择的代价可被具体化
required_signals:
  - 存在明确选择点
  - 存在代价
optional_signals:
  - 年龄阶段
  - 复利后果
negative_signals:
  - 选择并不关键
  - 代价描述过于夸张
applicable_topics:
  - 工作
  - 婚恋
  - 城市
  - 行业
applicable_intents:
  - 帮助判断
  - 放大决策权重
target_emotions:
  - 后怕
  - 谨慎
promise_type:
  - 看清某个选择背后的真实成本
evidence_requirement: 中
title_formula:
  - "最怕的不是X，是选错Y"
lexicon:
  - 选错
  - 代价
  - 浪费几年
examples:
  - 普通家庭的孩子，最怕选错第一份工作
counter_examples:
  - 任何选择都一样严重
similar_methods_diff:
  - 与阶层创伤型相邻，但本方法主卖点是代价，不是被看见
allowed_secondary_categories:
  - 身份归属
  - 解释重构
forbidden_secondary_categories:
  - 焦虑损失
```

## 方法卡：长期吃亏型

```yaml
id: anxiety_long_term_loss
name: 长期吃亏型
category: 焦虑损失
definition: 强调某种习惯、认知或做法会持续带来隐性损失。
trigger_condition:
  - 内容涉及长期行为模式
  - 损失并非一次性，而是慢性累积
required_signals:
  - 存在长期模式
  - 存在隐性损耗
optional_signals:
  - 低感知损失
negative_signals:
  - 损失只是短期情绪
applicable_topics:
  - 职场
  - 成长
  - 财富
  - 关系
applicable_intents:
  - 提醒慢性问题
  - 促使调整长期策略
target_emotions:
  - 警醒
  - 不安
promise_type:
  - 看见长期隐损
evidence_requirement: 中
title_formula:
  - "最吃亏的不是A，是你长期在B"
lexicon:
  - 一直吃亏
  - 隐性损耗
  - 慢性损失
examples:
  - 一直靠熬解决问题的人，后劲都不会太好
counter_examples:
  - 什么都说成长期问题
similar_methods_diff:
  - 与解释重构不同，本方法重点不是重新安顿情绪，而是提醒损失
allowed_secondary_categories:
  - 解释重构
  - 路径捷径
forbidden_secondary_categories:
  - 焦虑损失
```
