# `reference_templates.md`

本文件用于把高质量 `reference` 标题抽象成可复用的“母版”。

目标不是从零生成标题，而是：

1. 先匹配主方法
2. 再匹配最相似的母版
3. 最后在限定槽位内改写

这样可以显著降低“重新生成标题”的不确定性。

---

## 使用原则

### 1. 先匹配方法，再匹配模板

模板不能替代方法判断。

正确顺序是：

`内容 -> 主类/主方法 -> 模板家族 -> 槽位改写`

### 2. 模板只提供表达骨架，不提供结论

模板能复用的是：

- 冲突结构
- 表达节奏
- 信息展开方式

模板不能直接照抄观点结论。

### 3. 优先做“近似母版改写”，不要做“自由发挥”

如果已经找到高相似模板，优先输出：

- 同结构改写
- 轻微变体
- 强度变体

不要跳回完全自由生成。

### 4. 模板必须带适用条件和禁用条件

一个模板只有在满足内容形态时才可调用。

---

## 模板字段

每个模板建议包含：

```yaml
template_id:
source_reference:
primary_category:
primary_method:
secondary_category:
template_family:
surface_structure:
rewrite_slots:
applicable_when:
avoid_when:
tone_profile:
abstraction_level:
strength_range:
example_rewrites:
```

字段说明：

- `template_id`
  模板唯一标识。

- `source_reference`
  来源强样本。

- `primary_category` / `primary_method`
  模板所属主类和主方法。

- `secondary_category`
  常见辅类，可为空。

- `template_family`
  模板家族名，用于聚类。

- `surface_structure`
  表面表达骨架。

- `rewrite_slots`
  可替换槽位。

- `applicable_when`
  何时适用。

- `avoid_when`
  何时不要用。

- `tone_profile`
  语气特征。

- `abstraction_level`
  抽象度。

- `strength_range`
  适合输出的强度。

- `example_rewrites`
  演示如何改写。

---

## 模板库

## Template 1. 不是A，是B

```yaml
template_id: tpl_not_a_b
source_reference:
  - 穿的不是衣服，是权力感
  - 我不是情绪稳定了，我是有钱了
  - 感情中最该守住的，不是底线，是注意力
primary_category: 认知颠覆
primary_method: 价值观反转型
secondary_category:
  - 解释重构
  - 信息稀缺
template_family: 判断重写型
surface_structure: 不是A，是B
rewrite_slots:
  - A: 用户默认理解
  - B: 新判断/真实解释/更高优先级对象
applicable_when:
  - 内容核心在于替换默认答案
  - A和B之间有清晰对撞
  - B比A更有解释力或更有张力
avoid_when:
  - A不明确
  - B过于抽象，无法落地
  - 内容并非重写判断，而是给路径
tone_profile: 锋利、判断感强、短句
abstraction_level: medium
strength_range:
  - strong
  - balanced
example_rewrites:
  - 你缺的不是努力，是判断力
  - 婚姻里最该守住的，不是体面，是边界
```

## Template 2. 你以为A，其实B

```yaml
template_id: tpl_you_think_a_b
source_reference:
  - 你以为你在过渡，其实这就是你的一生。
  - 查没查出什么，对你都没好处。
primary_category: 认知颠覆
primary_method: 因果质疑型
secondary_category:
  - 解释重构
  - 焦虑损失
template_family: 预设反转型
surface_structure: 你以为A，其实B
rewrite_slots:
  - A: 用户默认假设/动作收益
  - B: 真实结果/反结论
applicable_when:
  - 内容里存在明显默认假设
  - 可以明确指出该假设失效
avoid_when:
  - 只是换说法，没有反结论
  - B没有信息增量
tone_profile: 直接、冲击、对抗感适中
abstraction_level: medium
strength_range:
  - strong
  - balanced
example_rewrites:
  - 你以为你在忍，其实你在教别人怎么对你
  - 你以为换城市能重来，其实你只是把旧问题搬走
```

## Template 3. 有些X，是你Y的

```yaml
template_id: tpl_some_x_is_y
source_reference:
  - 有些痛苦，是你选的
primary_category: 认知颠覆
primary_method: 因果质疑型
secondary_category:
  - 解释重构
template_family: 归因重击型
surface_structure: 有些X，是你Y的
rewrite_slots:
  - X: 负面结果/持续困境
  - Y: 选择/默许/长期动作
applicable_when:
  - 内容本质是归因重写
  - 用户通常把结果归因给外界
avoid_when:
  - 容易变成受害者指责
  - 没有后续解释支撑
tone_profile: 短促、冒犯感、讨论度高
abstraction_level: medium
strength_range:
  - strong
example_rewrites:
  - 有些委屈，是你长期讨好换来的
  - 有些失控，是你一直不肯做决定
```

## Template 4. X之后，才知道Y

```yaml
template_id: tpl_after_x_then_y
source_reference:
  - 赚到一百万之后，才知道为什么赚不到
primary_category: 认知颠覆
primary_method: 认知顺序重排型
secondary_category:
  - 路径捷径
template_family: 迟得认知型
surface_structure: X之后，才知道Y
rewrite_slots:
  - X: 某个结果/阶段/里程碑
  - Y: 更底层的认知
applicable_when:
  - 内容强调“知道得太晚”
  - 存在明确前后认知落差
avoid_when:
  - X不具体
  - Y过于普通
tone_profile: 后知后觉、经验浓度高
abstraction_level: high
strength_range:
  - balanced
  - soft
example_rewrites:
  - 离开那段关系之后，才知道自己当时到底在失去什么
  - 开始赚钱之后，才知道以前根本不是不努力
```

## Template 5. X没教，但Y得知道

```yaml
template_id: tpl_not_taught_but_must_know
source_reference:
  - 妈妈没教，但女孩得知道的小知识
primary_category: 信息稀缺
primary_method: 信息壁垒型
secondary_category:
  - 身份归属
template_family: 缺失知识补位型
surface_structure: X没教，但Y得知道
rewrite_slots:
  - X: 原本应承担传递角色的人/系统
  - Y: 目标人群
  - 补充项: 知识/判断/规则
applicable_when:
  - 内容承诺补一个被忽略的知识缺口
  - 目标人群明确
avoid_when:
  - 不是知识缺口，而是价值表达
  - Y不明确
tone_profile: 补课感、私密感、专属感
abstraction_level: low
strength_range:
  - balanced
example_rewrites:
  - 学校没教，但普通人一定要懂的谈薪规则
  - 没人提醒，但女生越早知道越好的边界感
```

## Template 6. 没人说的X

```yaml
template_id: tpl_no_one_tells_x
source_reference:
  - 没人说的蓝海赛道
primary_category: 信息稀缺
primary_method: 机会金矿型
secondary_category:
  - 焦虑损失
template_family: 蓝海机会型
surface_structure: 没人说的X
rewrite_slots:
  - X: 机会/赛道/高回报对象
applicable_when:
  - 内容里真有低竞争、高收益机会
  - 能展开为什么“没人说”
avoid_when:
  - 只是普通赛道包装成蓝海
  - 没有收益依据
tone_profile: 稀缺、窗口、低调发财感
abstraction_level: low
strength_range:
  - strong
  - balanced
example_rewrites:
  - 没人说的县城服务业机会
  - 没人讲透的中年转型入口
```

## Template 7. 我身边的X都在Y

```yaml
template_id: tpl_people_around_me_doing_y
source_reference:
  - 我身边的老板们在偷偷投资什么？
primary_category: 权威借信
primary_method: 贴身见闻型
secondary_category:
  - 信息稀缺
template_family: 近身观察型
surface_structure: 我身边的X都在Y
rewrite_slots:
  - X: 某类高势能人群
  - Y: 共同动作/共同判断
applicable_when:
  - 说话者具备贴身观察视角
  - X和Y之间存在可转述规律
avoid_when:
  - 只是借圈层标签
  - 观察样本过少
tone_profile: 近身、偷师感、可接近
abstraction_level: low
strength_range:
  - balanced
example_rewrites:
  - 我接触过的厉害销售，都很少急着成交
  - 我认识的有钱人，买东西都很少只看价格
```

## Template 8. X教我的Y

```yaml
template_id: tpl_x_taught_me_y
source_reference:
  - 亿万身家温州老板教我的理财五不做
  - 姥爷教我降维打法
primary_category: 权威借信
primary_method: 家族权威型
secondary_category:
  - 路径捷径
  - 信息稀缺
template_family: 权威传授型
surface_structure: X教我的Y
rewrite_slots:
  - X: 权威来源
  - Y: 方法/原则/动作
applicable_when:
  - 权威来源明确
  - Y可被提炼成可传授内容
avoid_when:
  - 只有人名没有方法
  - 权威来源与内容无关
tone_profile: 可信、经验传递、距离近
abstraction_level: low
strength_range:
  - balanced
example_rewrites:
  - 一个创业十年的老板教我的谈判顺序
  - 我妈教我的关系止损法
```

## Template 9. X都不值得你Y

```yaml
template_id: tpl_x_not_worth_y
source_reference:
  - 绝大多数人不值得你烦恼
primary_category: 解释重构
primary_method: 负面信号重定义型
secondary_category:
  - 身份归属
template_family: 精神资源止损型
surface_structure: X都不值得你Y
rewrite_slots:
  - X: 外界对象/噪音来源
  - Y: 情绪投入/注意力投入
applicable_when:
  - 内容重点是重配精神资源
  - 需要帮用户从高敏反应里抽出来
avoid_when:
  - 内容重点不是情绪止损
  - 容易显得太高姿态
tone_profile: 切断感、清场感、轻蔑感适中
abstraction_level: medium
strength_range:
  - strong
  - balanced
example_rewrites:
  - 不是每个误解都值得你解释
  - 绝大多数冷暴力，都不值得你自责
```

## Template 10. X不是A，是B

```yaml
template_id: tpl_x_is_not_a_b
source_reference:
  - 自信不是鸡汤，是策略
  - 出轨不是自由，是短视
primary_category: 认知颠覆
primary_method: 常识纠偏型
secondary_category:
  - 价值观反转型
template_family: 概念重定义型
surface_structure: X不是A，是B
rewrite_slots:
  - X: 某个常见概念
  - A: 用户默认错误理解
  - B: 作者给出的更准定义
applicable_when:
  - 内容在重定义一个概念
  - A与B能够形成鲜明差异
avoid_when:
  - B太空
  - X本身不具备公共认知基础
tone_profile: 利落、定义感强、适合口播开头
abstraction_level: medium
strength_range:
  - strong
  - balanced
example_rewrites:
  - 情绪稳定不是忍住，是有能力不乱
  - 独立不是逞强，是有退路
```

## Template 11. X后，我Y

```yaml
template_id: tpl_after_x_i_y
source_reference:
  - 买房后，我无家可归
  - 成为互联网野人后，我找到了人生开挂的捷径！
primary_category: 焦虑损失
primary_method: 选择代价型
secondary_category:
  - 路径捷径
  - 认知颠覆
template_family: 结果反噬型
surface_structure: X后，我Y
rewrite_slots:
  - X: 某个重大动作/重大选择
  - Y: 反常识后果/新状态
applicable_when:
  - 内容有清晰的选择节点
  - 选择后的后果与常规预期相反
avoid_when:
  - 只是普通经历，没有反差
  - Y不够具体
tone_profile: 叙事感、反差感、强钩子
abstraction_level: low
strength_range:
  - strong
  - balanced
example_rewrites:
  - 结婚后，我第一次真正一个人生活
  - 裁员后，我才开始赚钱
```

## Template 12. X越A，越B

```yaml
template_id: tpl_more_a_more_b
source_reference:
  - 情商越高，越无法向上社交
primary_category: 认知颠覆
primary_method: 因果质疑型
secondary_category:
  - 隐藏规则型
template_family: 反因果递进型
surface_structure: X越A，越B
rewrite_slots:
  - X: 某种能力/动作/倾向
  - A: 用户默认正向程度
  - B: 反常识负结果
applicable_when:
  - 内容在挑战某个“越多越好”的假设
  - B足够意外
avoid_when:
  - 逻辑不成立
  - 只是情绪化对立
tone_profile: 锋利、因果反咬、争议性强
abstraction_level: medium
strength_range:
  - strong
example_rewrites:
  - 你越懂事，越容易被当成理所当然
  - 你越怕麻烦别人，越容易累死自己
```

---

## 推荐调用流程

推荐把标题生成链路改成：

1. 用 `rules.md` 判定主类和主方法
2. 在本文件中筛选同 `primary_method` 的模板
3. 用内容信号判断最相似的 `template_family`
4. 只在 `rewrite_slots` 内进行替换
5. 输出：
   - `best_template`
   - `rewrite_reason`
   - `draft_titles`

推荐最小输出新增字段：

```yaml
best_template:
template_family:
rewrite_reason:
slot_mapping:
```

---

## 与其他文件的关系

本文件负责：

- 把强样本转成可仿写模板
- 降低自由生成不确定性
- 为后续“参考匹配 -> 改写”提供中间层

本文件不负责：

- 判定主类
- 判定主方法
- 替代 reference 原样本库

相关文件：

- 规则判断：[rules.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/rules.md)
- 方法定义：[method_cards](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/method_cards)
- 强样本：[strong_titles.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/strong_titles.md)
- 边界样本：[boundary_cases.md](/Users/coreyzh/Documents/Corey的商业/小致的风火山林/02方法论沉淀/02标题方法论/references/boundary_cases.md)
