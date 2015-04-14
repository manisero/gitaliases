Useful git aliases and other options.
Feel free to copy them to your "C:\Users\\[user]\\.gitconfig" file (Windows).

```
[http]
	sslVerify = false
[credential]
	helper = store
[push]
	default = simple
[alias]
	# git:
	b = branch
	s = status -u .
	a = add -A .
	c = commit -m
	amend = commit --amend
	pul = pull
	pus = push

	co = checkout
	master = checkout master
	dev = checkout develop
	back = checkout -

	create = checkout -b
	delete = branch -d
	track = branch -u

	ignore = update-index --assume-unchanged
	unignore = update-index --no-assume-unchanged
	ignored = !git ls-files -v | grep "^[[:lower:]]"

	#macros:
	pulldev = !git dev && git pull && git back && git merge -
	pushdev = !git pulldev && git push && git dev && git merge - --no-ff && git push

# available colors: normal, black, red, green, yellow, blue, magenta, cyan and white
# color attributes: bold, dim, ul, blink and reverse
[color "status"]
	added = green bold
	changed = red bold
	untracked = red bold
[color "diff"]
	old = red bold
	new = green bold
```
