# Brand repo starter

A folder that teaches Claude your brand once, so every prompt after that starts from your real guidelines instead of a guess.

No coding and no terminal needed. You need the Claude desktop app on a paid plan (for the Code tab).

## Get your copy

**Simplest:** click the green **Code** button on this page, choose **Download ZIP**, unzip it and rename the folder after your brand.

**If you use GitHub:** click **Use this template** to make your own private copy, then clone it with GitHub Desktop. Choose this if a team will share the brand files or you want a history of every change.

Keep your copy **private**. Once it's set up it holds your brand material.

## Set it up in three steps

### 1. Load what you already have

Put anything that describes your brand in `sources/`:

- brand guidelines (save Word files, Google Docs and slides as PDF first)
- 3 to 5 of your best past pieces: posts, emails, web pages
- pitch decks, about pages, product sheets
- logo files and any colour or font specs (these go in `brand/`)

More real material means fewer questions in step 2. If you have very little, that's fine too.

### 2. Run `/brand-setup`

Open the folder in the Claude desktop app (Code tab, then choose the folder) and type `/brand-setup`.

Claude reads everything in `sources/`, drafts your brand files, then asks you questions one at a time to fill the gaps. Expect around 10 to 20 questions, usually 15 to 20 minutes. Most questions have suggested answers to pick from. You can stop at any point and run it again later to carry on.

### 3. Run `/brand-check`

Claude writes three test pieces using only your brand files. You mark each one as on-brand or not. If something's off, Claude fixes the **brand file** that caused it, not the prompt, and tries again.

When all three pass, you're set up.

## Then use it

Open the folder and ask for things in plain English. Your brand files load at the start of every session, and under each piece Claude lists anything it had to invent or assume, so you can check it before it goes out. For example:

- "Write three LinkedIn posts about our new product launch"
- "Give me ten content ideas for next month based on our audience"
- "Make an Instagram carousel explaining our pricing"
- "Turn this blog post into a newsletter"

When you correct something, Claude suggests the change to your brand files that would have prevented it. Accept it, and the fix applies to everyone who uses the folder, not just you. And you can turn tasks you repeat into skills of your own: just ask Claude to "make this a skill".

## What's in the folder

| Folder | What goes in it |
|---|---|
| `CLAUDE.md` | The rules Claude reads at the start of every session |
| `sources/` | Your raw material. Used for setup only, never copied into new content |
| `knowledge/` | Who you are, who you're for, how you sound, what you say |
| `brand/` | Colours, fonts, logos |
| `templates/` | Formats you repeat (a weekly post, a monthly email) |
| `work/` | Drafts in progress |
| `outputs/` | Approved, finished pieces, which Claude also uses as examples |
