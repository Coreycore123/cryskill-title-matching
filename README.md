# cryskill-title-matching

一个 `cryskill`（全称 `coreyskill`）前缀下的标题匹配技能库，用来解决四类任务：

- 行业话题生成标题
- 正文内容生成标题
- 优化已有标题
- 分析高数据标题为什么有效

这套仓库的核心不是“自由生成标题”，而是：

`先判断标题方法 -> 再匹配强样本母版 -> 最后做受控改写`

---

## 核心能力

### 1. 标题方法匹配

根据内容判断最适合激活的点击驱动力，例如：

- 信息稀缺
- 认知颠覆
- 权威借信
- 身份归属
- 焦虑损失
- 路径捷径
- 解释重构

### 2. 强样本匹配

不从零自由生成标题，而是优先匹配：

- 强标题样本
- 边界案例
- 可仿写模板

### 3. 受控改写

标题生成不是随意发挥，而是：

- 先找母版
- 再做槽位映射
- 最后输出 `<=21字` 的标题

### 4. 长度约束

硬性规则：

`标题包括标点在内，不得超过21个字。`

---

## 仓库结构

```text
.
├── SKILL.md
├── README.md
├── rules.md
├── output_schema.md
├── method_cards/
│   ├── anxiety.md
│   ├── authority.md
│   ├── contrarian.md
│   ├── identity.md
│   ├── reframing.md
│   ├── scarcity.md
│   └── shortcut.md
└── references/
    ├── boundary_cases.md
    ├── reference_templates.md
    └── strong_titles.md
```

---

## 文件说明

### `SKILL.md`

入口文件。  
定义目标、使用模式、工作流和调用顺序。

### `rules.md`

系统规则层。  
定义分类树、主辅规则、边界规则、禁用规则、长度规则。

### `method_cards/`

方法卡层。  
定义每种标题方法的：

- 触发条件
- 必要信号
- 禁用信号
- 适用内容
- 相邻方法区别

### `references/strong_titles.md`

强样本库。  
记录高表现标题为什么有效。

### `references/boundary_cases.md`

边界案例库。  
记录容易误判的标题，以及为什么不是另一个方法。

### `references/reference_templates.md`

标题母版库。  
用于做模板匹配和槽位改写，降低自由生成的不确定性。

### `output_schema.md`

输出规范。  
定义最终结构化结果长什么样。

---

## 使用模式

本 Skill 默认支持 4 种模式：

- `topic_to_title`
- `content_to_title`
- `optimize_existing_title`
- `analyze_reference_title`

### `topic_to_title`

输入一个行业话题或一句话命题，输出适合的标题。

### `content_to_title`

输入正文或口播内容，提炼核心承诺并生成标题。

### `optimize_existing_title`

输入一个已有标题，判断它命中的方法，并做优化。

### `analyze_reference_title`

输入一个高数据标题，分析为什么有效，并决定是否纳入样本库。

---

## 推荐工作流

推荐调用顺序：

1. 读取 `SKILL.md`
2. 读取 `rules.md`
3. 匹配 `method_cards/`
4. 参考 `references/boundary_cases.md`
5. 匹配 `references/reference_templates.md`
6. 按 `output_schema.md` 输出结果

推荐生成链路：

`内容 -> 分类 -> 模板匹配 -> 槽位改写 -> 标题输出`

不推荐链路：

`内容 -> 分类 -> 自由生成标题`

---

## 安装方式

### 方式一：`git clone`

适合本地 Agent、Codex、Claude Code、Cursor 等环境。

```bash
git clone <https://github.com/Coreycore123/cryskill-title-matching/tree/main>
```

然后让你的 Agent 从以下文件开始读取：

- `SKILL.md`
- `rules.md`
- `references/reference_templates.md`

### 方式二：`raw` 链接

适合支持 URL 读取规则文件或 Prompt 文件的环境。

可按需读取：

- `SKILL.md`
- `rules.md`
- `output_schema.md`
- `references/reference_templates.md`

---

## 输出特点

每次调用默认输出：

- 主类
- 主方法
- 辅类
- 命中信号
- 被排除候选
- 最佳模板
- 槽位映射
- 多条标题候选

并对每条标题检查：

- 是否过 21 字
- 是否存在标题党风险
- 是否和主方法一致

---

## 版本管理

当前版本：

- `0.1.0`

建议更新规则：

- `major`：分类树、输出结构、母版调用方式发生重大变化
- `minor`：新增方法卡、新增模板、新增 reference 类型
- `patch`：修正文案、修正边界说明、补样本

版本号写在：

- `SKILL.md` frontmatter

---

## 适合谁

适合：

- 内容团队
- 品牌团队
- 个人 IP
- 咨询顾问
- 需要把“标题能力”结构化的人

尤其适合：

- 有大量高数据标题要复盘的人
- 想把标题经验沉淀成可复用系统的人

---

## 一句话理解

这不是一个“帮你随手写标题”的 Prompt。

它是一套：

`把内容匹配到最合适标题机制，再借强样本模板稳定产出标题的技能系统。`
