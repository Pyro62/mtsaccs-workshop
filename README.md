# Mt. SAC CS Club Git Workshop Activity: Claim a Cell

Add one file to `cells/` and watch it appear on the live grid.

**Live gridmap:** https://pyro62.github.io/mtsaccs-workshop/

## Before you start

- A GitHub account
- Git installed. Check with `git --version`.
- Your identity set (once per machine):

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Part 1: Add your cell

1. Click **Fork** (top right) to copy this repo to your account. Then clone **your fork**:
   ```bash
   git clone https://github.com/YOUR-USERNAME/mtsaccs-workshop.git
   cd mtsaccs-workshop
   ```
2. Create and switch to a new branch:
   ```bash
   git switch -c cell-yourname
   ```
3. Add a file to `cells/` named after you, such as `cells/yourname.txt`.
   - Text: up to 200 characters.
   - Or a small `.png` / `.jpg` under 200 KB.
4. Check what changed, then stage and commit:
   ```bash
   git status
   git add .
   git commit -m "Add my cell"
   ```
5. Push your branch:
   ```bash
   git push -u origin cell-yourname
   ```
   A GitHub sign-in window may pop up. That's expected. If the terminal asks for a
   password instead, stop and raise your hand.
6. On GitHub, click **Compare & pull request**. Make sure the **base repository** is
   the original repo, not your fork. Then click **Create pull request**.
7. When your PR is merged, refresh the live grid (it can take a minute) and find your cell.

## Part 2: Cause a conflict on purpose

Everyone edits the same line in `favorites.md`.

1. On your fork's GitHub page, click **Sync fork** to get the latest `main`. Then:
   ```bash
   git switch main
   git pull
   git switch -c conflict-yourname
   ```
2. In `favorites.md`, replace `Favorite language: ___` with your answer.
3. Commit and push:
   ```bash
   git add .
   git commit -m "Add my favorite language"
   git push -u origin conflict-yourname
   ```
4. Open a pull request, the same way as Part 1.
5. If GitHub says **This branch has conflicts**, click **Resolve conflicts**:
   - You'll see three marker lines: `<<<<<<<`, `=======`, and `>>>>>>>`.
   - Keep both people's lines and delete the three marker lines.
   - Click **Mark as resolved**, then **Commit merge**.

## Handy commands

| Command | What it does |
| --- | --- |
| `git status` | Shows what's modified and staged |
| `git log --oneline` | Shows commit history (press `q` to exit) |
| `git diff` | Shows changes before you stage them |
| `git branch -a` | Lists all branches |
| `git switch main` | Moves you back to `main` |

## Rules

- Only `.txt`, `.png`, and `.jpg` files in `cells/`.
- Keep content friendly and appropriate for a club event.
- Stuck? Raise your hand.