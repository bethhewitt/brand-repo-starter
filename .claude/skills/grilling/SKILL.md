---
name: grilling
description: Grill the user relentlessly about a plan, decision, or idea. Use when the user wants to stress-test their thinking, or uses any 'grill' trigger phrases.
---

Interview the user relentlessly until you reach a shared understanding. Map this as a **design tree**: every decision branches into the decisions that hang off it.

The **frontier** is every decision whose prerequisites are already settled: the questions you can ask _now_ without guessing at answers you haven't heard yet. Track the whole frontier yourself, but **ask one question at a time**. Each turn, pick the single most foundational question on the frontier (the one that unblocks the most downstream decisions), ask it, and wait for the answer before asking the next. Never batch several questions into one message.

**Ask every question with the AskUserQuestion tool** so the user can pick an answer instead of typing one out:

- One question per call.
- 2-4 distinct, concrete options. Put your recommended answer first and add "(Recommended)" to its label.
- Put the reasoning for each option in its `description`. Use `preview` when a snippet or mockup would help compare options.
- Keep `header` to a short chip label (max 12 chars).
- Don't add an "Other" option. The tool provides one for free-text answers, which covers open questions (personal anecdotes, names, facts only the user knows). Still offer your best guesses as options for those.

In the message around the tool call, keep context brief: at most a line on why this question matters now. Don't repeat the options in prose.

If the user declines a question or says it belongs somewhere else, take that as a decision about scope. Drop that branch and everything that depended on it from the tree, and don't ask it again in another form.

Each answer reshapes the tree: settled decisions push the frontier outward and unblock questions that depended on them. Recompute the frontier and ask the next question. Never ask a question whose answer depends on one that's still open.

Finding _facts_ is your job, never the user's. When a frontier question needs a fact from the environment (filesystem, tools, etc.), dispatch a sub-agent to find it; don't ask the user for anything you could look up yourself. Don't block on it: a running exploration is an unsettled prerequisite, so only the questions downstream of it wait for the sub-agent to report; keep asking the rest of the frontier meanwhile. The _decisions_ are the user's: put each to them and wait.

The session is done when the frontier is empty: every branch of the design tree visited, nothing left silently assumed. Before acting on it, summarise every decision reached and confirm with the user that you have a shared understanding.

Adapted from Matt Pocock's [grill-me skill](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me), used under the MIT License (see `LICENSE` in this folder).
