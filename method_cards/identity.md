# `身份归属` 方法卡

## 方法卡：普通人阵营型

```yaml
id: identity_ordinary_people
name: 普通人阵营型
category: 身份归属
definition: 用“我们普通人”“没背景的人”等表达先完成同类归队，再承接观点或方法。
trigger_condition:
  - 内容明显服务于非精英、非强资源人群
  - 用户会因为被点名而提升代入感
required_signals:
  - 明确群体身份
  - 群体处境或共同限制
optional_signals:
  - 和强势人群对照
negative_signals:
  - 群体指向太泛
  - 点名人群后没有真正服务这类人
applicable_topics:
  - 赚钱
  - 成长
  - 职场
  - 人生路径
applicable_intents:
  - 提高代入
  - 降低防御
  - 让用户觉得被理解
target_emotions:
  - 被看见
  - 同类感
promise_type:
  - 为某类普通人提供更适合的判断
evidence_requirement: 中
title_formula:
  - "我们/普通人/没背景的人 + 真正要解决的问题"
lexicon:
  - 我们普通人
  - 普通人
  - 没背景的人
examples:
  - 我们普通家庭出来的孩子，思维差在哪？
counter_examples:
  - 随便套普通人标签吸引流量
similar_methods_diff:
  - 与阶层创伤型不同，本方法侧重同类认同，不一定强调创伤结构
allowed_secondary_categories:
  - 解释重构
  - 焦虑损失
forbidden_secondary_categories:
  - 身份归属
```

## 方法卡：阶层创伤型

```yaml
id: identity_class_trauma
name: 阶层创伤型
category: 身份归属
definition: 点名出身、资源、信息继承差异造成的结构性受限，再将困境从能力缺陷重构为认知缺口。
trigger_condition:
  - 内容与出身、资源差、路径选择直接相关
  - 文中存在从“我不行”转向“结构/信息差”的归因重构
required_signals:
  - 明确的出身或阶层身份
  - 明确的受限感
  - 归因重构
optional_signals:
  - 与中产、强资源人群对照
negative_signals:
  - 只有抱怨，没有重构
  - 对用户处境定义过头，显得冒犯
applicable_topics:
  - 教育
  - 职业选择
  - 财富认知
  - 人生机会
applicable_intents:
  - 命名痛点
  - 重写归因
  - 给希望
target_emotions:
  - 被理解
  - 委屈被说中
  - 重新获得掌控感
promise_type:
  - 解释为什么普通出身的人更容易卡住
evidence_requirement: 中
title_formula:
  - "普通家庭/中产家庭/某类出身 + 真实困境 + 新归因"
lexicon:
  - 普通家庭出来的孩子
  - 中产家庭
  - 阶层惯性
  - 只是不会
examples:
  - 普通人家的孩子，只是不会选划算的工作
  - 大佬给的信息差，和中产家庭教我的正好相反
counter_examples:
  - 纯粹制造对立，不给任何解释出口
similar_methods_diff:
  - 与困境归因重构型不同，本方法先锁定阶层身份，再做归因重写
allowed_secondary_categories:
  - 解释重构
  - 焦虑损失
forbidden_secondary_categories:
  - 身份归属
```

## 方法卡：特定人群点名型

```yaml
id: identity_specific_group
name: 特定人群点名型
category: 身份归属
definition: 直接点名某一类清晰人群，让标题瞬间提高相关性。
trigger_condition:
  - 内容天然对应某类明确用户
  - 该类人群有独特痛点或目标
required_signals:
  - 清晰人群标签
  - 与内容强相关
optional_signals:
  - 场景或阶段特征
negative_signals:
  - 人群定义太宽
  - 人群与内容弱相关
applicable_topics:
  - 女性
  - 宝妈
  - 创业者
  - 打工人
  - 学生
applicable_intents:
  - 提高点击相关性
  - 快速筛选受众
target_emotions:
  - 这就是在说我
promise_type:
  - 为某一类人提供专属判断
evidence_requirement: 低
title_formula:
  - "某类人 + 最该知道的判断/方法"
lexicon:
  - 女生
  - 打工人
  - 创业者
  - 宝妈
examples:
  - 女生要先探索人生，而不是只过日子
counter_examples:
  - 为了吸引点击随便点名一个群体
similar_methods_diff:
  - 与普通人阵营型不同，本方法群体更窄、更明确
allowed_secondary_categories:
  - 解释重构
  - 焦虑损失
forbidden_secondary_categories:
  - 身份归属
```

## 方法卡：关系角色型

```yaml
id: identity_role_based
name: 关系角色型
category: 身份归属
definition: 从人生角色切入，而非阶层切入，让用户以角色责任和处境代入内容。
trigger_condition:
  - 内容与用户所扮演角色强相关
  - 角色本身能携带决策压力或身份感
required_signals:
  - 明确角色
  - 与角色强相关的问题
optional_signals:
  - 关系张力
negative_signals:
  - 角色标签只是修饰词
applicable_topics:
  - 婚恋
  - 亲子
  - 家庭
  - 职场关系
applicable_intents:
  - 强化角色代入
  - 放大相关性
target_emotions:
  - 代入
  - 责任感
promise_type:
  - 针对该角色提供判断或方法
evidence_requirement: 低
title_formula:
  - "某角色 + 最容易忽略的问题/方法"
lexicon:
  - 女儿
  - 妈妈
  - 伴侣
  - 领导
examples:
  - 爸爸对女儿的建议：如何选好老公几率达90%
counter_examples:
  - 只换角色词，不改变内容
similar_methods_diff:
  - 与家族权威型不同，本方法卖的是“你是谁”，不是“谁在教你”
allowed_secondary_categories:
  - 权威借信
  - 解释重构
forbidden_secondary_categories:
  - 身份归属
```
