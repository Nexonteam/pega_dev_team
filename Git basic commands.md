🟢 Basic Git Commands
Setup
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list

Starting a Repository
git init
git clone <repo-url>

Staging and Committing
git status
git add <file>
git add .           # Stage all changes
git commit -m "Message"

Viewing Changes
git diff
git log
git show <commit>

Working with Remotes
git remote -v
git remote add origin <url>
git push -u origin main

🟡 Intermediate Git Commands
Branching
git branch
git branch <branch-name>
git checkout <branch-name>
git switch <branch-name>  # Newer alternative to checkout
git merge <branch-name>

Undoing Changes
git checkout -- <file>
git reset HEAD <file>
git revert <commit>

Stashing
git stash
git stash list
git stash pop

Tags
git tag
git tag -a v1.0 -m "Release v1.0"
git push origin --tags

🔴 Advanced Git Commands
Rewriting History
git rebase <branch>
git rebase -i HEAD~3
git cherry-pick <commit>

Cleaning and Repairing
git clean -f         # Remove untracked files
git fsck             # Integrity check
git gc               # Garbage collection

Submodules
git submodule add <repo-url> path/
git submodule update --init --recursive

Git Hooks

Hooks are scripts you place in .git/hooks/.

# Example: pre-commit hook
echo "echo 'Running pre-commit checks...'" > .git/hooks/pre-commit
chmod +x .git/hooks/pre-commit
