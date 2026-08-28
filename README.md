# Second Brain Curator

> Preserve the source. Develop your own thinking. Connect the cards.

Second Brain Curator is an open Codex Skill for turning messy inbox material into reviewable knowledge cards.

It accepts reading highlights, annotations, quick thoughts, and chat messages; keeps the original material untouched; asks questions that help clarify your own view; creates candidate cards; and proposes meaningful links to cards you already have.

## 中文简介

Second Brain Curator 是一个开源 Codex Skill，用来把散乱的 Inbox、读书笔记、批注和聊天想法整理成可审核、可连接的知识卡片。

它不会直接改写原始资料，而是把原料库与卡片库分开：先完整保存来源，再识别哪些是原文、哪些是你自己的看法；随后通过 AI 追问帮助你澄清观点、产生候选卡片，并寻找卡片之间真正有意义的联系。所有候选卡片都需要你明确确认后，才能进入正式知识库。

安装时可以直接对 Codex 说：

```text
请从这个仓库安装 second-brain-curator Skill：
https://github.com/shidifenjin/second-brain-curator
```

## Why this exists

Most review tools resurface highlights. Highlights are useful, but they are not yet your knowledge.

This Skill follows a different loop:

```text
Inbox source
    ↓ preserve unchanged
Raw archive
    ↓ distinguish quote from personal view
Candidate card
    ↓ question, revise, connect
Approved knowledge card
    ↓ periodic review
New thought or new connection
```

The raw archive and the card vault remain separate. The AI may add new captures and indexes, but it must not rewrite existing source material. A generated card stays in review until you approve it.

## Features

- Immutable raw-source archive
- Deduplication by message ID, URL, or content hash
- Clear separation between quotations and your own annotations
- Atomic candidate cards centered on reusable claims
- AI questions designed to develop, not merely summarize, your thinking
- Proposed semantic links with explicit relationship types and reasons
- Conversation exits such as continue, update, branch, link, stop, or discard
- Safe cursor handling for scheduled inbox processing
- Works with Obsidian folders and can be adapted to Feishu/Lark, Slack, email, or another input channel

## Install

Ask Codex:

```text
Install the second-brain-curator skill from:
https://github.com/shidifenjin/second-brain-curator
```

Or clone/copy this folder into your personal Codex Skills directory and restart Codex so the Skill can be discovered.

## Configure

Copy [`references/local-config.example.md`](references/local-config.example.md) to a private `local-config.md`, then fill in your own paths and input channel.

Never commit `local-config.md`, access tokens, chat IDs, user IDs, or processing-state files. They are ignored by the included `.gitignore`.

Example request:

```text
Use $second-brain-curator to import this reading note. Preserve the complete source, identify which lines are my own thoughts, and create candidate cards for review.
```

## Card lifecycle

```text
captured → candidate → in_review → approved
                             ↘ discarded
```

Approval is intentionally explicit. Automation may prepare, question, and propose; it must not silently promote a draft into permanent knowledge.

## Repository contents

- `SKILL.md` — agent instructions and safety boundaries
- `references/card-schema.md` — portable raw-record and candidate-card schemas
- `references/conversation-workflow.md` — review dialogue and branching behavior
- `references/local-config.example.md` — private configuration template
- `assets/` — Markdown templates that may be copied into a vault

## Philosophy

The inbox is your memory substrate. The cards are your current understanding. The AI is the curator between them.

## License

MIT
