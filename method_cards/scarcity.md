# `信息稀缺` 方法卡

## 方法卡：数字未知型

```yaml
id: scarcity_numeric_unknown
name: 数字未知型
category: 信息稀缺
definition: 用多数人不知道、少数人看懂、比例失衡等表达，制造认知落差和未知感。
trigger_condition:
  - 内容里存在一个可以被包装为普遍误判的认知点
  - 该认知点和用户利益、痛点或选择直接相关
required_signals:
  - 存在可概括的认知盲区
  - 存在明确受众
  - 存在利益、避坑或判断价值
optional_signals:
  - 可量化比例
  - 可对比的人群差异
negative_signals:
  - 内容没有真实认知点，只是口号
  - 比例纯编造且无表达合理性
  - 主题过于常识，无法支撑“多数人不知道”
applicable_topics:
  - 赚钱
  - 职场
  - 成长
  - 选择判断
applicable_intents:
  - 纠偏
  - 开眼界
  - 快速抓重点
target_emotions:
  - 好奇
  - 怕落后
  - 轻微羞耻
promise_type:
  - 获取少数人知道的认知
evidence_requirement: 中
title_formula:
  - "X%的人不知道 + 痛点/方法/机会"
  - "大多数人搞错的 + 关键判断"
lexicon:
  - X%的人不知道
  - 大多数人没搞懂
  - 很多人以为
  - 其实不是
examples:
  - 90%人不知道的邪门思路
  - 90%人对赚钱没概念
counter_examples:
  - 今天聊一个大家都知道但我想再说一遍的道理
similar_methods_diff:
  - 与信息壁垒型不同，本方法卖的是“多数人没意识到”，不是“信息拿不到”
  - 与常识纠偏型不同，本方法优先触发未知感，不一定需要强反转
allowed_secondary_categories:
  - 权威借信
  - 焦虑损失
forbidden_secondary_categories:
  - 信息稀缺
```

## 方法卡：信息壁垒型

```yaml
id: scarcity_barrier
name: 信息壁垒型
category: 信息稀缺
definition: 通过构造渠道、身份、时间、价格、机会等门槛，让信息显得稀缺可得。
trigger_condition:
  - 内容可以被表述为少数人才接触到的认知或方法
  - 信息本身对用户有明确收益
required_signals:
  - 存在可命名的信息门槛
  - 存在具体利益点或避坑点
optional_signals:
  - 权威来源
  - 长时间验证
  - 免费公开/首次公开
negative_signals:
  - 内容过于普通，无法支撑稀缺感
  - 只有门槛感，没有信息内容
  - 权威或来源模糊，显得像标题党
applicable_topics:
  - 创业
  - 副业
  - 职场
  - 行业认知
  - AI工具
applicable_intents:
  - 获取内部认知
  - 少走弯路
  - 提前看见机会
target_emotions:
  - 好奇
  - 占便宜
  - 怕错过
promise_type:
  - 获取原本难拿到的信息
evidence_requirement: 高
title_formula:
  - "内部/普通人也能/行业内 + 利益/方法"
  - "免费公开/压箱底/一辈子只说一次 + 方法/认知"
lexicon:
  - 内部信息
  - 免费公开
  - 压箱底
  - 一辈子只说一次
  - 我验证了X年
  - 无意间得到
examples:
  - 内部信息，普通人的红利
  - 我决定免费公开我的创业方法
  - 50万粉博主如何恰饭，无意间得到AI内部商机
counter_examples:
  - 这是一个所有平台都能搜到的基础方法
similar_methods_diff:
  - 与权威借信不同，本方法主卖点是“获取门槛”，不是“人物可信度”
  - 与机会金矿型不同，本方法卖“拿到信息”，不是“发现蓝海”
allowed_secondary_categories:
  - 权威借信
  - 焦虑损失
forbidden_secondary_categories:
  - 信息稀缺
```

## 方法卡：机会金矿型

```yaml
id: scarcity_goldmine
name: 机会金矿型
category: 信息稀缺
definition: 宣称存在低竞争、高收益、别人没注意到的机会，以“蓝海感”驱动点击。
trigger_condition:
  - 内容中存在机会窗口、赛道差异或低竞争空间
  - 用户会把该内容理解为可转化的现实收益
required_signals:
  - 存在机会描述
  - 存在收益暗示
  - 存在“别人没说/没做/没看见”的对照
optional_signals:
  - 平台红利
  - 新行业
  - 时间窗口
negative_signals:
  - 没有真实机会，只是情绪词堆叠
  - 收益承诺过大但没有支撑
  - 内容本质是经验总结，不是机会判断
applicable_topics:
  - 赚钱
  - 创业
  - 平台红利
  - 赛道判断
applicable_intents:
  - 找机会
  - 提前布局
  - 寻找增长方向
target_emotions:
  - 贪便宜
  - 怕错过
  - 向上流动欲望
promise_type:
  - 发现别人还没重视的机会
evidence_requirement: 高
title_formula:
  - "没人说的 + 蓝海/机会/赛道"
  - "偷偷/闷声 + 赚钱/发财/布局"
lexicon:
  - 没人说
  - 蓝海
  - 偷偷
  - 闷声
  - 红利
  - 机会
examples:
  - 没人说的蓝海赛道
  - 偷偷卖一亿
  - 闷声发财
counter_examples:
  - 这是一个已经卷得很厉害但我还是想聊的赛道
similar_methods_diff:
  - 与信息壁垒型不同，本方法卖点是机会本身，而不是信息入口
  - 与路径捷径不同，本方法卖点是“做什么有机会”，不是“怎么更省力地做”
allowed_secondary_categories:
  - 焦虑损失
  - 权威借信
forbidden_secondary_categories:
  - 信息稀缺
```

## 方法卡：隐藏规则型

```yaml
id: scarcity_hidden_rules
name: 隐藏规则型
category: 信息稀缺
definition: 强调事情表面之下存在一套没被明说的运行逻辑，卖点是看见真实规则。
trigger_condition:
  - 内容不是纯方法，而是解释事情如何运作
  - 用户默认认知与真实机制之间存在落差
required_signals:
  - 存在可被概括的底层逻辑
  - 存在表象与真实机制的反差
optional_signals:
  - 圈层差异
  - 行业机制
  - 职场潜规则
negative_signals:
  - 只是普通观点，没有机制解释
  - 没有“表面 vs 真相”的张力
applicable_topics:
  - 职场
  - 人际
  - 平台机制
  - 社会观察
applicable_intents:
  - 看懂规则
  - 减少误判
  - 解释复杂现象
target_emotions:
  - 好奇
  - 清醒感
  - 防被骗
promise_type:
  - 看见事情真正怎么运作
evidence_requirement: 中
title_formula:
  - "表面上是X，其实底层是Y"
  - "真正决定X的，不是A，而是B"
lexicon:
  - 真相
  - 真实逻辑
  - 底层规则
  - 潜规则
  - 背后机制
examples:
  - 真正决定职场上升的，不是努力，是可见度
counter_examples:
  - 我单纯分享一点自己的感受
similar_methods_diff:
  - 与认知颠覆相邻，但本方法重点是“揭示规则”，而不是价值判断反转
allowed_secondary_categories:
  - 权威借信
  - 认知颠覆
forbidden_secondary_categories:
  - 信息稀缺
```
