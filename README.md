# Operating protocol

A protocol for how an AI agent answers in chat: the answer first, one matter per turn, no invented names, and a short menu of next steps instead of a wall of text. It exists so that the person keeps steering the conversation instead of reading padding.

The protocol is one file, in three languages:

- [operating-protocol.md](operating-protocol.md) - English
- [operating-protocol-uk.md](operating-protocol-uk.md) - Ukrainian / українська
- [operating-protocol-es.md](operating-protocol-es.md) - Spanish / español

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

Each translation is a full replacement, not an addition: use one language, so the agent reads one copy of each rule.

The Breach signal is the part people skip. A single `x` as a reply means the protocol was breached and the answer is to be corrected, not explained. It only works if the agent has the protocol in context, so keep it in a file the agent reloads, not in a message from an hour ago.

## Vocabulary

Rule 9 forbids coining a label, which only works when there is an agreed list of words to use instead. For search and content work that list is the SEO glossary: https://github.com/internetyev/seo-glossary - read it before writing, use only the terms in it, and ask before adding one. The glossary also holds a table of rejected terms with the word that replaces each one.

## License

Released under the [Creative Commons Attribution 4.0](LICENSE) license: use, copy and adapt it freely, with attribution.
