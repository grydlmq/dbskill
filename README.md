# dbskill

把说不清的商业、内容与行动问题，变成能继续判断和行动的下一步。

dbskill 由自媒体博主 dontbesilent 创建，全网可搜 `@dontbesilent 聊赚钱`。dontbesilent 累计发布 16152 条推文，dbskill 将其中经过筛选的内容整理为 4176 个知识原子和 26 个 AI Skills。

适用于有真实业务问题的人：创业者、个体经营者、内容创作者、知识付费从业者，以及需要长期记录判断的人。

**最新更新：v2.17.1**

[新手从这里开始](docs/新手入门.md) · [查看全部 Skill](docs/新手入门.md#skill-全目录) · [安装 dbskill](#安装) · [关注作者](https://x.com/dontbesilent)

## 你可以用它做什么

| 你遇到的情况 | dbskill 会帮你做什么 |
|---|---|
| 有一个生意、产品或定价问题 | 拆清交易、客户、交付与风险，判断问题该从哪里解决 |
| 想做内容却不知道从哪里开始 | 判断内容方向，处理开头、标题、共鸣、逻辑与发布排版 |
| 想找对标，却不知道谁值得学 | 过滤噪音，找到能提供有效参照的对象 |
| 知道该做什么，却总是拖着不动 | 分析行动卡点，区分目标、方法和执行上的问题 |
| 有大量旧内容、案例或课件 | 建成可检索、可重组、可继续生长的内容资产工程 |
| 需要长期追踪关键选择 | 保存诊断、回填结果、整理报告，沉淀个人决策记忆 |

## 从第一次提问开始

安装后，第一次使用直接输入：

```text
/dbs 新手入门
```

dbskill 会先了解你的实际情况，一次只问一个问题，再推荐合适的 Skill，并带你完成第一次实际使用。

你也可以直接输入 `/dbs`，补全下面任意一句：

```text
我在做【什么】，现在卡在【哪里】。
我想通过内容获得【什么结果】，但不知道该做什么。
我看到【谁／什么案例】做得很好，想判断自己该不该学。
我知道自己该做【什么】，但一直没开始，因为【什么】。
```

`/dbs` 会先读取当前对话里已有的信息，再把你带到合适的 Skill。需要完整示例、每个 Skill 的说明和组合用法时，阅读 [dbskill 新手入门](docs/新手入门.md)。

已经知道要做什么时，可以直接调用：

```text
/dbs-diagnosis 我做面向宝妈的收纳咨询，客户总觉得贵。我该降价还是换交付？
/dbs-content 我想讲“普通人别急着做个人 IP”，这个选题怎么做？
/dbs-hook 这是我短视频的前 20 秒，帮我优化开头：……
/dbs-benchmark 我想研究做企业服务内容的账号，帮我找对标。
```

## 作者与答疑

作者：[X](https://x.com/dontbesilent) · [小红书](https://xhslink.com/m/637xuspR4iI) · [抖音](https://v.douyin.com/pRUDhpBqOrc/)

如需加入付费答疑群，可扫描下方二维码，或直接打开 [查看答疑群](https://mp.weixin.qq.com/s/V7Dr0-75VYZOLJ6lbT_s0w)。

![付费答疑群二维码](docs/paid-qa-group-qrcode.png)

## 安装

### Codex、Claude Code 与其他支持 Skills 的 Agent

```bash
npx -y skills add dontbesilent2025/dbskill -g --all
```

### Claude Code 插件市场

```bash
claude plugin marketplace add dontbesilent2025/dbskill
claude plugin install dbs@dontbesilent-skills
```

![Claude Code 插件安装演示](demo.gif)

本地构建时运行：

```bash
bash tools/build-skills.sh
```

产物位于 `dist/skills/`。构建脚本会跳过名称带 `beta` 的本地试验 Skill。

## 常用路径

先按自己要推进的事情选择路径。实际使用中，后续步骤会根据前一步的结论调整。

### 判断一个方向值不值得做

```text
/dbs-diagnosis → /dbs-benchmark → /dbs-decision → /dbs-save
```

诊断方向和商业模式，寻找能提供现实参照的对标，将判断和结果长期回填，再保存阶段结论。

### 从零开始做内容

```text
/dbs → /dbs-content → /dbs-hook → /dbs-xhs-title → /dbs-script-flow
```

先说清业务、受众和目标；确认内容方向；处理开头、标题和逐字稿衔接。

### 写完内容到发布

```text
/dbs-resonate → /dbs-script-flow → /dbs-ai-check → /dbs-wechat-html
```

检查内容是否击中人、逻辑是否连贯、文字是否有明显 AI 痕迹，最后生成微信公众号排版 HTML。

### 知道该做却一直做不动

```text
/dbs-action → /dbs-goal 或 /dbs-diagnosis → /dbs-slowisfast
```

先找到行动受阻的具体信号；再检查目标或方向；最后判断哪些摩擦值得长期承担。

### 把旧内容变成资产

```text
/dbs-content-system → /dbs-content → /dbs-decision
```

将文稿、推文、选题、案例和课程稿搭成内容工程，再继续生产内容并记录关键判断。

完整路径与每一步的输入示例见 [新手入门教程](docs/新手入门.md#常用组合路径)。

## 直接调用的 Skill

dbskill 当前正式发布 26 个 Skill。下面按用户目标列出入口；每个 Skill 的适用时机、输入示例、预期产出与衔接关系见 [完整 Skill 手册](docs/新手入门.md#skill-全目录)。

| 目标 | 直接调用 |
|---|---|
| 不知道从哪里开始，或完成一轮工作后找下一步 | `/dbs` |
| 判断生意、产品、定价或客户 | `/dbs-diagnosis` |
| 找值得研究的对标 | `/dbs-benchmark` |
| 诊断内容方向与做法 | `/dbs-content` |
| 优化短视频开头、标题、文稿共鸣或逻辑 | `/dbs-hook`、`/dbs-xhs-title`、`/dbs-resonate`、`/dbs-script-flow` |
| 分析内容为什么传播、检查 AI 写作痕迹 | `/dbs-spread`、`/dbs-ai-check` |
| 生成微信公众号 HTML | `/dbs-wechat-html` |
| 拆概念、审计目标、把问题写清楚 | `/dbs-deconstruct`、`/dbs-goal`、`/dbs-good-question` |
| 处理拖延、贪快和行动受阻 | `/dbs-action`、`/dbs-slowisfast` |
| 持续学习、决策回填与项目记忆 | `/dbs-learning`、`/dbs-decision`、`/dbs-save`、`/dbs-restore`、`/dbs-report` |
| 把大量素材搭成内容资产工程 | `/dbs-content-system` |
| 多视角讨论或奥派经济学讨论 | `/dbs-chatroom`、`/dbs-chatroom-austrian` |
| 整理或桥接多端 Agent 工作台 | `/dbs-agent-migration`、`/dbs-bridge` |

## 知识库

项目公开了 4,176 条结构化知识原子、按 Skill 整理的方法论知识包和高频概念词典。你可以安装整套 Skill，也可以单独取用其中一部分。

- 想了解字段、主题和数据范围，阅读 [原子库说明](知识库/原子库/README.md)。
- 想做 RAG，将 `知识库/原子库/atoms.jsonl` 导入向量数据库。
- 想给自己的 AI 加商业诊断能力，使用 `知识库/Skill知识包/diagnosis_公理与诊断框架.md` 作为系统提示词背景。
- 想看方法论文档，浏览 [Skill 知识包](知识库/Skill知识包)。

![Skill 联动图](docs/skill-link-map.svg)

## 进阶使用

### 存档、接续与报告

对话关闭后，当前上下文不会自动保留。需要跨对话继续时：

```text
/dbs-save 训练营定价判断
/dbs-restore
/dbs-report
```

存档默认位于 `~/.dbs/sessions/{项目名}/`，报告默认位于 `~/.dbs/reports/{项目名}/`。完整规则见 [新手入门中的状态管理说明](docs/新手入门.md#行动学习与长期记录)。

### 多端使用

`/dbs-agent-migration` 可以审计并整理 Claude Code、Codex、Grok 与通用 Agents 的规则文件和 Skill 真源。`/dbs-bridge` 可将一个 Skill 或整个 `skills/` 目录桥接到这些 Agent。

## 更新

### Claude Code 插件市场安装

```bash
claude plugin marketplace update dontbesilent-skills
claude plugin update dbs@dontbesilent-skills
/reload-plugins
```

### 通过 `npx skills add` 安装

重新运行安装命令：

```bash
npx -y skills add dontbesilent2025/dbskill -g --all
```

版本变更见 [GitHub Releases](https://github.com/dontbesilent2025/dbskill/releases)。当前版本：`v2.17.1`。

## 许可证

本项目采用 [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) 许可证。

- 个人使用、学习、研究、非商业项目：不需要署名，不需要申请。
- 公开发布衍生作品（文章、工具、课程等）：请注明来源。
- 商业用途：需要单独授权，请联系作者。
