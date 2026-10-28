---
name: brand-setup
description: Set up or continue setting up this brand repo. Reads the material in sources/, drafts the brand files in knowledge/ and brand/, then interviews the user one question at a time to fill gaps and settle contradictions. Use when the user runs /brand-setup, asks to "set up my brand", or wants to carry on an unfinished setup.
---

# Brand setup

Turn the user's existing material into confirmed brand files, then fill what's missing by asking them. The user is a marketer, not a developer. Use plain language, and never mention files or folders they don't need to know about.

Work in four stages. If the brand files are already partly filled, this is a resumed setup: skip to the first stage that isn't finished.

## 1. Read what's there

- Read everything in `sources/` and `brand/`, including PDFs and images. Skip the `README.md` files: they're instructions, not brand material.
- If `sources/` is empty, ask for the brand's website address and read its main pages (home, about, product or services). If there's no website either, say it'll take more questions and go straight to stage 3.
- Tell the user in two or three lines what you found and what looks thin. Don't list every file.

## 2. Draft the brand files

Fill in `knowledge/about.md`, `knowledge/audience.md`, `knowledge/voice.md`, `knowledge/messaging.md` and `brand/identity.md`, keeping the headings already in each file. Remove the "Not filled in yet" line from each file you fill.

- Only write what the sources support. Note where each fact came from, e.g. `(from: brand-guidelines.pdf)`.
- In `voice.md`, back every trait with a real line quoted from the sources. Don't describe a voice you can't show. Don't use a line as an example if it breaks the brand's own guidelines. Flag it as a conflict instead.
- Where the sources say nothing, write `[gap: what's missing]`.
- Where sources disagree, write `[conflict: source A says X, source B says Y]`.
- Never fill a gap with a reasonable-sounding guess. A visible gap is better than a confident invention.

## 3. Interview to close the gaps

Work through every `[gap]` and `[conflict]`, plus these questions only a person can answer, even when the sources look complete:

- Who is this brand not for?
- What would you never say, or never want to be mistaken for?
- Which claims can you prove, and how?
- Which past piece is the best example of you, and why?
- What do people usually get wrong when they write or design for you?
- What practical details come up in most content: opening hours, location, prices, how to buy or book?

Rules for the interview:

- **Group related markers.** If several gaps or conflicts share one cause, such as an out-of-date website breaking three guideline rules, ask one question that settles them all. For a conflict, ask which source is current.
- **One question per turn.** Ask with the AskUserQuestion tool. Give 2 to 4 concrete options drawn from what the sources suggest, put your best guess first and mark it "(Recommended)", and put the reasoning in each option's description. The tool adds a free-text option, so don't add your own "Other".
- Ask the most foundational question first: positioning and audience before voice, voice before formatting details.
- Write each answer into the right file straight away, so stopping halfway loses nothing.
- If the user skips a question, leave the `[gap]` in place and move on. Don't ask it again in another form.
- Every 8 or so questions, offer to stop and carry on later.

## 4. Write the brand rules

- Pick up to 10 rules for the "Brand rules" section of `CLAUDE.md`. Choose the ones that would be embarrassing to break: banned words, claims never made, colour or logo misuse, formatting rules. Each one short and specific.
- Replace `[Brand name]` in the title of `CLAUDE.md`.
- Save the best piece the user named, plus up to two more strong on-brand pieces from `sources/`, into `outputs/` as examples. One file each, named after what it is (e.g. `example-instagram-cardamom-buns.md`), with a line at the top saying which channel it's for and why it's a good example. Check with the user before saving any piece they didn't name.
- Summarise in a few lines what's set up and which gaps are left, then suggest running `/brand-check`.
