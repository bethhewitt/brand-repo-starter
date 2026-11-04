# [Brand name]

Claude reads this file at the start of every session. The brand files below load with it automatically, so every task starts from them.

Built with `/brand-starter`. Run `/brand-check` after changing the brand files.

## Brand files

@knowledge/about.md
@knowledge/mission.md
@knowledge/competitors.md
@knowledge/audience.md
@knowledge/messaging.md
@knowledge/voice.md
@brand/identity.md

For a repeat format, also read the matching file in `templates/`. For a feel of what good looks like, read the pieces in `outputs/`.

## Rules for every task

1. **Check the setup first.** If any brand file above still says "Not filled in yet", tell the user and suggest running `/brand-starter` before doing anything else.
2. **Don't invent facts.** Never make up statistics, prices, opening hours, product details, customer names, quotes, testimonials, claims or facts about competitors. If the brand files don't cover it, say so and ask.
3. **Write for someone specific.** Aim every piece at an audience or persona from `audience.md`, and start from the pillars and lines in `messaging.md`. If the request doesn't say who it's for, use the main audience and say which you chose.
4. **Sound like no one else.** Don't lean on the claims and phrases under "What everyone says" in `competitors.md`. Only name or compare with a competitor in the ways "How we talk about competitors" allows. If it says nothing, don't name them.
5. **List what you assumed.** Under every piece of content, add a short "Invented or assumed" list: anything not taken from the brand files. Write "nothing" if that's true.
6. **Only write from the brand files.** `sources/` is raw material for setup and may be out of date. Never copy lines or facts from it into new content. When the two disagree, the brand files win.
7. **The brand files win over requests too.** If a request conflicts with them, including the mission, flag the conflict before going ahead.
8. **Fix the files, not the prompt.** When the user corrects an output, suggest the edit to the brand file that would have prevented it, so the fix reaches everyone who uses this folder.
9. **Save work in the right place.** Drafts go in `work/YYYY-MM-DD/`. Approved, finished pieces go in `outputs/`.

## Brand rules

_Filled in by `/brand-starter`. Up to 10 short, specific rules that would be embarrassing to break, such as words never used, claims never made or colours never paired._

## Folders

- `sources/` raw material, for setup only
- `knowledge/` who the brand is, why it exists, who it competes with, who it's for, what it says, how it sounds
- `brand/` visual identity: colours, fonts, logos
- `templates/` repeat formats
- `work/` drafts in progress, by date
- `outputs/` approved pieces, which double as examples of good work
