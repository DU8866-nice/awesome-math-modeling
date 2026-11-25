<!-- section:intro -->
AI is changing modeling contests. In the last six months alone, more than 1,600 new GitHub repositories mention 数学建模 (mathematical modeling) in their name or description, from agents that write a whole paper to small skills that only help pick a problem, and quality varies a lot. Meanwhile MCM/ICM, CUMCM and the Huawei Cup have all published AI rules: you may use AI, but you must disclose it.

This list sorts the projects that work and are still maintained by what they do, and puts the contest rules first so you know the limits before you start.

<!-- section:rules -->
## Read the rules first: AI use in contests

| Contest | Allowed? | What you must submit | If you don't comply |
|---|---|---|---|
| MCM/ICM ([COMAP policy](https://www.contest.comap.com/undergraduate/contests/mcm/flyer/Contest_AI_Policy.pdf), 2025) | Responsible use is permitted; the problems don't require AI | Cite AI use in the text and references, and append a **Report on Use of AI Tools** after the 25-page solution (it doesn't count toward the limit); for generative AI, include the queries and full outputs | COMAP takes action when it finds undisclosed use |
| CUMCM ([2026 trial rules](https://www.mcm.edu.cn/html_cn/node/fef94648f2836ab6cc81586f4c38512b.html), in Chinese, in force from September 1, 2026) | Allowed but not required; the team must lead the core modeling and analysis and check everything AI contributed, item by item | An **AI tool use statement** before the references: the main purposes if you used AI, or "本参赛队在竞赛过程中未使用任何AI工具" (we used no AI tools) if you didn't. Teams that used AI add **AI工具使用详情.pdf** (AI tool usage details) to the supporting materials, with each tool's name and version, purpose and stage, how it was prompted and used, and what was kept, edited and verified | Handled by severity; hiding AI use, a false statement, or submitting unchecked AI output as the core modeling and analysis means disqualification from awards |
| Huawei Cup graduate contest ([2025 rules](https://yjsb.zjnu.edu.cn/_upload/article/files/75/fc/43236cdd4cbfa29c3ed8006080e8/359fe3e7-2758-402c-b25d-b5a6868c5437.pdf), in Chinese) | As an aid only, never in place of the team's own thinking and core ideas | Final text in the team's own words; AI "models" and "formulas" without a verifiable source are not accepted; label AI-assisted data analysis and code with the tool's name, version, developer and date | Disqualified from awards |

> [!IMPORTANT]
> Rules change from year to year, so check the current year's official notice. The CUMCM link points to the official contest site; the Huawei Cup link points to a copy reposted by a university graduate school.

In November 2026 the CUMCM committee published [a notice about contest papers with high similarity](https://www.mcm.edu.cn/html_cn/node/74c9193dcdfd44d026d2c3bf5f93695c.html); the details are in its attachments. When many teams use the same popular skill or the same prompts, ideas and wording tend to converge, which is one reason this list labels human-in-the-loop tools: keep the key decisions your own.

<!-- section:pick -->
## Where to start

| Your situation | Start with |
|---|---|
| First contest, and you want to learn modeling | [shumo-expert](https://github.com/XiucuiGuan/shumo-expert) (tutor, won't do the work), [intro-mathmodel](https://github.com/datawhalechina/intro-mathmodel), [MathModel](https://github.com/zhanwen/MathModel) |
| CUMCM team that wants AI as an assistant | [mathmodel-skill](https://github.com/handsomeZR-netizen/mathmodel-skill), [modeling-workbench](https://github.com/Lucasuiii/modeling-workbench), [cumcm-step-review](https://github.com/yuanchen-home/cumcm-step-review) |
| MCM/ICM, writing in English | the skill pack in [LLM-MM-Agent](https://github.com/usail-hkust/LLM-MM-Agent), [mathodology](https://github.com/sweetcornna/mathodology), the [LaTeX-in-ICM-MCM](https://github.com/QTH1225/LaTeX-in-ICM-MCM) template |
| No setup, just an app | [MathModelAgent](https://github.com/jihe520/MathModelAgent) desktop, [HaJiMi](https://github.com/yjz211/HaJiMi-Math-Model-Agent), [Remit](https://github.com/zhou2030109-glitch/Remit) |
| Huawei Cup | [Huaweibei-cool](https://github.com/siyunhao2025-beep/Huaweibei-cool), [hwb-math-modeling-skills](https://github.com/xieyouxixi/hwb-math-modeling-skills), [GMCMthesis](https://github.com/latexstudio/GMCMthesis) |
| Stuck choosing a problem or a model | [route-selection](https://github.com/y3519712124-ui/math-modeling-contest-route-selection), [cumcm-taste](https://github.com/bydtesla1609/cumcm-taste) |
| Final checks before submitting | [bzd-math-modeling-skills](https://github.com/BZDmathclub/bzd-math-modeling-skills), [mathematical-modeling-review](https://github.com/landawang-star/mathematical-modeling-review), then [CUMCM-AI-Usage-Report](https://github.com/EmpyreanHYR/CUMCM-AI-Usage-Report) for the AI-use report |
| Turning a contest paper into a journal paper | [math-modeling-to-sci-skill](https://github.com/siyunhao2025-beep/math-modeling-to-sci-skill) |

This table is based on each project's README; the tools were not tested one by one.

<!-- section:faq -->
## FAQ

**How do I install a skill?**
Most projects use the standard SKILL.md format. For Claude Code, put the folder in `~/.claude/skills/` (global) or `.claude/skills/` in your project; for Codex, `~/.codex/skills/`; or run `npx skills add owner/repo`. Paths differ between tools, so follow each project's README.

**Do I have to disclose AI use?**
Yes. All three contests require you to state which tools you used and where. See [the rules](#rules).

**Can I submit a paper an autopilot skill wrote?**
Not a good idea. CUMCM requires the team to lead the core modeling and analysis, and submitting unchecked AI output as the core work means disqualification; the Huawei Cup requires the final text in the team's own words. Autopilot tools are better for practice and for comparing ideas before the contest.

**Do you list tools that lower AI-detection scores?**
No. Projects whose main pitch is beating AIGC detection are not listed. The contests ask for honest disclosure.

**How often are stars updated?**
Every Monday GitHub Actions refreshes the stars and re-sorts the list, and links are checked weekly.

<!-- section:finder -->
## Let your agent pick

This list is also a skill. Install the [`skills/math-modeling-finder`](skills/math-modeling-finder) folder in your agent (or run `npx skills add DU8866-nice/awesome-math-modeling`) and ask:

> We're a three-person MCM team using Claude Code and want a human-in-the-loop skill. Which one should we install?

It picks two or three entries for your contest, your tool and how much you want the AI to do, explains why, and reminds you of the contest's AI rules.

<!-- section:contributing -->
## Contributing

Suggestions and corrections are welcome: [open an issue](https://github.com/DU8866-nice/awesome-math-modeling/issues/new/choose), or edit [`data/tools.yaml`](data/tools.yaml) and send a PR. See the [contributing guide](CONTRIBUTING.md). The README is generated by a script, so please don't edit it directly.
