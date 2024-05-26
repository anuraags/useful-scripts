# Useful git aliases

```
dt = difftool -t opendiff
st = status
ci = commit
co = checkout
lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
hist = rev-list --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --oneline HEAD --
latest-tag = describe --abbrev=0

cz = "!git add -u && npx git-cz"
po = push origin HEAD -u
cleanup = "!git branch --merged | grep  -v '\\*\\|master' | xargs -n 1 git branch -d"
dangles = "!git branch -vv | cut -c 3- | awk '$3 !~/\\[/ { print $1 }'"
diffs = diff --staged
```