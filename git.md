Git tasks:

1. local repository

- &quot;git init&quot;   using this command we will create local repository in our machine.

create file

touch a.txt  b.txt

2. config the user name and mail

git config --global user.email &quot; [_devops.ya@gmail.com_](mailto:devops.ya@gmail.com)&quot;

git config --global user.name &quot;malli333&quot;

 user.email=devops.ya

user.name=malli333

core.repositoryformatversion=0

core.filemode=true

core.bare=false

core.logallrefupdates=true

3. enter the data into that files

cat a.txt

Hi Team Ninja

..

cat &gt;&gt; b.txt

..

root@samhith:/opt/git# cat b.txt

This is VCS:Git

4. create bracnh

root@samhith:/opt/git# git branch

\* master

  ninja

5. Edit the b.txt

root@samhith:/opt/git# cat b.txt

&quot;This is VCS:Git. This is ninja branch

6. Rename the b.txt to c.txt

root@samhith:/opt/git# git mv b.txt c.txt

root@samhith:/opt/git# ls

a.txt  c.txt

7. Remove the the c.txt

root@samhith:/opt/git# rm c.txt

root@samhith:/opt/git# ls

a.txt

8. create file text.

root@samhith:/opt/git# ls

a.txt  text.txt

9. add the file

root@samhith:/opt/git# git status

On branch ninja

Changes to be committed:

  (use &quot;git reset HEAD &lt;file&gt;...&quot; to unstage)

 new file:   text.txt

10. remove the text.txt in stagning area

root@samhith:/opt/git# git reset HEAD text.txt

root@samhith:/opt/git# git status

On branch ninja

Untracked files:

  (use &quot;git add &lt;file&gt;...&quot; to include in what will be committed)

 text.txt

11.create github account

user : [devops.ya@gmail.com](mailto:devops.ya@gmail.com)

12. Fork the ot/traning in my account

[git](https://github.com/malli333/git)

Forked from [ot-training/git](https://github.com/ot-training/git)

this will contain git related stuff

13. clone the repo

root@samhith:/opt/git# git clone https://github.com/malli333/git-.git

Cloning into &#39;git-&#39;...

remote: Counting objects: 3, done.

remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0

Unpacking objects: 100% (3/3), done.

Checking connectivity... done.

14 .create vajpayee.txt file and add that file commit the file and push into remote repo.

|   | [vajpayee1.txt](https://github.com/malli333/git-/blob/master/vajpayee1.txt) | [commited by malli](https://github.com/malli333/git-/commit/01386602ab8baeef865dd749f9b6dc46f1aee46b) |   |
| --- | --- | --- | --- |

15 . create multiple branchs.

[ops](https://github.com/malli333/git-/tree/ops) Updated by malli333

1

1

[ninja](https://github.com/malli333/git-/tree/ninja) Updated by malli333

1

1

15.using script clone the remote.

#/bin/bash

repository=&quot;https://github.com/malli333/git-.git&quot;

localFolder=&quot;/opt/git&quot;

git clone $repository&quot; &quot;$localFolder

16. use ssh clone the repo

\* for this first i generate the ssh-keygen after that key add into github then go to git using below command i clone the repo.

 git clone git@github.com:malli333/ops.git

Cloning into &#39;ops&#39;...

remote: Counting objects: 6, done.

remote: Compressing objects: 100% (3/3), done.

remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0

Receiving objects: 100% (6/6), done.

Checking connectivity... done.

17.create a tag and push the tag into our remote repo.

 git tag v1.1

### [v1.1](https://github.com/malli333/git-/releases/tag/v1.1)

- [72e8a72](https://github.com/malli333/git-/commit/72e8a728fd0ed939822a5e70795bc2fe76eb0b06)
- [zip](https://github.com/malli333/git-/archive/v1.1.zip)
- [gz](https://github.com/malli333/git-/archive/v1.1.tar.gz)

18. checkout to tag.

root@samhith:/opt/git/git-# git checkout -b  origin/remote\_tag\_v1.1Switched to a new branch &#39;origin/remote\_tag\_v1.1&#39;

19.create alias name for git commands.

git config –global alias.c=commit

git config –global alias.st=status

git config –global alias.a=add

20. using &quot;git stash&quot; we will store into teampary memory.

21. i created github and gitlab and bitbucket accounts.

Gitub : 1.github is open source

2. easy to bugtracking .

3.find our project easliy.

4.high compatability.

Git lab :

1. open source

2. free hosting

3. LDAP integration.

Bitbucket:

1. authentication via github

2. integrated jira tools

22. user permission and repository permissions

go setting – interaction limts- limittoexistinguser

repo permissions: go setting – interaction limts – limit to repository collaborators

23. create two repository.

      1.ops 2.tree

24. create two braches in that using one text file edit the data in one file after that merge that getting

conflict issue.

 This branch has conflicts that must be resolved

Use the [web editor](https://github.com/malli333/tree/pull/1/conflicts) or the to resolve conflicts.

#### Conflicting files

text

create traning purpose

&lt;&lt;&lt;&lt;&lt;&lt;&lt; tree

mallikarjuna

=======

hi this mallikarjuna

&gt;&gt;&gt;&gt;&gt;&gt;&gt; master

reslove the issue

#### Continuous integration has not been set up

Several apps [are available](https://github.com/marketplace/category/continuous-integration) to automatically catch bugs and enforce style.

### This branch has no conflicts with the base branch

Merging can be performed automatically.
