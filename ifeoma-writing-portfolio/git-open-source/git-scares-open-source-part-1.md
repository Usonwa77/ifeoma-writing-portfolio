# Overcoming the 'Git Scares': A Friendly Beginner's Guide to Open Source. Part 1

**Original publication:** https://dev.to/ifeoma_nwafor/overcoming-the-git-scares-a-friendly-beginners-guide-to-open-source-pt-1-adding-yourself-to-1fm3

**Tags:** #git #beginners #career #opensource

Entering open source can feel daunting. The sheer fear of running the wrong command in your terminal, breaking a codebase, or looking inexperienced stops many capable developers from making their very first contribution. This is the "Git Scares"—and every engineer has felt it.

This guide eliminates that barrier. Instead of throwing you into complex codebases and messy bug fixes, Part 1 walks you through the cleanest, zero-risk way to submit your first Pull Request: adding your name to CONTRIBUTORS.md in an active community repository (PinpointPro).

By the end of this tutorial, you will have completed the full professional Git lifecycle—forking, cloning, branching, committing, pushing, and opening a Pull Request—without the risk of breaking production.

## What You Need Before You Start

- A free GitHub account
- Git installed on your computer (Git Bash or PowerShell for Windows, or the built-in Terminal for macOS/Linux)
- A terminal
- A simple text editor such as Notepad, VS Code, or Vim

Take a breath, open your terminal, and let’s make your first contribution!

# STEP 1 — Fork the Repository on GitHub

Forking gives you a space you fully own — you can experiment, commit, and break things without touching the original project. We are working with a repository from https://github.com/raphgm/pinpointpro.

1. Open your browser and go to: https://github.com/raphgm/pinpointpro
2. Click the 'Fork' button in the top-right corner.
3. Leave all settings as default and click 'Create fork'.
4. GitHub will redirect you to your fork.

# STEP 2 — Configure Your Git Identity

Without this, Git cannot create a commit — it will error and ask you to configure your identity first.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

# STEP 3 — Clone Your Fork to Your Machine

All Git commands must run from inside the repository folder.

```bash
git clone https://github.com/YOUR_USERNAME/pinpointpro.git
cd pinpointpro
```

# STEP 4 — Wire Up the Upstream Remote

Add the upstream remote:

```bash
git remote add upstream https://github.com/raphgm/pinpointpro.git
```

Verify both remotes:

```bash
git remote -v
```

Sync your fork:

```bash
git fetch upstream
git checkout main
git merge upstream/main
```

# STEP 5 — Create Your Feature Branch

```bash
git checkout -b feature/yourname-add-contributor
git branch
```

# STEP 6 — Choose Your Contribution & Make It

Open the file:

```bash
vi CONTRIBUTORS.md
```

or on Windows:

```powershell
notepad .\CONTRIBUTORS.md
```

Append your contribution information at the bottom:

- Your Full Name
- GitHub: @your-username
- Contribution
- Date: YYYY-MM-DD

Check the changes:

```bash
git diff CONTRIBUTORS.md
```

# STEP 7 — Stage & Commit Your Work

```bash
git add CONTRIBUTORS.md
git status
```

Commit:

```bash
git commit -m "docs(contributors): add @yourname - Project name"
git log --oneline -3
```

# STEP 8 — Push & Open a Pull Request

```bash
git push -u origin feature/yourname-add-contributor
```

After pushing, open the Pull Request on GitHub and describe what you changed and why.

# STEP 9 — Create the README File

A README documents what a project is and how to reproduce it.

```bash
touch README.md
```

Add your project documentation, then:

```bash
git status
git add .
git commit -m "docs: add README for PinpointPro Git Flow lab"
git push -u origin feature/yourname-add-contributor
```

You Just Beat the "Git Scares"!

You forked, cloned, branched, committed, pushed, and officially submitted a Pull Request to an open-source project.

Share Your Win!

Drop your GitHub handle or your PR link in the comments below so we can celebrate your first contribution together.

Hit any roadblocks or get an unexpected terminal message? Comment with what went wrong—I'm actively checking the comments to help troubleshoot.

If this guide made Git feel a little less intimidating, don't forget to heart and bookmark it so other beginners can find it.

Stay tuned for Part 2, where we'll dive into finding "Good First Issues," reading project issue trackers, and resolving your very first merge conflict!
