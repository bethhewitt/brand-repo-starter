---
name: brand-starter
description: Build a brand repo from scratch. Collects the user's existing brand material, interviews them one question at a time, builds the folder of brand files Claude reads before every task, then tests it with brand-check. Use when the user runs /brand-starter, asks to "set up my brand", or wants to carry on an unfinished setup.
---

# Brand starter

Build this folder into a brand repo, starting from nothing. The user is a marketer, not a developer. Use plain language, and don't mention files or folders they don't need to know about.

There are four steps. Before starting, check where things are so a stopped setup can carry on:

- `knowledge/` has every file in this skill's `scaffold/knowledge/` and none of them say "Not filled in yet": the repo is built. Ask whether to run the checks (step 4) or start again.
- `knowledge/` exists but some files still say "Not filled in yet", or a file from `scaffold/knowledge/` is missing: the build is unfinished. Read `sources/interview-notes.md`. If the notes don't cover the headings in the unfinished files, go back to step 2 for those headings only. Then carry on from step 3, filling in only the files that aren't done yet.
- `sources/interview-notes.md` exists: the interview was started. Read it and carry on from step 2.
- Otherwise, start at step 1.

## 1. Start

- In two or three lines, tell the user what's about to happen: you'll gather what they have, ask some questions, build their brand files, then test them. It takes about 30 to 45 minutes, and they can stop at any point.
- Create a `sources/` folder. Copy `sources/README.md` into it from this skill's `scaffold/` folder.
- Ask for their existing material, all in one message:
  - the brand's name
  - their website address, if they have one
  - the 2 to 5 brands or alternatives their customers would most likely choose instead, with website addresses if they know them
  - any brand guidelines, past posts, emails, decks or logo files. Ask them to drop these into the `sources` folder inside this folder (in Finder or File Explorer), then say when they're done. Word files, Google Docs and slides work best saved as PDF first.
- If they attach files in the chat instead, read them, but don't rely on them being saved. Ask them to drop the files into `sources` too, so nothing is lost if the setup stops and carries on later. Text they paste into the chat, such as past posts, can be saved as markdown files in `sources/`.
- If they have nothing, that's fine: the interview will take longer.

## 2. Ask for what's missing

**Read what they gave you.** Read everything in `sources/` except its README, and the main pages of their website (home, about, products or services). In two or three lines, tell the user what you found and what looks thin. Don't list every file.

**Research the competitors and the market.** For each competitor the user named, visit their homepage, about page and main social profile. Note how they describe themselves (quote headlines and subheads word for word), who they say they're for, the three things they lead with, and the proof they show. Then search the web for the 3 to 5 recent changes in the category, platforms or audience behaviour that would change what this brand's content should do, each with one specific fact and its source and date. Save all of it, with today's date, in `sources/competitor-research.md`. If the user named no competitors, suggest a few from the research and confirm them before profiling.

**Work out what's missing.** Use the outlines in this skill's `scaffold/knowledge/` and `scaffold/brand/identity.md` as the checklist: every heading in them needs an answer. List the gaps (nothing in the material) and conflicts (sources that disagree).

Always ask these as well, because only a person can answer them:

- Why does the brand exist, and what would it never do, even for money?
- What would your customers do if you didn't exist, including doing nothing?
- Should content ever name or compare itself with a competitor?
- What makes someone start looking for something like you, and what stops them choosing you?
- Which of what you know about your customers comes from real data (analytics, reviews, sales), and which is belief?
- Who is this brand not for?
- What would you never say, or never want to be mistaken for?
- Which claims can you prove, and how?
- Which past piece is the best example of you, and why?
- What do people usually get wrong when they write or design for you?
- What practical details come up in most content: opening hours, location, prices, how to buy or book?

**Interview the user.** Rules:

- **One question per turn.** Ask with the AskUserQuestion tool. Give 2 to 4 concrete options drawn from what the material suggests, put your best guess first and mark it "(Recommended)", and put the reasoning in each option's description. The tool adds a free-text option, so don't add your own "Other".
- **Most foundational first:** mission and vision, then competitors and audience, then positioning and messaging, then voice, then formatting details.
- **Draft statements for the user to choose from.** For the mission, vision, positioning and tagline, draft 2 to 4 options from the material, ranging from safe to bold. Before offering them, test each one: could a new team member repeat it after one reading? Is it true today (or, for the vision, plausible)? Would it be wrong if a competitor said it? Does it rule something out? Offer only the options that pass. Settle the mission before the vision, and the positioning before the tagline.
- **Personas only where they help.** Add personas when people in the audience care about meaningfully different things, such as a buyer and a user. The material can't tell you what goes on in a persona's head, so ask the user for that rather than inventing it.
- **Group related questions.** If several gaps or conflicts share one cause, such as an out-of-date website breaking three guideline rules, ask one question that settles them all. For a conflict, ask which source is current.
- **Save as you go.** Add each answer to `sources/interview-notes.md` straight away, so stopping halfway loses nothing.
- If the user skips a question, note it as skipped and move on. Don't ask it again in another form.
- Every 8 or so questions, offer to stop and carry on later.

## 3. Build the repo

Copy everything in this skill's `scaffold/` folder into the root of this folder, keeping the folder structure, except `CLAUDE.template.md`: save that as `CLAUDE.md` instead. Don't overwrite `sources/`, or any brand file that's already filled in.

If `CLAUDE.md` already exists with the brand's name at the top, this is an update to an older setup: don't replace it, because its brand rules would be lost. Instead, compare it with `CLAUDE.template.md` and add only what it's missing: any `@` line under "Brand files", and any rule under "Rules for every task" (renumbering the list). Keep its "Brand rules" section exactly as it is.

Then fill in the brand files:

- Fill in every file in `knowledge/` (`about.md`, `mission.md`, `competitors.md`, `audience.md`, `messaging.md`, `voice.md`) and `brand/identity.md`, keeping the headings. Remove the "Not filled in yet" line from each.
- Only write what the material or the interview supports. Note where each fact came from, e.g. `(from: brand-guidelines.pdf)` or `(from: interview)`.
- In `competitors.md`, quote competitors' own words exactly, with the page and the date checked. If the user didn't say whether content may name competitors, write `[gap: whether content may name competitors]`.
- In `audience.md`, mark each point (observed) or (assumed), as the file explains.
- In `messaging.md`, every pillar and difference needs proof from `about.md` or the interview. Where there's none, write the pillar anyway and add `[gap: proof needed, e.g. a review score or customer number]`. Don't use anything listed under "What everyone says" in `competitors.md`.
- In `voice.md`, back every trait with a real line quoted from their material. Don't describe a voice you can't show. Don't use a line as an example if it breaks the brand's own guidelines.
- Avoid empty words such as "inspire", "empower", "world-class" and "passionate" in every file, unless the sentence falls apart without them.
- Where nothing covers a heading, write `[gap: what's missing]`. Never fill a gap with a reasonable-sounding guess. A visible gap is better than a confident invention.
- Where sources disagree and the interview didn't settle it (for example, the user skipped the question), write `[conflict: what disagrees, and where]` instead of choosing one.
- In `CLAUDE.md`, replace `[Brand name]` with the brand's name. Write up to 10 rules in its "Brand rules" section: the ones that would be embarrassing to break, such as banned words, claims never made, how to treat competitors, colour or logo misuse, formatting rules. Each one short and specific.
- Save the piece the user named as their best, plus up to two more strong on-brand pieces from their material, into `outputs/` as examples. One file each, named after what it is (e.g. `example-instagram-cardamom-buns.md`), with a line at the top saying which channel it's for and why it's a good example. Check with the user before saving any piece they didn't name.

Tell the user in a few lines what's been built and which gaps are left.

## 4. Run the checks

Run the brand-check skill. When it finishes, tell the user the repo is ready, and give two or three example requests they could try, based on their channels.
