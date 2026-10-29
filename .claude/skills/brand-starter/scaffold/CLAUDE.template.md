# [Brand name]

Claude reads this file at the start of every session. The brand files below load with it automatically, so every task starts from them.

Built with `/brand-starter`. Run `/brand-check` after changing the brand files.

## Brand files

@knowledge/about.md
@knowledge/audience.md
@knowledge/voice.md
@knowledge/messaging.md
@brand/identity.md

For a repeat format, also read the matching file in `templates/`. For a feel of what good looks like, read the pieces in `outputs/`.

## Rules for every task

1. **Check the setup first.** If any brand file above still says "Not filled in yet", tell the user and suggest running `/brand-starter` before doing anything else.
2. **Don't invent facts.** Never make up statistics, prices, opening hours, product details, customer names, quotes, testimonials or claims. If the brand files don't cover it, say so and ask.
3. **List what you assumed.** Under every piece of content, add a short "Invented or assumed" list: anything not taken from the brand files. Write "nothing" if that's true.
4. **Only write from the brand files.** `sources/` is raw material for setup and may be out of date. Never copy lines or facts from it into new content. When the two disagree, the brand files win.
5. **The brand files win over requests too.** If a request conflicts with them, flag the conflict before going ahead.
6. **Fix the files, not the prompt.** When the user corrects an output, suggest the edit to the brand file that would have prevented it, so the fix reaches everyone who uses this folder.
7. **Save work in the right place.** Drafts go in `work/YYYY-MM-DD/`. Approved, finished pieces go in `outputs/`.

## Brand rules

_Filled in by `/brand-starter`. Up to 10 short, specific rules that would be embarrassing to break, such as words never used, claims never made or colours never paired._

## Folders

- `sources/` raw material, for setup only
- `knowledge/` who the brand is, who it's for, how it sounds, what it says
- `brand/` visual identity: colours, fonts, logos
- `templates/` repeat formats
- `work/` drafts in progress, by date
- `outputs/` approved pieces, which double as examples of good work
