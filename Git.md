# Git

Failed to connect to raw.githubusercontent.com
输入访问不了的域名,查询之后可以获得正确的 IP 地址,本机的 host 文件中添加

```git
https://www.ipaddress.com
sudo vim /etc/hosts
```

## SSH Key Connect

creat

```git
ssh-keygen -t rsa -C ""
```

add public key to github

```git
cat ~/.ssh/id_rsa.pub
```

test

```git
ssh -T git@github.com
```

## Config

```git
git remote add origin git@github.com:
git config --global user.email ""
git config --global user.name ""
git config --global color.ui auto
git push -u origin master
```

## Command

```git
git init
git status
git add
git commit
git log
git log --pretty=short
git log --graph
git log xx.md
git log -p xx.md
git reflog expire --expire=7.days.ago --expire-unreachable=now --all
git diff
git diff HEAD
```

## Branch

```git
git branch
git branch -b xx
git branch -
git merge --no-ff xx
git reset --hard yyyyyyy
git checkout --orphan
git branch --set-upstream-to=origin/master
git reflog
```

## Commit

```git
git commit --amend
git rebase -i HEAD~2
```

## Remote

```git
git clone --depth=1
git remote -v
git remote remove
```

## Pull Developer's Branch

```git
git branch -new
git checkout -b xx origin/xx
git pull origin xx
```

## Clean

```git
git reflog expire --expire=now --all
git gc --prune=now
git gc --aggressive --prune=now
```
