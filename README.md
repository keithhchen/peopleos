# PeopleOS

A personal relationship management and networking advisor that runs in your terminal. Supports Claude Code, OpenAI Codex, and OpenClaw.

## Setup

### Claude Code / OpenAI Codex

Clone the repo and run your harness inside it:

```bash
git clone https://github.com/keithhchen/peopleos.git
cd peopleos
```

**Claude Code**
```bash
npm install -g @anthropic-ai/claude-code
claude
```

**OpenAI Codex**
```bash
npm install -g @openai/codex
codex
```

Once the harness is running, send `Hi` to start onboarding.

### OpenClaw

Install and onboard:

```bash
npm install -g openclaw@latest
openclaw onboard --install-daemon
```

Then send this prompt once to activate PeopleOS mode:

> You're about to enter PeopleOS mode for relationship analysis.
>
> 1. `git clone https://github.com/keithhchen/peopleos.git`
> 2. Record in `USER.md`: whenever I mention peopleos, send chat logs, or bring up relationship questions, enter the peopleos directory and work from there.
> 3. Now, activate PeopleOS mode and start onboarding.

## What it does

A thinking partner for the relationships that actually matter — partners, colleagues, clients, friends. Built on one belief: most relationship problems aren't solved by better tactics. They're solved by seeing the situation more clearly.

Lives entirely on your machine. No cloud, no sync, no telemetry.

## User flows

**Onboarding in 5 questions.** Say `Hi`. Five questions cover your background, pressures, conflict style, communication, and goals — your profile gets written to `SOUL.md`. Asked once, ever.

**Just say a name.** New people get a 3-question intake; known people load their full history. Either way, straight into the situation.

**Drop in raw material.** Screenshots, chats, emails, transcripts — paste anything. Transcribed, filed under the right person, grounded in what actually happened.

**Three-layer reading, three reply options.** What happened, what they might be thinking, where you stand — then 2–3 ready-to-send replies with one recommended.

**Memory that grows on its own.** Each conversation updates the right files. No tagging, no maintenance — just talk.

## Why this isn't a Skill

PeopleOS isn't a Claude Code skill, and the difference matters. A skill is a recipe — instructions for how an agent should behave on a task. PeopleOS is something else: a loosely-defined file system on your disk that grows over time. Each person gets a folder. Every screenshot, email, or chat you paste is transcribed and filed. The patterns in how you handle conflict, what you avoid, what you actually want — all written to plain markdown you can read, edit, grep, and version with git.

ChatGPT.com remembers across conversations, but it doesn't build per-person profiles on your machine. The point of PeopleOS isn't to give the agent better instructions. It's to help you store your life — on your own disk.

|  | ChatGPT.com | A Skill | PeopleOS |
| --- | --- | --- | --- |
| Essence | ❌ Chat product | ❌ Behavior recipe | ✅ File system database |
| Where your data lives | ❌ Their cloud | ❌ One-shot | ✅ Your disk, plain markdown |
| Per-person profile | ❌ No | ❌ No | ✅ One folder per person |
| Raw material (chats, emails, screenshots) | ❌ Pasted, not retained | ❌ Pasted, not retained | ✅ Transcribed and filed |

---

# PeopleOS（中文）

终端里的人际关系与人脉顾问。支持 Claude Code、OpenAI Codex、OpenClaw。

## 安装

### Claude Code / OpenAI Codex

克隆仓库，在目录内启动 harness：

```bash
git clone https://github.com/keithhchen/peopleos.git
cd peopleos
```

**Claude Code**
```bash
npm install -g @anthropic-ai/claude-code
claude
```

**OpenAI Codex**
```bash
npm install -g @openai/codex
codex
```

启动后，发送 `你好` 进入 onboarding。

### OpenClaw

安装并初始化：

```bash
npm install -g openclaw@latest
openclaw onboard --install-daemon
```

然后发送一次以下指令激活 PeopleOS 模式：

> 接下来，你将获得 PeopleOS 模式，用于我的人际关系分析。
>
> 1. `git clone https://github.com/keithhchen/peopleos.git`
> 2. 记录到 `USER.md` 中：每当用户提到 peopleos、发送聊天记录、或聊到人际关系问题，请进入 peopleos 目录并工作
> 3. 现在，启动 peopleos 模式并开始 onboarding

## 它是什么

服务于真正在乎的关系——伙伴、同事、客户、朋友——的思考伙伴。我们只相信一件事：人际关系的问题，大多数时候不是靠更好的话术解决的，而是靠把局面看清楚解决的。

完全运行在你的电脑上。无云端、无同步、无埋点。

## 使用方式

**5 个问题，建档完成。** 发送 `你好`，问你的背景、压力、冲突方式、沟通习惯、目标——画像写入 `SOUL.md`。只问这一次。

**说出一个名字。** 陌生人三问建档；熟人直接调出历史。然后立刻进入当前情境。

**粘贴原始材料。** 截图、消息、邮件、记录都可以。自动转写、归档到对应人物——分析建立在真实发生过的内容上。

**三层解读，三个回复。** 发生了什么、对方在想什么、你在哪——给你 2–3 条可直接发送的回复，标注推荐。

**记忆自然生长。** 每次对话自动更新对应文件。无需标签、无需维护——聊，就够了。

## 为什么不做成 Skill

PeopleOS 不是一个 Claude Code skill，这个区别重要。Skill 是一份配方——告诉 agent 在某个任务上应该怎么做。PeopleOS 是另一种东西：一个长在你硬盘上、随时间生长、松散定义的文件系统。每个被你提到的人都有一个文件夹。每张被你贴进来的截图、邮件、对话都被自动转写、归档。你怎么处理冲突、你回避什么、你真正想要什么——都被写到纯 markdown 里，你可以读、可以编辑、可以 grep、可以用 git 管。

ChatGPT.com 跨对话有记忆，但它不会在你的电脑上为每个人建档。PeopleOS 的意义不是让 agent 更聪明，而是帮你把自己的人和事，存在自己的硬盘上。

|  | ChatGPT.com | Skill | PeopleOS |
| --- | --- | --- | --- |
| 本质 | ❌ 聊天产品 | ❌ 行为配方 | ✅ 文件系统数据库 |
| 数据存放在 | ❌ 他们的云端 | ❌ 一次性 | ✅ 你的硬盘，纯 markdown |
| 是否为每个人建档 | ❌ 否 | ❌ 否 | ✅ 一人一文件夹 |
| 原始材料（聊天、邮件、截图） | ❌ 仅粘贴，不保留 | ❌ 仅粘贴，不保留 | ✅ 自动转写、归档 |
