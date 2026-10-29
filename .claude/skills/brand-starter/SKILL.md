---
name: brand-starter
description: Build a brand repo from scratch. Collects the user's existing brand material, interviews them one question at a time, builds the folder of brand files Claude reads before every task, then tests it with brand-check. Use when the user runs /brand-starter, asks to "set up my brand", or wants to carry on an unfinished setup.
---

# Brand starter

Build this folder into a brand repo, starting from nothing. The user is a marketer, not a developer. Use plain language, and don't mention files or folders they don't need to know about.

There are four steps. Before starting, check where things are so a stopped setup can carry on:

- `knowledge/` exists: the repo is built. Ask whether to run the checks (step 4) or start again.
- `sources/interview-notes.md` exists: the interview was started. Read it and carry on from step 2.
- Otherwise, start at step 1.

## 1. Start

- In two or three lines, tell the user what's about to happen: you'll gather what they have, ask some questions, build their brand files, then test them. It takes about 20 to 30 minutes, and they can stop at any point.
- Create a `sources/` folder. Copy `sources/README.md` into it from this skill's `scaffold/` folder.
- Ask for their existing material, all in one message:
  - the brand's name
  - their website address, if they have one
  - any brand guidelines, past posts, emails, decks or logo files. They can drag them into the chat or drop them into `sources/`. Word files, Google Docs and slides work best saved as PDF first.
- Save anything they attach in the chat into `sources/`. If they have nothing, that's fine: the interview will take longer.

## 2. Ask for what's missing

**Read what they gave you.** Read everything in `sources/` except its README, and the main pages of their website (home, about, products or services). In two or three lines, tell the user what you found and what looks thin. Don't list every file.

**Work out what's missing.** Use the outlines in this skill's `scaffold/knowledge/` and `scaffold/brand/identity.md` as the checklist: every heading in them needs an answer. List the gaps (nothing in the material) and conflicts (sources that disagree).

Always ask these as well, because only a person can answer them:

- Who is this brand not for?
- What would you never say, or never want to be mistaken for?
- Which claims can you prove, and how?
- Which past piece is the best example of you, and why?
- What do people usually get wrong when they write or design for you?
- What practical details come up in most content: opening hours, location, prices, how to buy or book?

**Interview the user.** Rules:

- **One question per turn.** Ask with the AskUserQuestion tool. Give 2 to 4 concrete options drawn from what the material suggests, put your best guess first and mark it "(Recommended)", and put the reasoning in each option's description. The tool adds a free-text option, so don't add your own "Other".
- **Most foundational first:** positioning and audience before voice, voice before formatting details.
- **Group related questions.** If several gaps or conflicts share one cause, such as an out-of-date website breaking three guideline rules, ask one question that settles them all. For a conflict, ask which source is current.
- **Save as you go.** Add each answer to `sources/interview-notes.md` straight away, so stopping halfway loses nothing.
- If the user skips a question, note it as skipped and move on. Don't ask it again in another form.
- Every 8 or so questions, offer to stop and carry on later.

## 3. Build the repo

Copy everything in this skill's `scaffold/` folder into the root of this folder, keeping the folder structure. Save `CLAUDE.template.md` as `CLAUDE.md`. Don't overwrite `sources/`. Then fill in the brand files:

- Fill in `knowledge/about.md`, `knowledge/audience.md`, `knowledge/voice.md`, `knowledge/messaging.md` and `brand/identity.md`, keeping the headings. Remove the "Not filled in yet" line from each.
- Only write what the material or the interview supports. Note where each fact came from, e.g. `(from: brand-guidelines.pdf)` or `(from: interview)`.
- In `voice.md`, back every trait with a real line quoted from their material. Don't describe a voice you can't show. Don't use a line as an example if it breaks the brand's own guidelines.
- Where nothing covers a heading, write `[gap: what's missing]`. Never fill a gap with a reasonable-sounding guess. A visible gap is better than a confident invention.
- In `CLAUDE.md`, replace `[Brand name]` with the brand's name. Write up to 10 rules in its "Brand rules" section: the ones that would be embarrassing to break, such as banned words, claims never made, colour or logo misuse, formatting rules. Each one short and specific.
- Save the piece the user named as their best, plus up to two more strong on-brand pieces from their material, into `outputs/` as examples. One file each, named after what it is (e.g. `example-instagram-cardamom-buns.md`), with a line at the top saying which channel it's for and why it's a good example. Check with the user before saving any piece they didn't name.

Tell the user in a few lines what's been built and which gaps are left.

## 4. Run the checks

Run the brand-check skill. When it finishes, tell the user the repo is ready, and give two or three example requests they could try, based on their channels.
