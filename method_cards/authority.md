# `权威借信` 方法卡

## 方法卡：家族权威型

```yaml
id: authority_family
name: 家族权威型
category: 权威借信
definition: 借长辈、父母、亲密关系中的身份和人生经验建立可信度，缩短心理距离。
trigger_condition:
  - 内容适合以关系中的智慧传递来表达
  - 说话者或信息来源具备亲近而有分量的身份
required_signals:
  - 明确的家族或亲密关系身份
  - 可被传授的经验、建议或判断
optional_signals:
  - 高知背景
  - 年龄
  - 反刻板印象
negative_signals:
  - 只有身份，没有内容
  - 身份过于生硬，像强贴标签
applicable_topics:
  - 婚恋
  - 人生建议
  - 女性成长
  - 家庭关系
applicable_intents:
  - 降低防御
  - 提高接受度
  - 传递经验
target_emotions:
  - 信任
  - 被照顾
  - 被点醒
promise_type:
  - 得到来自亲近权威的经验判断
evidence_requirement: 高
title_formula:
  - "家族身份 + 教我/讲 + 方法/判断"
lexicon:
  - 我妈
  - 我爸
  - 姥爷
  - 高知长辈
  - 60岁妈妈
examples:
  - 姥爷教我降维打法
  - 高知男长辈讲：如何婚前擦亮眼
  - 60岁高知妈妈病好后大彻大悟教我的
counter_examples:
  - 随便找个人设成长辈口吻输出建议
similar_methods_diff:
  - 与经验权威型不同，本方法的核心不是年数，而是关系信任
allowed_secondary_categories:
  - 解释重构
  - 身份归属
forbidden_secondary_categories:
  - 权威借信
```

## 方法卡：财富权威型

```yaml
id: authority_wealth
name: 财富权威型
category: 权威借信
definition: 用财富规模、老板身份、阶层标签做可信度代理，让用户默认“他们有资格说”。
trigger_condition:
  - 内容与赚钱、选择、效率、商业判断相关
  - 可借用明确财富或社会身份
required_signals:
  - 明确财富数字或高势能身份
  - 与内容存在相关性
optional_signals:
  - 地域商业标签
  - 圈层接触感
negative_signals:
  - 财富身份与内容无关
  - 财富标签太空泛
  - 夸张到失真
applicable_topics:
  - 赚钱
  - 创业
  - 理财
  - 职场判断
applicable_intents:
  - 建立可信度
  - 借势提高点击
target_emotions:
  - 信服
  - 羡慕
  - 想复制
promise_type:
  - 跟成功者借判断
evidence_requirement: 高
title_formula:
  - "财富数字/身份 + 教我/告诉我 + 方法"
lexicon:
  - 亿万身家
  - 年入X
  - 温州老板
  - 富婆
  - 阔太
examples:
  - 亿万身家温州老板教我的理财五不做
  - 年入2亿的创业者聊创业机会
  - 我身边的老板们在偷偷投资什么
counter_examples:
  - 一个没法验证的有钱人朋友说
similar_methods_diff:
  - 与贴身见闻型不同，本方法的重点是权威身份本身，不是观察视角
allowed_secondary_categories:
  - 路径捷径
  - 信息稀缺
forbidden_secondary_categories:
  - 权威借信
```

## 方法卡：大佬背书型

```yaml
id: authority_bigshot
name: 大佬背书型
category: 权威借信
definition: 用知名成功者、企业家或公共权威为某个方法、书籍、观点背书，缩短成功心理距离。
trigger_condition:
  - 内容中存在可明确挂靠的大人物或公共成功样本
  - 该权威与主题强相关
required_signals:
  - 可识别的知名人物
  - 可转述的推荐、启发或学习动作
optional_signals:
  - 普适感
  - 可模仿感
negative_signals:
  - 只是蹭名字
  - 权威与主题弱相关
applicable_topics:
  - 商业
  - 思维
  - 学习方法
  - 投资
applicable_intents:
  - 降低怀疑
  - 缩短心理距离
target_emotions:
  - 信任
  - 模仿欲
  - 连接感
promise_type:
  - 学成功者也在学的东西
evidence_requirement: 高
title_formula:
  - "知名人物 + 推荐/学习/启发 + 方法/书/观点"
lexicon:
  - 雷军也在学
  - 李想推荐
  - 段永平的启发
  - 向大师学
examples:
  - 雷军居然学日本akb48女团营销
  - 李想推荐的这本书聊的是强者思维
  - 跟优衣库创始人学如何管理注意力
counter_examples:
  - 用一个名人名字硬包装普通内容
similar_methods_diff:
  - 与财富权威型不同，本方法强调可识别人物的背书，不只是成功阶层标签
allowed_secondary_categories:
  - 路径捷径
  - 信息稀缺
forbidden_secondary_categories:
  - 权威借信
```

## 方法卡：经验权威型

```yaml
id: authority_experience
name: 经验权威型
category: 权威借信
definition: 用长期实践、时间积累和反复验证建立专业可信度。
trigger_condition:
  - 内容来自长期沉淀，而非短期心得
  - 时间本身能增强结论可信度
required_signals:
  - 年限
  - 实践对象
  - 稳定结论
optional_signals:
  - 行业标签
  - 老手身份
negative_signals:
  - 只有年数，没有内容
  - 年数和结论无关
applicable_topics:
  - 行业经验
  - 生活经验
  - 技能方法
applicable_intents:
  - 建立稳感
  - 提高可信度
target_emotions:
  - 安心
  - 信任
promise_type:
  - 学已经被验证过的经验
evidence_requirement: 高
title_formula:
  - "X年/三十年 + 老师傅/老手 + 教我/告诉我 + 方法"
lexicon:
  - 三十年
  - 老师傅
  - 做了X年
  - 验证了X年
examples:
  - 三十年老师傅教我：什么衣服便宜贵的都一样
counter_examples:
  - 做了很多年但没什么结论
similar_methods_diff:
  - 与家族权威型不同，本方法不靠关系亲近感，而靠实践年限
allowed_secondary_categories:
  - 路径捷径
  - 解释重构
forbidden_secondary_categories:
  - 权威借信
```

## 方法卡：贴身见闻型

```yaml
id: authority_close_observation
name: 贴身见闻型
category: 权威借信
definition: 通过“我接触过这类人/圈层”建立观察者可信度，重点是可接近性而非顶格权威。
trigger_condition:
  - 内容基于近距离观察某一类强势样本
  - 说话者位置具备旁观可信度
required_signals:
  - 存在被观察对象
  - 存在贴近性叙述
optional_signals:
  - 圈层洞察
  - 反直觉观察
negative_signals:
  - 观察来源模糊
  - 只是借人设，不是真观察
applicable_topics:
  - 阶层观察
  - 老板思维
  - 人群差异
  - 行业洞察
applicable_intents:
  - 提供近距离样本
  - 降低距离感
target_emotions:
  - 好奇
  - 信任
  - 想偷师
promise_type:
  - 从近距离观察中提炼判断
evidence_requirement: 高
title_formula:
  - "我接触过/我身边的 + 某类人 + 在怎么做"
lexicon:
  - 我身边的老板们
  - 我认识一位
  - 我接触过的有钱人
examples:
  - 我身边的老板们在偷偷投资什么？
  - 我在网上认识一位年入20亿的网友
counter_examples:
  - 我听说某类人都这样
similar_methods_diff:
  - 与财富权威型不同，本方法卖的是观察视角和接近性
allowed_secondary_categories:
  - 信息稀缺
  - 路径捷径
forbidden_secondary_categories:
  - 权威借信
```
