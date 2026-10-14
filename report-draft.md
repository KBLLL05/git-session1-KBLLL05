# Assignment 1 report - draft

## 1. Repository Setup
The starter HTML and CSS were imported from the supplied practice ZIP. The repository was initialized with git init -b main. The .gitignore excludes local.env, .env, and normal *.log files; !important.log preserves the required exception. git check-ignore -v and git ls-files verified the rules and tracked files.

## 2. README & Commit History
The README includes the provisional name Amr, username KBLLL05, a description, technologies, a shell code block, and a GitHub link. The required image is pending because no image was included in the supplied ZIP. Five focused commits cover the starter files, README, homepage structure, styling, and About feature; a sixth commit records the merge.

## 3. Selective Staging
index.html and style.css were modified together. git diff showed unstaged edits. Only index.html was staged with git add index.html, and git diff --cached confirmed the staged content. After committing the homepage, git status --short still showed style.css modified. The stylesheet was then committed separately.

## 4. Branch & Merge
git switch -c feature/about created the feature branch. The About page and homepage link were committed there. After git switch main, git merge --no-ff feature/about merged the feature and preserved an explicit merge commit.

## 5. Remote Changes
A commit records the staged snapshot in the local repository. A push transfers local commits to a remote repository. Fetch downloads remote objects and updates remote-tracking references without integrating them into the working branch; pull fetches and integrates remote changes. Execution of the GitHub creation, push, browser README edit, fetch verification, and pull is pending GitHub sign-in. These steps have not yet been completed.

## 6. Fair Use of AI
AI assistance was used extensively to inspect the assignment, prepare the starter-based website and README, execute the local Git workflow, capture command output, and draft this report. The request was to complete the assignment using the supplied materials. The generated HTML/CSS, ignore rules, branch workflow, and explanations were accepted provisionally. The assistant verified staging with git status and git diff --cached, ignore behavior with git check-ignore and git ls-files, and the merge with git log --graph. The student still needs to review the files and understand each command; this draft does not claim that personal review has happened.

## 7. Sources & Reflection
Sources: Assignment 1 and Report Template - Group D.pdf (requirements and report structure); git presentation - session 1 - group D.pdf (Git commands); Session1_Practice - group D.zip (starter files). Suggested reflection for student review: The staging area is the trickiest distinction because modified files do not automatically enter a commit. If Git behaves unexpectedly, first check git status, the current branch, and the staged versus unstaged diff.

## Troubleshooting example
A deliberate attempt to git add app.log was rejected because *.log is ignored. git check-ignore -v app.log identified the responsible rule. The resolution was to leave this normal log untracked; important.log remained tracked through the exception. This was a controlled demonstration, not an accidental failure.