---
name: brand-check
description: Test whether this brand repo is set up correctly. Writes three test pieces from the brand files alone, has the user judge each one, and fixes the brand files (never the prompt) when something comes out off-brand. Use when the user runs /brand-check, asks "is my brand set up right?", or after changing the brand files.
---

# Brand check

Prove the brand files are enough on their own. If a test piece comes out off-brand, the fix goes into the brand files, so every future prompt benefits.

## 1. Check for gaps

Read `CLAUDE.md` and every `.md` file in `knowledge/` and `brand/`. If any file still says "Not filled in yet", or any `[gap: …]` or `[conflict: …]` markers remain, list them in a line or two. Then ask whether to run `/brand-starter` first or test anyway.

## 2. Make three test pieces

Choose three pieces that suit this brand's channels (from `audience.md`) and cover different skills:

1. **A short written piece** on the brand's main channel, e.g. a social post.
2. **A longer written piece**, e.g. a newsletter intro, product email or web section.
3. **A visual**: a single social image or slide as a self-contained HTML file, sized for its channel and following the colours, fonts, contrast, layout and imagery rules in `brand/identity.md`.

Use only the brand files, and pick topics the brand files already cover so nothing needs inventing. Aim each piece at a named audience or persona from `audience.md`, build it from the pillars in `messaging.md`, and say which you used above the piece. If the brand has personas, aim at least two pieces at different ones. At least one piece should feature an offer from `offering.md` and use proof from `proof.md` (cleared items only), so those files get tested too. Don't lean on anything listed under "What everyone says" in `competitors.md`. If the logo or another asset isn't in `brand/`, leave a visible placeholder such as `[logo]` rather than drawing one. Save the pieces in `work/YYYY-MM-DD/brand-check/` using today's date.

Under each piece, add two short lists:

- **Rules followed:** the brand rules this piece relied on.
- **Invented or assumed:** every fact, number, detail or comparison that isn't in the brand files, such as opening hours, a statistic or a customer anecdote. Be strict: if you can't point to the file it came from, it goes here.

Every item under "Invented or assumed" is a gap. In step 4, deal with it even if the user calls the piece on-brand: either the fact goes into the brand files, or a rule says not to use it.

## 3. Let the user judge

Open the visual so the user can see it. Then show the user each piece and ask, one at a time with AskUserQuestion: "On-brand", "Close, but something's off" or "Off-brand". Then ask what's wrong if it isn't on-brand.

## 4. Fix the files, not the prompt

For each piece that isn't on-brand:

- Work out why: which brand file was missing something, too vague, or contradicted itself.
- Show the user the exact edit you'd make to that file, such as a new banned word, a clearer rule or a better example line. Make the edit once they agree.
- If the problem is broad enough to matter in every task, also add a rule to the "Brand rules" section of `CLAUDE.md` (10 rules at most).
- Remake that piece from the updated files and ask again.

## 5. Finish

When all three pieces are on-brand, say so and summarise what changed in the brand files. If `outputs/` has no example for a channel one of the pieces covers, suggest saving that piece there as an example of what good looks like.
