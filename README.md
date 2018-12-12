# git-starter
This repo contains simple guideline to the basic git commands and usage

For those who cannot live without GUI tools:

### Graphical userinterface
Sourcetree is a GUI interface to git.
You can download it form [here](https://www.sourcetreeapp.com/)
And follow this [tutorial](https://confluence.atlassian.com/display/BITBUCKET/Tutorial%3A+Learn+SourceTree+with+Bitbucket+Cloud) to learn how to use SourceTree.


Learn more about git on github:

### Understand git

Please go to github [training page](https://services.github.com/on-demand/intro-to-github/) to learn the basics about github and git.

A number of [videos are available on github learning path](https://services.github.com/on-demand/resources/learning-path/).

[Learn git](https://lab.github.com/courses?tag=Git)

Following is the [github cheatsheet](https://services.github.com/on-demand/downloads/github-git-cheat-sheet/)

## Let us do some git commands

create a new branch and enter this branch to start working:

``` bash
 $ git checkout -b gitbranch
```

So the above command create your new working branch.
you can work on your code in this branch for the chosen feature.
When you have completed the code, you have to check it into git.

first do local commits:

```bash
$ git add .
$ git commit -m "commit description"
```

Then you can check status:

```bash
$ git staus

On branch gitcommands
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

the above outpus is before git commit.

To merge your changes with master branch, you must checkout the master

```bash
$ git checkout master
```

now you have to merge your code:

```bash 
$ git merge gitbranch master
```

gitbranch was your branch. Now they are merged to master and you have to run local test to verify that all is working.

```bash
$ git push
```

will push your code to the github master branch.

you can view the git tree
```bash
$ git tree
*   eabba75 (HEAD -> master, origin/master, origin/HEAD) Merge branch 'newbranch1'
|\
| * 770dbab (newbranch1) added a title
* | 8b31b78 (newbranch2) added new branch 2 file
|/
* 01c2317 added new branch1 file
* 4099fde (gitbranch) added brach info
* 4240806 first commit to master
* 8cc3ed8 Initial commit
```