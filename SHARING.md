# Share your brand repo with your team

Your brand folder works on your computer. Putting it on GitHub lets everyone on your team use the same brand files, and when one person improves them, everyone gets the fix.

No coding or terminal needed. You'll use **GitHub Desktop**, a free app that does it all with buttons.

About 15 minutes the first time.

## Before you start

- **A GitHub account.** Sign up free at github.com. Your teammates need one too.
- **GitHub Desktop.** Download it free from desktop.github.com, open it and sign in with your GitHub account.

**Used "Use this template" to get the kit?** Your folder is already on GitHub. Skip to step 3, but first click **Push origin** in GitHub Desktop to upload your brand files.

## 1. Add your folder to GitHub Desktop

1. In GitHub Desktop, go to **File**, then **Add Local Repository**.
2. Click **Choose…** and pick your brand folder.
3. It will probably say the folder isn't a repository yet. Click the **create a repository** link, keep the name, then click **Create Repository**.

GitHub Desktop now keeps track of every change to the folder.

## 2. Put it online

1. Click **Publish repository** at the top.
2. Leave **Keep this code private** ticked. Your folder holds brand material, so only invited people should see it.
3. If your company has a GitHub organisation, pick it from the **Organization** list so the repo belongs to the company, not to you.
4. Click **Publish repository**.

Your brand folder is now on GitHub, visible only to you so far.

## 3. Invite your team

1. In GitHub Desktop, go to **Repository**, then **View on GitHub**. This opens the repo in your web browser.
2. Click **Settings** (top right of the repo page), then **Collaborators** in the left menu.
3. Click **Add people**, type each teammate's GitHub username or email, and send the invite.

Each teammate gets an email and has to click **Accept invitation**.

## 4. Each teammate gets their own copy

Send your team these steps:

1. Accept the GitHub invite from your email.
2. Install GitHub Desktop and sign in.
3. Go to **File**, then **Clone Repository**, pick the brand repo from the list, choose where to save it, and click **Clone**.
4. In the Claude desktop app, start a **new session** in the Code tab, choose that folder, and start asking for things.

They don't need to run `/brand-starter`. The brand is already built.

## 5. Optional: make one person the reviewer

Skip this step if you're happy for anyone on the team to change the brand files directly, or you'd rather not pay for GitHub. Step 6 covers both ways of working.

Brand changes affect everyone's work, so it's safest if one person checks every change before it reaches the team. Once this is set up, nobody can change the shared brand files directly. Everyone suggests a change (a **pull request**), and it only goes in once the reviewer approves it.

**Check your GitHub plan first.** For a private repo, this needs a paid plan: **GitHub Team** if the repo belongs to an organisation, or **GitHub Pro** if it belongs to you. On the free plan the settings below can be saved but GitHub won't enforce them. You can check or upgrade under your organisation's (or your own) **Settings**, then **Billing and plans**.

**Name the reviewer.** Open the brand folder in Claude and ask "make [reviewer's GitHub username] the reviewer for every change". Claude adds a small file called `.github/CODEOWNERS` that tells GitHub who that is. In GitHub Desktop, click **Commit to main**, then **Push origin**. (This one can go straight in because the rule below isn't on yet.) From then on, GitHub asks the reviewer to look at every pull request automatically.

**Turn on the rule.** The repo owner does this once, on GitHub in the web browser:

1. Open the repo, click **Settings**, then **Rules** and **Rulesets** in the left menu.
2. Click **New ruleset**, then **New branch ruleset**.
3. Name it "Review before changes go in" and set **Enforcement status** to **Active**.
4. Under **Target branches**, click **Add target**, then **Include default branch**.
5. Under **Rules**, leave **Restrict deletions** and **Block force pushes** ticked, and tick **Require a pull request before merging**. In the options that appear:
   - set **Required approvals** to **1**
   - tick **Require review from Code Owners**
   - tick **Dismiss stale pull request approvals when new commits are pushed**, so the reviewer re-checks anything changed after they approved
6. Click **Create**.

**The reviewer's own changes.** GitHub won't let anyone approve their own pull request. Either ask a second person to approve the reviewer's changes, or let the reviewer skip the check: in the ruleset, under **Bypass list**, click **Add bypass** and pick the reviewer. If you do this, ask them to still use pull requests so there's a record of what changed.

## 6. Keep everyone in sync

Two habits keep everyone's copy the same.

**Before you start work, get the latest.** Open GitHub Desktop. Check the **Current Branch** button at the top says **main** (click it and pick **main** if not). Click **Fetch origin**. If it changes to **Pull origin**, click that too. This brings in any changes your teammates made.

**After you change the brand files, share them.** For example, after Claude fixes a brand file following a correction, or after a `/brand-check`. How you do this depends on whether you set up a reviewer in step 5.

### No reviewer: share the change straight away

1. Open GitHub Desktop. It lists what changed.
2. In the **Summary** box at the bottom left, write a short note, such as "Banned the word 'elevated'".
3. Click **Commit to main**.
4. Click **Push origin**.

Everyone else gets the change the next time they click Fetch origin.

### With a reviewer: suggest the change

1. Open GitHub Desktop. It lists what changed.
2. Click **Current Branch**, then **New Branch**. Give it a short name, such as "ban-elevated", and click **Create Branch**. If it asks, choose to **bring your changes** to the new branch.
3. In the **Summary** box at the bottom left, write a short note, such as "Banned the word 'elevated'".
4. Click **Commit to ban-elevated** (it shows your branch name).
5. Click **Publish branch**.
6. Click **Create Pull Request**. This opens GitHub in your browser. Add a sentence on why you made the change, then click **Create pull request**.

The reviewer gets an email. Once it's approved and merged, switch back to **main** in GitHub Desktop and click **Fetch origin**, then **Pull origin**. Everyone else gets the change the next time they do the same.

**If you're the reviewer:**

1. Open the repo on GitHub and click **Pull requests**. Pick one.
2. Click **Files changed** to see exactly what's different. Green lines were added, red lines were removed.
3. Click **Review changes** (or **Submit review**). Choose **Approve**, or **Request changes** and say what to fix. Then click **Submit review**.
4. Once approved, click **Merge pull request**, then **Confirm merge**. Click **Delete branch** to tidy up.

Not sure about a change? Paste the pull request link into Claude and ask "does this change fit our brand files?"

## Good to know

- **No reviewer? Agree who changes the brand files.** Without a reviewer, anyone can change them, so it's simplest if one person (or a small group) makes the changes. Everyone else suggests changes to that person.
- **Have a reviewer and committed straight to main by mistake?** GitHub will refuse the push. Don't worry, nothing is lost. Open the folder in Claude and ask "move my last commit onto a new branch so I can open a pull request".
- **Changing the reviewer?** Ask Claude to update the reviewer in `.github/CODEOWNERS`, and update the bypass list in the ruleset if you used one.
- **If GitHub Desktop says there's a conflict,** two people changed the same lines at once. Open the folder in Claude and ask "help me resolve this conflict". Claude will explain which version to keep.
- **Made a mistake?** Every change is saved in the **History** tab. To undo a commit, right-click it and choose **Revert changes in commit**.
- **Big files** over 100MB, such as long videos, can't go on GitHub. Keep those somewhere else and link to them.
- **Your `work` folder stays on your computer.** Drafts in `work/` are never uploaded to GitHub, so teammates only see the brand files and finished pieces. This keeps half-done drafts out of everyone's way.
- **Want to share a draft?** Ask Claude to change the file so it can be shared, for example "move this draft into outputs so the team can see it". Then share it as in step 6.
- **Drafts already on GitHub from before?** Ask Claude to "stop sharing the work folder on GitHub". It will take them off GitHub but leave them on your computer.
