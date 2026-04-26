# `boundary_cases.md`

本文件用于收录容易误判、跨类、边界模糊的标题样本。

作用不是判断标题好不好，而是训练系统处理以下问题：

- 看起来像某一类，实际上主驱动力是另一类
- 主类和辅类容易抢位置
- 表面句式相似，但底层心理机制不同
- 同一句标题，为什么不能被多个方法同时主命中

默认原则：

- 每个样本必须明确“误判点”
- 每个样本必须明确“最终归类”
- 每个样本必须说明“为什么不是另一个相邻类”

---

## Case 1. 感情中最该守住的，是注意力

```yaml
title: 感情中最该守住的，是注意力
likely_misread_as:
  - 解释重构
  - 身份归属
final_primary_category: 认知颠覆
final_primary_method: 价值观反转型
secondary_category: 路径捷径
secondary_role: efficiency
misread_reason:
  - "守住注意力"容易被读成情绪安顿
  - "感情中"容易被误判成关系人群定向
final_reason:
  - 核心不是安顿情绪，而是重排“感情里什么最重要”的价值顺序
  - 用户默认答案可能是爱、底线、安全感、真诚，标题反而给出“注意力”
why_not_other_categories:
  - 不是解释重构：它没有重写已有痛苦的意义，而是在改写判断标准
  - 不是身份归属：没有点名特定人群，关系场景不等于身份类
boundary_rule:
  - 只要标题核心动作是“把重要性排序改掉”，优先判为认知颠覆
```

## Case 2. 查没查出什么，对你都没好处。

```yaml
title: 查没查出什么，对你都没好处。
likely_misread_as:
  - 解释重构
  - 焦虑损失
final_primary_category: 认知颠覆
final_primary_method: 因果质疑型
secondary_category: 焦虑损失
secondary_role: urgency
misread_reason:
  - 标题在说“对你没好处”，容易被看成后果警告
  - 恋爱冲突场景容易被读成情绪安抚
final_reason:
  - 核心点击力在于推翻“查手机能解决问题/获得安全感”的默认因果
  - “没好处”只是反因果成立后的结果，不是主承诺
why_not_other_categories:
  - 不是焦虑损失：损失感是辅助张力，不是第一驱动力
  - 不是解释重构：重点不是重新理解痛苦，而是推翻行动收益判断
boundary_rule:
  - 只要标题主张是“你以为这个动作有用，其实没有用”，优先判因果质疑型
```

## Case 3. 我不是情绪稳定了，我是有钱了

```yaml
title: 我不是情绪稳定了，我是有钱了
likely_misread_as:
  - 认知颠覆
  - 解释重构
final_primary_category: 信息稀缺
final_primary_method: 隐藏规则型
secondary_category: 认知颠覆
secondary_role: tension
misread_reason:
  - 句式很像“你以为A，其实B”，表面很反常识
  - 也容易被读成对个人状态的重新解释
final_reason:
  - 标题真正卖的是一个“大家不明说的真实规则”：资源条件会塑造情绪状态
  - 它首先提供的是机制揭示，而不是价值反转
why_not_other_categories:
  - 不是认知颠覆：反转只是表面句式，底层更像揭示隐藏机制
  - 不是解释重构：不是在安顿某个人的处境，而是在揭示社会规律
boundary_rule:
  - 如果标题重点是“事情真实怎么运作”，优先判隐藏规则型
```

## Case 4. 买房后，我无家可归

```yaml
title: 买房后，我无家可归
likely_misread_as:
  - 认知颠覆
  - 身份归属
final_primary_category: 焦虑损失
final_primary_method: 选择代价型
secondary_category: 认知颠覆
secondary_role: tension
misread_reason:
  - 句子有很强反差，看起来像典型反常识
  - 家庭、女性、婚姻议题也容易带出人群代入
final_reason:
  - 核心驱动力是“一个本该带来安全的选择，反而可能带来巨大代价”
  - 用户点开主要是想知道：为什么买房会导致失去归属
why_not_other_categories:
  - 不是认知颠覆：反差存在，但点击核心是选择代价
  - 不是身份归属：虽然某些群体更共鸣，但标题本身没先点名身份
boundary_rule:
  - 只要标题中心是“某个重大选择带来的隐藏代价”，优先判选择代价型
```

## Case 5. 妈妈没教，但女孩得知道的小知识

```yaml
title: 妈妈没教，但女孩得知道的小知识
likely_misread_as:
  - 身份归属
  - 权威借信
final_primary_category: 信息稀缺
final_primary_method: 信息壁垒型
secondary_category: 身份归属
secondary_role: audience_lock
misread_reason:
  - "女孩"会让人优先想到人群定向
  - "妈妈没教"会被误读为家族权威场景
final_reason:
  - 核心承诺是“你漏掉了一类重要知识，现在补给你”
  - 女孩身份是锁定受众，不是标题主要卖点
why_not_other_categories:
  - 不是身份归属：点名人群只是增强相关性，主承诺仍然是补知识缺口
  - 不是权威借信：这里没有借妈妈建立信任，反而在强调知识未被传递
boundary_rule:
  - 如果标题第一承诺是“你可能不知道但该知道”，优先判信息壁垒型
```

## Case 6. 我爸说，丑女孩才能成功

```yaml
title: 我爸说，丑女孩才能成功
likely_misread_as:
  - 认知颠覆
  - 身份归属
final_primary_category: 权威借信
final_primary_method: 家族权威型
secondary_category: 认知颠覆
secondary_role: tension
misread_reason:
  - 观点本身非常反常识，很容易压过来源
  - "丑女孩"会让人误判为身份点名型
final_reason:
  - 标题第一抓手是“我爸说”，也就是谁在说
  - 观点虽然刺痛，但来源先完成可信度和故事入口
why_not_other_categories:
  - 不是认知颠覆：反常识是张力来源，但不是第一点击驱动
  - 不是身份归属：人群标签是观点承接对象，不是标题起手核心
boundary_rule:
  - 当标题以“谁说的”作为第一钩子时，优先判权威借信
```

## Case 7. 一个人都不请的婚礼，有多爽？

```yaml
title: 一个人都不请的婚礼，有多爽？
likely_misread_as:
  - 路径捷径
  - 焦虑损失
final_primary_category: 认知颠覆
final_primary_method: 价值观反转型
secondary_category: 路径捷径
secondary_role: efficiency
misread_reason:
  - 不请人、极简婚礼容易被读成省钱省事的低成本路径
  - 婚礼议题也容易引出“传统做法让人吃亏”的损失框架
final_reason:
  - 核心在于把“不请人”从失礼/遗憾翻转成“爽”
  - 省力和省钱只是反转成立后的次级收益
why_not_other_categories:
  - 不是路径捷径：用户先被吸引的不是更省事，而是价值判断被推翻
  - 不是焦虑损失：没有先打“再这样会吃亏”的警报
boundary_rule:
  - 当标题把一个被默认“不体面”的选择改写成高收益体验时，优先判价值观反转型
```

## Case 8. 文科废物编简历，抢了班长的offer

```yaml
title: 文科废物编简历，抢了班长的offer
likely_misread_as:
  - 身份归属
  - 认知颠覆
final_primary_category: 路径捷径
final_primary_method: 杠杆加速型
secondary_category: 身份归属
secondary_role: audience_lock
misread_reason:
  - "文科废物"极强身份自降，很容易优先判为普通人阵营或特定人群
  - 结果反差也像一种反常识逆袭
final_reason:
  - 真正卖点是“通过简历这个杠杆实现超车”
  - 身份标签只是让弱势求职者更快代入
why_not_other_categories:
  - 不是身份归属：标题不是停留在“这说的是我”，而是承诺一个超车机制
  - 不是认知颠覆：反差只是结果呈现，主承诺仍然是路径效率
boundary_rule:
  - 只要标题中心是“弱势者通过方法杠杆获得更高结果”，优先判路径捷径
```

## Case 9. 绝大多数人不值得你烦恼

```yaml
title: 绝大多数人不值得你烦恼
likely_misread_as:
  - 认知颠覆
  - 焦虑损失
final_primary_category: 解释重构
final_primary_method: 负面信号重定义型
secondary_category: 身份归属
secondary_role: audience_lock
misread_reason:
  - 句子非常像一种强观点判断，容易被放进认知颠覆
  - “不值得”也会让人误判成风险/损失导向
final_reason:
  - 核心是把“我被别人影响得很重”重新安顿为“这些人不值得占用我的精神资源”
  - 它首先提供的是情绪止损和意义重置
why_not_other_categories:
  - 不是认知颠覆：不是挑战公共常识，而是帮助个体重置注意力
  - 不是焦虑损失：没有制造未来警报，而是在当下做解释重写
boundary_rule:
  - 如果标题主要功能是帮用户重新安排精神资源，优先判解释重构
```

## Case 10. 屁股决定脑袋

```yaml
title: 屁股决定脑袋
likely_misread_as:
  - 认知颠覆
  - 价值观反转型
final_primary_category: 信息稀缺
final_primary_method: 隐藏规则型
secondary_category: 认知颠覆
secondary_role: tension
misread_reason:
  - 表达粗暴短促，很像一句单纯反常识判断
  - 容易被看成“立场宣言”而不是规则揭示
final_reason:
  - 这句话的真正价值在于揭示“立场和利益先塑造观点”的运行规则
  - 它卖的是看透机制，不是单纯制造冲突
why_not_other_categories:
  - 不是价值观反转：没有直接挑战一个被赞美的道德判断
  - 不是一般认知颠覆：反常识只是入口，机制揭示才是主货
boundary_rule:
  - 当一句短标题本质在揭示底层运行逻辑时，优先判隐藏规则型
```

---

## 当前边界总结

最常见的误判模式有 4 类：

1. 看到反差句式，就误判成 `认知颠覆`
说明：
很多标题表面是“不是A，是B”，但底层可能是在卖隐藏规则、路径替代或选择代价。

2. 看到人群词，就误判成 `身份归属`
说明：
人群词很多时候只是 `audience_lock`，并不一定承担主点击驱动力。

3. 看到关系/情绪话题，就误判成 `解释重构`
说明：
要看标题是在安顿处境，还是在推翻因果、重排价值、揭示规则。

4. 看到省事、省钱、省力，就误判成 `路径捷径`
说明：
如果真正的第一驱动力是“这件事原来不该这么理解”，主类仍可能是 `认知颠覆`。

---

## 使用建议

在做自动匹配时，若一个标题同时命中两个以上一级类，优先读取本文件中的相邻案例说明，再决定主类。

本文件优先级高于：

- 纯表面句式判断
- 单个关键词命中

本文件优先级低于：

- `rules.md` 的系统级总规则
