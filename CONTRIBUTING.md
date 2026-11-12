# Contributing to implementUW projects

These rules apply to every implementUW repository. Each project's README covers anything specific to that project, such as how to run it locally.

## How access works

- You get access to a project when you're added to its team. You only see the repositories your teams work on.
- You can read the code, fork it, open issues, and open pull requests. You can't push to the implementUW repository itself.
- Every change reaches `main` through a pull request that an owner or project lead reviews and merges.

## One-time setup

1. **Accept your invitation.** Check your email (or github.com/implementUW) and accept the invite to the implementUW organization.
2. **Fork the repository.** Open the project's repository on GitHub and click **Fork**. Choose your own account as the owner. Your fork is a private copy that only you and the project team can see.
3. **Clone your fork** (not the implementUW repository) to your computer:

   ```sh
   git clone https://github.com/<your-username>/<repo>.git
   cd <repo>
   git remote add upstream https://github.com/implementUW/<repo>.git
   ```

   `origin` is your fork; `upstream` is the implementUW repository.

## Every piece of work

1. **Sync your fork first.** The implementUW repository changes while you work. On your fork's GitHub page, click **Sync fork** > **Update branch**, then pull it locally:

   ```sh
   git checkout main
   git pull
   ```

   Or, from the command line only:

   ```sh
   git checkout main
   git fetch upstream
   git merge upstream/main
   git push origin main
   ```

2. **Create a branch** from `main` for this one change. Name it `<type>/<short-description>`, where type is `feature`, `fix`, `docs`, or `chore`:

   ```sh
   git checkout -b fix/footer-link
   ```

3. **Make your change and commit** with a message that says what changed, for example `Fix broken link in footer`.
4. **Push the branch to your fork:**

   ```sh
   git push -u origin fix/footer-link
   ```

5. **Open a pull request.** GitHub shows a **Compare & pull request** button on your fork after you push. Make sure the base is `implementUW/<repo>` on `main`, and the compare side is your branch.

## Pull request rules

- **One change per pull request.** Small pull requests get reviewed and merged faster.
- **Describe it:** what changed, why, and how you tested it. Add screenshots for anything visual.
- **Link the issue** it addresses, for example `Closes #12`.
- **Keep it current.** If `main` moves on before your pull request is merged, sync your fork and update your branch.
- **Respond to review comments** by pushing more commits to the same branch. The pull request updates automatically.
- **Don't open a pull request from your fork's `main` branch.** Always use a separate branch.

## Never

- **Commit secrets:** passwords, API keys, tokens, `.env` files, or customer data. If you commit one by accident, tell a project lead right away; deleting it in a later commit is not enough.
- **Share code from a private repository** outside the project team.
- **Make changes outside the pull request process**, including through other tools connected to a project. If a project's README says a tool is off-limits, it is.

## AI tools

You're welcome to use Claude, Gemini, Copilot, or any other tool. The same rules apply: changes go through your fork and a pull request, and you're responsible for every line you submit. Review what the tool wrote before you open the pull request.

## Issues

Use issues for bugs, tasks, and questions about the code. With your team access you can comment on, label, and assign issues and pull requests.

## Leaving a project

When you're removed from a project's team or leave the organization, GitHub deletes your forks of its private repositories. Copies on your own computer remain; please delete them.

## Questions

Ask your project lead or post in the club Slack.
