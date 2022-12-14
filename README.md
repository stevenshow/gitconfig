# gitconfig
Simple git config file for easy workspace setting up.  Mainly for the aliases.

```
[alias]
	br = branch --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(contents:subject) %(color:green)(%(committerdate:relative)) [%(authorname)]' --sort=-committerdate
	cmp = "!f() { git commit -m \"$@\" && git push; }; f"
	co = checkout -b
	col = checkout -
	com = checkout master
	del = branch -D
	log = !git log --pretty=format:\"%C(magenta)%h%Creset -%C(red)%d%Creset %s %C(dim green)(%cr) [%an]\" --abbrev-commit -30
	pom = pull origin master
	undo = reset HEAD~1 --mixed
```
