---
name: handoff
description: Compact the current conversation into a handoff document so a fresh chat can pick up the work exactly where this one stopped. Use when the user types /handoff or wants to continue this work in a new chat.
---

<!-- Adapted from Matt Pocock's "handoff" skill (github.com/mattpocock/skills), MIT License. See LICENSE.txt. -->

Write a handoff document summarising the current conversation so a fresh chat can continue the work.

Structure it as:

1. **Goal** - what we are trying to achieve, in one or two lines.
2. **Where we are** - what is done, what is decided, and why.
3. **Open threads** - what is still undecided or unfinished, in order of priority.
4. **Next step** - the very first thing the next chat should do.
5. **Key context** - facts, constraints and preferences the next chat must not have to ask for again.

Do not duplicate content that already lives in other artifacts, such as files, documents, specs or links. Reference them by name, path or URL instead.

Redact sensitive information: API keys, passwords, personal details.

If the user passed arguments, treat them as a description of what the next chat will focus on and tailor the document to it.

Delivery:
- If you can write files, as in Claude Code, save it as `handoff.md` in the system temp directory and tell the user the path.
- Otherwise, output the whole document in one copyable block, and tell the user: paste this as the first message of a new chat.
