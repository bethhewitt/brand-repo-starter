# Brand repo starter

Build a folder that teaches Claude your brand once, so every prompt after that starts from your real guidelines instead of a guess.

This version is for Claude. **Using another AI tool?** Use [Brand repo starter for any AI tool](https://github.com/bethhewitt/brand-repo-starter-any-ai) instead.

No coding and no terminal needed. Set aside about 45 minutes. You can stop partway and carry on later.

## Before you start

You need:

- **The Claude desktop app on a paid plan.** You'll work in its **Code** tab.
- **Your brand material, if you have it:** brand guidelines, 3 to 5 of your best past posts or emails, decks, logo files, price lists or service sheets, and any testimonials or reviews you can use. Save Word files, Google Docs and slides as PDF first. If you have very little, that's fine: Claude will ask more questions instead.
- **The names of your main competitors:** the 2 to 5 brands or alternatives your customers would most likely choose instead, with their websites if you know them.

## Install

1. **Download the kit.** On this page, click the green **Code** button, then **Download ZIP**.
    - *You should see:* a file called `brand-repo-starter-main.zip` in your Downloads folder.
2. **Unzip it and give it a home.** Double-click the ZIP to unzip it. Rename the folder after your brand, for example "Northside Bakery brand", and move it to Documents. Move the whole folder, not the files inside it, so the hidden `.claude` folder comes too.
    - *You should see:* `README.md`, `SHARING.md` and `LICENSE` inside it.
3. **Open the folder in Claude.** In the Claude desktop app, go to the **Code** tab and choose your brand folder. If it asks whether you trust the folder, say yes.

**Using GitHub instead?** If a team will share the brand files, or you want a history of every change, click **Use this template** on this page to make your own **private** copy, then clone it with GitHub Desktop and open that folder in step 3.

## Set up your brand

1. **Start the setup.** Type `/brand-starter` and press Enter.
    - *You should see:* a short message about what's going to happen, then a request for your brand name, your website, your main competitors and any material you have.
2. **Add your material.** Claude makes a `sources` folder inside your brand folder. Open it in Finder or File Explorer, drop your files in, then tell Claude you're done. Reply with your brand name, website and competitors in the same message.
    - Files dragged into the chat can be read, but may not be saved. Put them in `sources` so nothing is lost if you stop and carry on later.
    - *You should see:* a two- or three-line summary of what Claude found and what looks thin. Claude also looks at your competitors' websites and recent changes in your market. If you didn't name any competitors, it suggests some for you to confirm.
3. **Answer the questions.** Claude asks one question at a time, usually with suggested answers to click. Pick one, or type your own. For your mission, vision, positioning and tagline, Claude drafts a few options for you to choose between. Expect 20 to 30 questions.
    - When Claude asks to read your website or your competitors' websites, search the web or create files, choose **Allow**. It only creates files inside your brand folder.
    - To stop, just close the session. Later, open the folder again and type `/brand-starter`: it carries on where you left off.
4. **Let Claude build your brand files.** After the last question, Claude writes your brand files and tells you what's built and which gaps are left.
    - *You should see:* new `knowledge`, `brand`, `templates`, `work` and `outputs` folders, and a `CLAUDE.md` file. Anything Claude couldn't confirm is marked `[gap: …]` instead of guessed.
5. **Judge three test pieces.** Claude writes a short post, a longer piece and a simple visual using only your brand files, each aimed at one of your audiences or personas, and opens the visual for you. Mark each one **On-brand**, **Close, but something's off** or **Off-brand**, and say what's wrong.
    - When something's off, Claude shows you the change it would make to a brand file. Approve it, and Claude tries the piece again.
    - *You should see:* a message saying your brand is ready once all three pieces pass, with a few example requests to try.

## Use it day to day

Open your brand folder in the Code tab and ask for things in plain English. For example:

- "Write three LinkedIn posts about our new product launch"
- "Give me ten content ideas for next month based on our audience"
- "Make an Instagram carousel explaining our pricing"
- "Turn this blog post into a newsletter"

Your brand files load at the start of every session. Under each piece, Claude lists anything it had to invent or assume. Check that list before anything goes out. When you correct something, Claude suggests a change to your brand files so the same mistake doesn't happen again. Accept it, and the fix applies to everyone who uses the folder, not just you. After changing the brand files, type `/brand-check`.

To stress-test a plan or idea before you start on it, type `/grilling`. Claude asks one question at a time, with answers to pick from, until every decision is settled.

You can also turn tasks you repeat into skills of your own: just ask Claude to "make this a skill".

Keep your copy **private**. Once it's set up, it holds your brand material.

## Share it with your team

Put the finished folder on GitHub so your whole team works from the same brand files, and a fix one person makes reaches everyone. [SHARING.md](SHARING.md) walks you through it step by step with GitHub Desktop, no coding needed.

## If something goes wrong

| Problem | Fix |
|---|---|
| No **Code** tab in the app | Sign in with a paid plan and update the app to the latest version. |
| `/brand-starter` isn't recognised | You've opened the wrong folder, or the hidden `.claude` folder was left behind. Re-download the ZIP, move the whole folder, and open that folder in the Code tab. |
| Claude doesn't mention your files | Check they're inside the `sources` folder in your brand folder, then tell Claude they're there. |
| Setup stopped halfway | Open the same folder and type `/brand-starter` again. It carries on where it left off. |
| Claude can't read a competitor's website | Some sites block automated visits. Copy the text from their homepage and paste it into the chat. Claude uses that instead. |
| A test piece keeps coming out wrong | Say exactly what's off, such as a word you'd never use. Claude fixes the brand file, not just that piece. |
| Claude says a brand file is "Not filled in yet" | Setup didn't finish. Type `/brand-starter` to complete it. |
| You set up your brand with an older version | Copy in the new `.claude` folder from the latest download, then type `/brand-starter`. It moves your brand files into the new layout without losing anything, asks only what's needed for the new parts, and keeps your brand rules. |

## What gets built

| Folder | What goes in it |
|---|---|
| `CLAUDE.md` | The rules Claude reads at the start of every session |
| `sources/` | Your raw material and interview answers. Used for setup only, never copied into new content |
| `knowledge/` | The facts: who you are, what you sell and for how much, your proof (testimonials, results, customers), who you're for (with personas) and who you compete with. Update these whenever something changes. |
| `brand/` | The choices: why you exist, what you say, how you sound and how you look, with your logo and font files. Change these rarely, and with care. |
| `templates/` | Formats you repeat (a weekly post, a monthly email) |
| `work/` | Drafts in progress. Kept on your computer only, never shared on GitHub |
| `outputs/` | Approved, finished pieces, which Claude also uses as examples |

## Credits

The grilling skill is adapted from Matt Pocock's [grill-me skill](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me), used under the MIT License. His licence is in `.claude/skills/grilling/LICENSE`.
