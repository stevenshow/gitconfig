# gitconfig
Simple git config file for easy workspace setting up.  Mainly for the aliases.

### [alias]
	co = checkout -b
	del = branch -D
	cmp = "!f() { git commit -m \"$@\" && git push; }; f"
	br = branch --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(contents:subject) %(color:green)(%(committerdate:relative)) [%(authorname)]' --sort=-committerdate
	undo = reset HEAD~1 --mixed
	log = !git log --pretty=format:\"%C(magenta)%h%Creset -%C(red)%d%Creset %s %C(dim green)(%cr) [%an]\" --abbrev-commit -30
