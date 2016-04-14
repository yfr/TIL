# Remove all merged branches

`git branch --merged | grep -v "\*" | xargs -n 1 git branch -d`

# Remove all untracked branches

`git fetch -p && git branch -vv | grep gone | awk '{ print $1 }' | xargs -n 1 git branch -d`
