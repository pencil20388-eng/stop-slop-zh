# 🚫 Stop Slop 中文版 — 干掉 AI 味，写出人话

> ### ❌ Before
> 在当今数字化转型的时代，随着技术的不断进步，越来越多的企业开始关注自动化工具的应用。值得注意的是，这一趋势不仅仅是技术层面的变化，更是企业运营范式的根本性转变。综上所述，自动化已经成为不可忽视的战略方向。
>
> ### ✅ After
> 上周跟一个 200 人的电商团队聊，他们把客服响应从 4 小时压到了 11 分钟。不是加人，是把 80% 的重复问题交给了自动化。坦率的讲，这个转变的速度，很多团队还没反应过来。

[English](#english) | **中文**

> AI 中文写作有固定套路：废话连接词、教科书结构、播音腔句式。这个 skill 教 AI 识别并消除这些痕迹，让输出读起来像一个有判断力的人在认真聊，而不是机器在输出信息。

灵感来自 [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop)（英文版，4k+ stars）。中文 AI 写作有完全不同的"AI 味"特征，所以需要一套独立的规则。

## 这个 skill 做什么

装上之后，你的 AI 写出来的中文会：

- ❌ 不再用「综上所述」「值得注意的是」「在当今...的时代」
- ❌ 不再用冒号、破折号、双引号这些 AI 最爱的标点
- ❌ 不再用「第一、第二、第三」「首先...其次...最后」这种编号体
- ❌ 不再编造「某团队跟我们聊过」这种假案例
- ✅ 用口语化表达：「说真的」「坦率的讲」「踩过坑」「太离谱了」
- ✅ 用散文式结构，自然过渡，长短句交替
- ✅ 每个观点有具体数据/场景/人物支撑
- ✅ 写完自动跑四层质检，输出质检报告

## 文件结构

```
stop-slop-zh/
├── SKILL.md                    # 核心指令（装这个就够了）
├── references/
│   ├── banned-words.md         # 禁用词完整清单
│   ├── banned-punctuation.md   # 禁用标点规则
│   ├── banned-structures.md    # 禁用结构模式
│   ├── recommended-phrases.md  # 推荐口语化词组库
│   └── examples.md             # 改前/改后对照
├── README.md
└── LICENSE
```

## 安装

### Claude Code

```bash
mkdir -p .claude/skills
git clone https://github.com/pencil20388-eng/stop-slop-zh.git .claude/skills/stop-slop-zh
```

### Claude Projects

上传 `SKILL.md` 和 `references/` 文件夹到项目知识库。

### 自定义指令 / System Prompt

把 `SKILL.md` 的内容复制到你的 system prompt 里。references 文件按需加载。

### 其他 AI 工具（Cursor、Codex CLI、Gemini CLI）

把 `stop-slop-zh/` 文件夹复制到对应工具的 skills 目录。

## 使用

装好之后直接用自然语言：

```
> 帮我写一篇关于 XX 的文章

> 检查这段文字的 AI 味，帮我改掉

> 用 stop-slop-zh 的规则重写这段话

> 跑一遍四层质检，给我质检报告
```

## 这个 skill 和英文版 stop-slop 的区别

| | stop-slop（英文） | stop-slop-zh（中文） |
|---|---|---|
| 禁用词 | adverbs, throat-clearing, business jargon | 「综上所述」「值得注意的是」「本质上」等 |
| 禁用结构 | binary contrasts, dramatic fragmentation | 编号体、bullet point 罗列、大量加粗 |
| 标点规则 | 无特殊规则 | 禁用冒号、破折号、双引号 |
| 替代方案 | active voice, specifics | 口语化词组库（50+ 个推荐表达） |
| 质检体系 | 5 维度评分 | 四层自检（硬性规则→风格→内容→活人感） |
| 写作结构 | 无 | 完整的文章结构框架 |

## Credits

- 中文规则体系来自实战内容运营 SOP
- 英文版灵感来自 [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop)

## License

[MIT](LICENSE)

---
## 相关讨论

- 📌 [hardikpandya/stop-slop Discussion](https://github.com/hardikpandya/stop-slop) — 英文原版作者仓库，本项目的灵感来源
- 📌 [Leonxlnx/taste-skill Issue](https://github.com/Leonxlnx/taste-skill/issues) — 在 taste-skill（21k stars）中讨论中文 AI 写作模式
- 📌 [anthropics/knowledge-work-plugins Issue](https://github.com/anthropics/knowledge-work-plugins/issues) — 向 Anthropic 官方提议加入中文内容质检能力
- 

**⭐ 如果你也受不了 AI 中文写作的「AI 味」，给个 Star 吧。**

---

<a name="english"></a>

## English

**Stop Slop ZH** — A Claude Code skill that removes AI writing patterns from **Chinese** prose.

Chinese AI writing has its own distinct "AI smell": formulaic connectors, textbook structures, newsreader-style phrasing. This skill teaches AI to catch and eliminate these patterns, producing Chinese text that reads like a knowledgeable human having a real conversation.

Inspired by [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop) (English, 4k+ stars). Chinese AI writing has completely different telltale patterns, requiring an independent rule set.

### Install (Claude Code)

```bash
mkdir -p .claude/skills
git clone https://github.com/pencil20388-eng/stop-slop-zh.git .claude/skills/stop-slop-zh
```

### What it does

- Bans 30+ Chinese filler phrases (「综上所述」「值得注意的是」etc.)
- Bans AI-favored punctuation (colons, em-dashes, double quotes)
- Replaces numbered lists with natural prose transitions
- Injects 50+ colloquial Chinese expressions for authenticity
- Runs a 4-layer quality check: hard rules → style → content → human-feel
- Outputs a structured QA report after every piece

Compatible with Claude Code, Cursor, Codex CLI, Gemini CLI, and any agent supporting SKILL.md.
