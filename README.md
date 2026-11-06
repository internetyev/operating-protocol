# Operating protocol

A protocol for how an AI agent answers in chat: the answer first, one matter per turn, no invented names, and a short menu of next steps instead of a wall of text. It exists so that the person keeps steering the conversation instead of reading padding.

The protocol is one file, in three languages:

- [operating-protocol.md](operating-protocol.md) - English
- [operating-protocol-uk.md](operating-protocol-uk.md) - Ukrainian / українська
- [operating-protocol-es.md](operating-protocol-es.md) - Spanish / español

Two shortened variants exist for the ChatGPT custom instructions field, which takes about 5000 characters. Each drops the Principles section (it repeats the Overview) and folds four Overview items into the rules that already state them. Every rule keeps its full wording.

- [operating-protocol-chatgpt.md](operating-protocol-chatgpt.md) - English, 4083 characters (the full file is 5221)
- [operating-protocol-uk-chatgpt.md](operating-protocol-uk-chatgpt.md) - Ukrainian, 4735 characters (the full file is 6292)

## Origin

The foundation is the DEJAN Chat Protocol by Dan Petrovic, published at https://dejan.ai/blog/introducing-dejan-chat-protocol/. His text supplied the overview, the principles, the first eight rules and the breach signal.

This repository builds on it:

- rule 3 is rewritten as "one matter per turn", so a reply closes one question and offers the rest as options;
- rule 9, "never coin a label", is new: name a thing only by words already used for it, and propose a short name once before using it;
- the protocol is translated into Ukrainian and Spanish, each a full replacement rather than a word-for-word rendering;
- shortened English and Ukrainian variants fit the ChatGPT custom instructions field.

## Why

Left to themselves, agents answer long. A question gets three paragraphs of setup before the fact, every option at once instead of the next decision, and a new word invented for a thing that already had a name. Each of those costs the reader time and the author a correction.

The protocol removes the three habits by naming them: lead with the answer, fork on the next real decision instead of dumping all of them, and never coin a label. Loading it at the start of a session changes the default, so it does not have to be re-asked for every turn.

## What is inside

| Section | Content |
|---|---|
| Overview | the eight working habits, with what each one forbids in practice |
| Principles | the same habits in one line each, for a quick re-read |
| Rules | nine numbered rules, the operative part: answer sentence first, a question is literal, one matter per turn, fork instead of dump, no filler, verify before asserting, format for the medium, stay in scope, never coin a label |
| Breach signal | what the single reply "x" means and what to do about it |

## How to use it

Copy the contents of the protocol file into the file your agent reads at the start of every session:

| Agent | File |
|---|---|
| Claude Code | `AGENTS.md` or `CLAUDE.md` in the project root; `~/.claude/CLAUDE.md` to apply it to every project |
| OpenAI Codex | `AGENTS.md` |
| Gemini CLI | `GEMINI.md` |
| Cursor | a file under `.cursor/rules/` |
| A chat assistant with custom instructions | the custom instructions or system prompt field |
| ChatGPT | the custom instructions field, which holds about 5000 characters; use `operating-protocol-chatgpt.md` or `operating-protocol-uk-chatgpt.md` |

Each translation is a full replacement, not an addition: use one language, so the agent reads one copy of each rule.

The Breach signal is the part people skip. A single `x` as a reply means the protocol was breached and the answer is to be corrected, not explained. It only works if the agent has the protocol in context, so keep it in a file the agent reloads, not in a message from an hour ago.

## Vocabulary

Rule 9 forbids coining a label, which only works when there is an agreed list of words to use instead. For search and content work that list is the SEO glossary: https://github.com/internetyev/seo-glossary - read it before writing, use only the terms in it, and ask before adding one. The glossary also holds a table of rejected terms with the word that replaces each one.

## License

Released under the [Creative Commons Attribution 4.0](LICENSE) license: use, copy and adapt it freely, with attribution.

## Author

Andriy Terentyev, SEO consultant: https://terentyev.net

In SEO for over 15 years in-house and as a consultant. SEO Strategy Advisor at KyivIndependent.com, former SEO Lead at Kiwi.com, and before that COO, CTO and CEO in tech startups. Niches: travel, news, SaaS and ecommerce.

For the last three years I have worked solo, doing the work of a full SEO team with my proprietary SEO tools ([corgiseo.com](https://corgiseo.com)) and a set of AI agents. This protocol is the set of rules those agents answer by. What I take on: technical SEO of large sites, SEO automation and QA monitoring, AI-assisted content pipelines, SEO data harvesting and competitive intelligence, and custom LLM and skill setups for SEO and SEM tasks.

Pet project: https://corgiseo.com, an SEO data layer for AI agents.

LinkedIn: https://linkedin.com/in/terentyev
