# GITCommandsForUse
git commands for hack


# Git basics:

# Git UndoLast Push

First you need to determine the revision ID(SHA ID) of the last known commit. You can use HEAD^ or HEAD~{1} if you know you need to reverse exactly one commit.

git reset --hard <revision_id_of_last_known_good_commit>

git push --force

# Branch Creation

git branch

git checkout -b branch_name (branch creation)

git branch (number of branch in current desktop)


git checkout master (moving back to master)

git merge branchname (branchname from which it will take a code and merge it to the current branch(eg. Master))  
current branch means you are right now in


# GitBranch Push:

Git checkout –b mybranchname

Git commit 

Git push origin mybranchname



# Git add:

git add --a stages All (mixture of ‘.’ And ‘-u’)

git add . stages new and modified, without deleted

git add -u stages modified and deleted, without new  (-u shortcut to learn: u for update.. will not include new untrack change)

# Track branch:

Git branch –set-upstream-to=origin/master


# How to make GitLocal Repo:

remote(server)   please dnt confuse with remote.. this is just a different PC or server u can say

git init --bare

or

git --bare init

local

git init

create any file which you want to push(let say abc.txt)

git add .

git commit -am "msg"(this didnot put your abc.txt on server-- just history what all commited in local)


now i want to add that to server(remote)

git remote add remotename path(//Ajay-pc/repo)

git push remotename master


git pull remotename master


# Issues


# 1)
Your branch and 'origin/master' have diverged,and have 3 and 8 different commits each, respectively.

(use "git pull" to merge the remote branch into yours)

solution
git fetch origin
git reset --hard origin/master
