<!-- section:intro -->
AI 正在改变数学建模比赛。过去半年，GitHub 上名称或描述含“数学建模”的新仓库就有 1600 多个，从一键出论文的 Agent，到只管选题的小 skill，质量参差不齐。同时，美赛、国赛、华为杯都出台了 AI 使用规定：可以用，但必须如实声明。

这份清单把能用、仍在维护的项目按用途整理好，并把各赛事的 AI 规定放在最前面，用之前先弄清楚边界。

<!-- section:rules -->
## 先看规则：比赛允许怎么用 AI

| 赛事 | 能不能用 | 必须交什么 | 不合规会怎样 |
|---|---|---|---|
| 美赛 MCM/ICM（[COMAP 政策](https://www.contest.comap.com/undergraduate/contests/mcm/flyer/Contest_AI_Policy.pdf)，2025 版） | 允许负责任地使用，解题不要求用 AI | 正文中标注、参考文献列出；25 页正文之后附 **Report on Use of AI Tools**（不计入页数），生成式 AI 要写出提问和完整回答 | COMAP 发现未披露的使用会采取相应处理 |
| 国赛 CUMCM（[2026 年试行规定](https://www.mcm.edu.cn/html_cn/node/fef94648f2836ab6cc81586f4c38512b.html)，2026 年 9 月 1 日起试行） | 可以用，但不要求必须用；核心建模与分析由参赛队主导，AI 参与完成的内容要逐项人工审查、核实 | 论文参考文献之前写 **AI 工具使用声明**：用了 AI 写明主要用途，没用写“本参赛队在竞赛过程中未使用任何AI工具”。用了 AI 的在支撑材料里附 **《AI工具使用详情.pdf》**（工具名称和版本、使用目的和环节、主要提示方式和使用过程、对 AI 输出的采纳、人工修改和核验情况） | 视情节轻重处理；故意隐瞒、虚假声明，或把未经人工审查核实的 AI 内容直接当作核心建模与分析成果提交的，取消评奖资格 |
| 华为杯研赛（[2025 年规定](https://yjsb.zjnu.edu.cn/_upload/article/files/75/fc/43236cdd4cbfa29c3ed8006080e8/359fe3e7-2758-402c-b25d-b5a6868c5437.pdf)） | 可作辅助手段，不能替代独立思考和核心创新 | 最终文字用参赛队自己的语言表述；来源无法确认的 AI“模型”“公式”不予认可；AI 参与的数据分析结果和程序要注明工具名称、版本、开发机构和日期 | 取消评奖资格 |

> [!IMPORTANT]
> 规定每年可能调整，赛前以当届官方通知为准。国赛规定链接的是竞赛官网原文，华为杯规定链接的是高校研究生院转发的原文。

2026 年 11 月，国赛组委会发布了[部分参赛作品相似度较高的通报](https://www.mcm.edu.cn/html_cn/node/74c9193dcdfd44d026d2c3bf5f93695c.html)，具体情况见通报附件。很多队伍用同一个热门 skill 或同一套提示词时，思路和行文容易趋同，这也是本清单把“人机协作”类工具标出来的原因：关键判断留给自己。

<!-- section:pick -->
## 怎么挑

| 你的情况 | 可以先看 |
|---|---|
| 第一次参赛，想真正学会建模 | [shumo-expert](https://github.com/XiucuiGuan/shumo-expert)（只引导、不代写）、[intro-mathmodel](https://github.com/datawhalechina/intro-mathmodel)、[MathModel](https://github.com/zhanwen/MathModel) |
| 国赛队伍，想让 AI 当助手、自己拿主意 | [mathmodel-skill](https://github.com/handsomeZR-netizen/mathmodel-skill)、[modeling-workbench](https://github.com/Lucasuiii/modeling-workbench)、[cumcm-step-review](https://github.com/yuanchen-home/cumcm-step-review) |
| 美赛，要写英文论文 | [LLM-MM-Agent](https://github.com/usail-hkust/LLM-MM-Agent) 的技能包、[mathodology](https://github.com/sweetcornna/mathodology)、[LaTeX-in-ICM-MCM](https://github.com/QTH1225/LaTeX-in-ICM-MCM) 模板 |
| 不想配环境，要装好就能用的软件 | [MathModelAgent](https://github.com/jihe520/MathModelAgent) 桌面版、[HaJiMi](https://github.com/yjz211/HaJiMi-Math-Model-Agent)、[Remit](https://github.com/zhou2030109-glitch/Remit) |
| 华为杯研赛 | [Huaweibei-cool](https://github.com/siyunhao2025-beep/Huaweibei-cool)、[hwb-math-modeling-skills](https://github.com/xieyouxixi/hwb-math-modeling-skills)、[GMCMthesis](https://github.com/latexstudio/GMCMthesis) |
| 卡在选题或选模型 | [route-selection](https://github.com/y3519712124-ui/math-modeling-contest-route-selection)、[cumcm-taste](https://github.com/bydtesla1609/cumcm-taste) |
| 交卷前查漏 | [bzd-math-modeling-skills](https://github.com/BZDmathclub/bzd-math-modeling-skills)、[mathematical-modeling-review](https://github.com/landawang-star/mathematical-modeling-review)，再用 [CUMCM-AI-Usage-Report](https://github.com/EmpyreanHYR/CUMCM-AI-Usage-Report) 写 AI 使用详情 |
| 赛后想发论文 | [math-modeling-to-sci-skill](https://github.com/siyunhao2025-beep/math-modeling-to-sci-skill) |

这张表依据各项目 README 整理，没有逐个实测。

<!-- section:faq -->
## 常见问题

**skill 怎么装？**
多数项目是标准 SKILL.md 格式。Claude Code 放进 `~/.claude/skills/`（全局）或项目里的 `.claude/skills/`，Codex 放进 `~/.codex/skills/`，也可以用 `npx skills add 作者/仓库名`。各工具路径不同，以项目 README 的安装说明为准。

**用了 AI 要声明吗？**
要。三个赛事都要求写明用了什么工具、用在哪里，见上方[规则](#rules)。

**全自动 skill 跑出来的论文能直接交吗？**
不建议。国赛要求核心建模与分析由参赛队主导，没经过人工审查核实就把 AI 内容当作核心成果提交会被取消评奖资格；华为杯要求最终文字用参赛队自己的语言表述。全自动工具更适合赛前练习和对照思路，比赛里把关键判断留给自己。

**会收录“降 AI 率”工具吗？**
不收录以降 AI 率、躲避 AIGC 检测为主要卖点的项目。比赛要求的是如实披露。

**星标数多久更新一次？**
每周一由 GitHub Actions 自动刷新并重新排序，链接每周检查一次。

<!-- section:finder -->
## 让 Agent 帮你挑

这份清单也是一个 skill。把仓库里的 [`skills/math-modeling-finder`](skills/math-modeling-finder) 文件夹装进你的 agent（或运行 `npx skills add DU8866-nice/awesome-math-modeling`），然后问它：

> 我们是国赛三人队，用 Codex，想要人机协作的 skill，装哪个？

它会按你的赛事、所用工具和想要的 AI 参与程度，从清单里挑两三个并说明理由，同时提醒当届的 AI 使用规定。

<!-- section:contributing -->
## 参与贡献

欢迎推荐项目或纠错：[提交 Issue](https://github.com/DU8866-nice/awesome-math-modeling/issues/new/choose)，或者修改 [`data/tools.yaml`](data/tools.yaml) 后提 PR，详见[贡献指南](CONTRIBUTING.md)。README 由脚本生成，请不要直接改它。
