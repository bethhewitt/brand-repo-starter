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

## 5. Keep everyone in sync

Two habits keep everyone's copy the same.

**Before you start work, get the latest.** Open GitHub Desktop and click **Fetch origin**. If it changes to **Pull origin**, click that too. This brings in any changes your teammates made.

**After you change the brand files, share them.** For example, after Claude fixes a brand file following a correction, or after a `/brand-check`:

1. Open GitHub Desktop. It lists what changed.
2. In the **Summary** box at the bottom left, write a short note, such as "Banned the word 'elevated'".
3. Click **Commit to main**.
4. Click **Push origin**.

Everyone else gets the change the next time they click Fetch origin.

## Good to know

- **Agree who changes the brand files.** Brand changes affect everyone's work, so it's simplest if one person (or a small group) approves them. Everyone else suggests changes to that person.
- **If GitHub Desktop says there's a conflict,** two people changed the same lines at once. Open the folder in Claude and ask "help me resolve this conflict". Claude will explain which version to keep.
- **Made a mistake?** Every change is saved in the **History** tab. To undo a commit, right-click it and choose **Revert changes in commit**.
- **Big files** over 100MB, such as long videos, can't go on GitHub. Keep those somewhere else and link to them.
- **Don't want drafts shared?** Ask Claude to "stop sharing the work folder on GitHub" and it will set that up for you.
