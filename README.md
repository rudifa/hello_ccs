# hello_ccs
**An exercise in creating a new github repo from a TI CCS project**

1. Created a CCS project on local computer: /Users/rudifarkas/ti_workspace_v6_2/hello_ccs
In CCS Git perspective, created new repository in this directory.

```
hello_ccs $ git status
On branch master

 No commits yet

 Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.ccsproject
	.cproject
	.project
	.settings/
	Debug/
	main.c

nothing added to commit but untracked files present (use "git add" to track)
```

Created `.gitignore` to exclude `Debug`:

`Debug/*`

2. Add and commit

```
hello_ccs $ git add .
hello_ccs $ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   .ccsproject
	new file:   .cproject
	new file:   .gitignore
	new file:   .project
	new file:   .settings/org.eclipse.cdt.codan.core.prefs
	new file:   .settings/org.eclipse.cdt.debug.core.prefs
	new file:   .settings/org.eclipse.core.resources.prefs
	new file:   main.c

hello_ccs $ git commit -m "Initial commit"
[master (root-commit) f91fb69] Initial commit
 8 files changed, 214 insertions(+)
 create mode 100644 .ccsproject
 create mode 100644 .cproject
 create mode 100644 .gitignore
 create mode 100644 .project
 create mode 100644 .settings/org.eclipse.cdt.codan.core.prefs
 create mode 100644 .settings/org.eclipse.cdt.debug.core.prefs
 create mode 100644 .settings/org.eclipse.core.resources.prefs
 create mode 100644 main.c

hello_ccs $ git status
On branch master
nothing to commit, working tree clean
```

Now the CCS git perspective shows
```
  References
    HEAD [refs/heads/master] f91fb69 Initial commit
```


To push the new repo to GitHub ...

3. Created a new repository in GitHub web GUI: `https://github.com/rudifa/hello_ccs.git`

```
hello_ccs $ git remote add origin https://github.com/rudifa/hello_ccs.git
hello_ccs $ git remote -v
origin	https://github.com/rudifa/hello_ccs.git (fetch)
origin	https://github.com/rudifa/hello_ccs.git (push)
```

Now CCS git perspective shows under Remotes the equivalent of

```
hello_ccs $ git remote -v
origin	https://github.com/rudifa/hello_ccs.git (fetch)
origin	https://github.com/rudifa/hello_ccs.git (push)
```

4. Pushed to the new repository

```
hello_ccs $ git push --set-upstream origin master
Counting objects: 11, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (9/9), done.
Writing objects: 100% (11/11), 3.71 KiB | 1.86 MiB/s, done.
Total 11 (delta 0), reused 0 (delta 0)
To https://github.com/rudifa/hello_ccs.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
```




