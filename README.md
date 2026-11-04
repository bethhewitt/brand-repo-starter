# Brand repo starter

Build a folder that teaches Claude your brand once, so every prompt after that starts from your real guidelines instead of a guess.

No coding and no terminal needed. You need the Claude desktop app on a paid plan (for the Code tab).

## Get your copy

**Simplest:** click the green **Code** button on this page, choose **Download ZIP**, unzip it and rename the folder after your brand.

**If you use GitHub:** click **Use this template** to make your own private copy, then clone it with GitHub Desktop. Choose this if a team will share the brand files or you want a history of every change.

Keep your copy **private**. Once it's set up it holds your brand material.

## Build it

Open the folder in the Claude desktop app (Code tab, then choose the folder) and type `/brand-starter`. Claude takes it from there in four steps:

1. **Start.** Claude asks for your brand name, your website and anything you already have: brand guidelines, 3 to 5 of your best past posts or emails, decks, logo files. Claude makes a `sources` folder inside your brand folder: drop them in there. Save Word files, Google Docs and slides as PDF first. More real material means fewer questions. If you have very little, that's fine too.
2. **Questions.** Claude reads it all, works out what's missing, and asks you one question at a time. Most come with suggested answers to pick from. Expect around 10 to 20 questions. You can stop at any point and type `/brand-starter` again later to carry on.
3. **Build.** Claude creates your brand files: who you are, who you're for, how you sound, what you say and how you look. Anything it couldn't confirm is marked as a gap, never guessed.
4. **Check.** Claude writes three test pieces using only your brand files. You mark each one as on-brand or not. If something's off, Claude fixes the **brand file** that caused it, not the prompt, and tries again.

When all three test pieces pass, you're set up. It usually takes 20 to 30 minutes.

## Then use it

Open the folder and ask for things in plain English. Your brand files load at the start of every session, and under each piece Claude lists anything it had to invent or assume, so you can check it before it goes out. For example:

- "Write three LinkedIn posts about our new product launch"
- "Give me ten content ideas for next month based on our audience"
- "Make an Instagram carousel explaining our pricing"
- "Turn this blog post into a newsletter"

When you correct something, Claude suggests the change to your brand files that would have prevented it. Accept it, and the fix applies to everyone who uses the folder, not just you. Run `/brand-check` again whenever you change the brand files.

To stress-test a plan or idea before you start on it, type `/grilling`. Claude asks one question at a time, with answers to pick from, until every decision is settled.

You can also turn tasks you repeat into skills of your own: just ask Claude to "make this a skill".

## Share it with your team

Put the finished folder on GitHub so your whole team works from the same brand files, and a fix one person makes reaches everyone. [SHARING.md](SHARING.md) walks you through it step by step with GitHub Desktop, no coding needed.

## What gets built

| Folder | What goes in it |
|---|---|
| `CLAUDE.md` | The rules Claude reads at the start of every session |
| `sources/` | Your raw material and interview answers. Used for setup only, never copied into new content |
| `knowledge/` | Who you are, who you're for, how you sound, what you say |
| `brand/` | Colours, fonts, logos |
| `templates/` | Formats you repeat (a weekly post, a monthly email) |
| `work/` | Drafts in progress. Kept on your computer only, never shared on GitHub |
| `outputs/` | Approved, finished pieces, which Claude also uses as examples |

## Credits

The grilling skill is adapted from Matt Pocock's [grill-me skill](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me), used under the MIT License. His licence is in `.claude/skills/grilling/LICENSE`.
