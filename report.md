# Assignment 1 - Git & GitHub Fundamentals

Amr Kabelma | 145927 | CSC 3324-03 | KBLLL05

Repository: https://github.com/KBLLL05/git-session1-KBLLL05

## 1. Repository Setup

The supplied starter HTML and CSS were imported into git-session1-KBLLL05, then git init -b main initialized the repository. The .gitignore excludes local.env, .env, and *.log; !important.log keeps the required log visible. git check-ignore -v verified the rules, and git ls-files confirmed that important.log is tracked. A .gitattributes rule treats PDF files as binary to preserve their bytes across platforms.

## 2. README & Commit History

The README contains my name, GitHub username, project description, HTML/CSS/Git/Markdown technologies, a shell code block, and links. The AUI logo was extracted from the README example on lecture slide 12 because the starter ZIP did not contain a separate image. The initial work was split into five focused commits: starter setup, README, homepage structure, styling, and the About feature. Later commits record the merge, report preparation, identity/logo updates, and remote synchronization.

## 3. Selective Staging

index.html and style.css were modified together. git diff showed unstaged edits. git add index.html staged only the homepage; git diff --cached showed only that file. Commit 2dea208 recorded the homepage while git status --short still showed style.css modified. The stylesheet was committed separately as 13a8d16. This demonstrates that a commit records the index, not every change in the working directory.

## 4. Branch & Merge

git switch -c feature/about created the feature branch. Commit 38d8167 added about.html and a homepage link. After git switch main, git merge --no-ff feature/about created merge commit a637cda. The graph on page 3 shows that the feature branch was merged into main.

## 5. Remote Changes

An empty public GitHub repository was created, connected using git remote add origin, and published with git push -u origin main. A commit saves a staged snapshot locally; push uploads commits to a remote. The README was edited directly in the GitHub browser editor, creating f36e02a. git fetch origin updated origin/main while leaving local HEAD and the README unchanged. git status -sb showed [behind 1], and git rev-list --left-right --count HEAD...origin/main returned 0 1. git pull --ff-only origin main then integrated that commit; the comparison became 0 0. Fetch updates remote-tracking information; pull fetches and integrates it into the current branch.

## 6. Fair Use of AI

I used AI to check whether there were any improvements I could make to my report.

## 7. Sources & Reflection

Sources: Assignment 1 and Report Template - Group D.pdf (requirements and report headings); git presentation - session 1 - group D.pdf (Git workflow and slide 12 logo); Session1_Practice - group D.zip (starter HTML, CSS, and practice logs). The most subtle concept in this workflow is separating the working tree, staging area, and repository history: a modified file stays outside a commit until it is staged. When Git behaves unexpectedly, the first checks are git status, the current branch, and git diff versus git diff --cached.

## Troubleshooting

A controlled git add app.log attempt failed because *.log is ignored. git check-ignore -v app.log identified the exact rule; the file was correctly left untracked instead of forcing it into Git. Network commands also initially failed in the restricted execution environment; after network approval, push, fetch, and pull succeeded without changing repository URLs or ignore rules.