
bugfix

File system: bugfix

cd ~/Desktop
mkdir test
rm -r test (remove)

1, Git: keep tack of text changes version control system VCS
2, distributed version control
Git: http://git-scm.com
Github: https://help.github.com/articles/set-up-git
Which git
Git –version
Git bash: UNIX environment

3, git configureing
Files\git\etc\gitconfig (system)
HOME\.gitconfig

Git config –system
Git config –global (user all repo)
Git config (project)
Git config –global user.name “Yun Zhang”
Git config –global user.emal “yzhhang@” 
(GitHub uses the email address set in your local Git configuration to associate commits pushed from the command line with your GitHub account.)

Git config –list
(git account information) why I have two git username?

https://help.github.com/articles/caching-your-github-password-in-git/#platform-linux
Git config –global credential.helper osxkeychain (mac)
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=3600'
# Set the cache to timeout after 1 hour (setting is in seconds)


Git config user.name
Git config –global core.editor “mate -wl1” (wait)
Git config –global color.ui true 



Git fetch origin
Git log –oneline -5 origin/master
Git branch
Git branch -r

Creat Repo: Ctrl + H show hidden file
in the repo folder type:
git init

Check status:  branch, commit
git status

add some files: they are untracked
git add <filename> <file2>
or
git add .
to keep them tracked by git. (means staged)
to unstage:
git rm –cached <file>

Take snapshot:
git commit

Check difference:
git diff
after git add, difference disappear
git diff –staged

branching: to modify without messing master
git branch newfeature
switch to new branch:
git chekout newfeature
if keep git branch, new branch will build on newfeature branch
or use
git checkout -b newfeature2
to create and switch to new branch.
To check which branch you are on and what branch you have:
git branch
change branch name:
git branch -m <oldname> <newname>
When new branch is more advanced, check back to master will disappear new files and modifies
To undo merge:
git reset --hard HEAD~1

Merging branches:
when clean, no modifies or new files on both branches.
Switch to the branch being merged.
Git merge <branchname>
tunk branch will not be merged if new branch is more advanced
