# `解释重构` 方法卡

## 方法卡：负面信号重定义型

```yaml
id: reframing_negative_signal
name: 负面信号重定义型
category: 解释重构
definition: 将用户正在经历的负面信号重新解释为有价值、可利用或具有积极指向的信号。
trigger_condition:
  - 内容中存在用户会痛的处境
  - 作者能够给出成立的新解释
required_signals:
  - 明确负面信号
  - 明确新定义
optional_signals:
  - 成功前兆
  - 价值反转
negative_signals:
  - 只是安慰，没有解释结构
  - 将严重伤害轻飘飘正向化
applicable_topics:
  - 成长
  - 女性成长
  - 关系
  - 低谷
applicable_intents:
  - 安顿情绪
  - 重建意义
target_emotions:
  - 被安放
  - 释然
  - 重新有劲
promise_type:
  - 换一种方式理解眼前的不舒服
evidence_requirement: 中
title_formula:
  - "你讨厌的A，可能正说明B"
lexicon:
  - 前兆
  - 先兆
  - 说明
  - 恰恰代表
examples:
  - 女生成功之前有一个先兆：有人看你不顺眼
  - 只要有人说low的事，我跪着研究
counter_examples:
  - 被伤害就是老天给你的礼物
similar_methods_diff:
  - 与价值观反转型不同，本方法不是挑战公共道德，而是重写个人处境意义
allowed_secondary_categories:
  - 身份归属
  - 认知颠覆
forbidden_secondary_categories:
  - 解释重构
```

## 方法卡：痛苦意义重写型

```yaml
id: reframing_pain_rewrite
name: 痛苦意义重写型
category: 解释重构
definition: 不否认痛苦本身，而是重新赋予它在成长、选择或关系中的意义。
trigger_condition:
  - 内容围绕低谷、失落、受挫或长期痛苦
  - 作者能给出痛苦的新用途或新价值
required_signals:
  - 存在痛苦经历
  - 存在意义重写
optional_signals:
  - 人生阶段
negative_signals:
  - 只灌鸡汤
  - 强行美化真实伤害
applicable_topics:
  - 低谷
  - 失恋
  - 失业
  - 转型
applicable_intents:
  - 修复
  - 重新理解过往
target_emotions:
  - 被安抚
  - 被理解
promise_type:
  - 让痛苦不只是白受
evidence_requirement: 中
title_formula:
  - "你以为这段经历只带来了伤害，其实还给了你X"
lexicon:
  - 这段经历真正给你的
  - 不只是伤害
examples:
  - 那些最难熬的阶段，真正逼你长出来的是判断力
counter_examples:
  - 你所有痛苦都是好事
similar_methods_diff:
  - 与负面信号重定义型相比，本方法更偏长期意义，而非即时信号
allowed_secondary_categories:
  - 身份归属
  - 权威借信
forbidden_secondary_categories:
  - 解释重构
```

## 方法卡：困境归因重构型

```yaml
id: reframing_attribution_shift
name: 困境归因重构型
category: 解释重构
definition: 把“是我不行”重写为“路径、结构、信息、认知出了问题”，帮助用户恢复行动感。
trigger_condition:
  - 内容与自我否定、失败归因、长期卡住相关
  - 作者能提供比“你不够好”更成立的解释
required_signals:
  - 存在自责式归因
  - 存在替代归因
optional_signals:
  - 身份处境
negative_signals:
  - 变成纯甩锅
  - 没有新的行动出口
applicable_topics:
  - 职场
  - 成长
  - 阶层
  - 赚钱
applicable_intents:
  - 修正归因
  - 释放羞耻
  - 恢复掌控感
target_emotions:
  - 释然
  - 被理解
  - 想重新开始
promise_type:
  - 解释你为什么卡住，并告诉你不只是你个人的问题
evidence_requirement: 中
title_formula:
  - "不是你不行，是你没见过/没学过/路径不对"
lexicon:
  - 不是你不行
  - 只是不会
  - 路径不对
examples:
  - 普通人家的孩子，只是不会选划算的工作
counter_examples:
  - 什么都怪环境
similar_methods_diff:
  - 与阶层创伤型不同，本方法主卖点是归因重写，不一定先点明身份
allowed_secondary_categories:
  - 身份归属
  - 认知颠覆
forbidden_secondary_categories:
  - 解释重构
```

## 方法卡：自我许可型

```yaml
id: reframing_self_permission
name: 自我许可型
category: 解释重构
definition: 通过给予心理许可，帮助用户从规训、羞耻或外部标准中暂时解脱出来。
trigger_condition:
  - 内容涉及标准答案、乖顺脚本、被规训的生活方式
  - 作者能给出一种更松动但不悬浮的合法性
required_signals:
  - 存在旧标准
  - 存在新的许可
optional_signals:
  - 女性议题
  - 边界感
negative_signals:
  - 只有情绪煽动，没有新标准
applicable_topics:
  - 女性成长
  - 人生选择
  - 边界感
  - 关系
applicable_intents:
  - 松绑
  - 解除羞耻
target_emotions:
  - 轻松
  - 解放
promise_type:
  - 允许你不再按旧标准生活
evidence_requirement: 低
title_formula:
  - "你可以不X，也可以Y"
lexicon:
  - 你可以
  - 不必
  - 不需要
examples:
  - 女生可以先探索人生，而不是只过日子
counter_examples:
  - 任何事都随心所欲就好
similar_methods_diff:
  - 与价值观反转型相比，本方法更温和，重点是给许可而不是制造不安
allowed_secondary_categories:
  - 身份归属
  - 认知颠覆
forbidden_secondary_categories:
  - 解释重构
```
