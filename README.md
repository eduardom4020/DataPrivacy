# Data Privacy

This repository is where we will put all works made at the opitative subject of Data Privacy, taught in the Federal University of Ceará (UFC) by professor Javam Machado.

**This is actualy a development repository, and all final results obtained here will be transposed to Professor's repositories made to this subject. Lately we will release the link to that.**


# To The Contributors Of This Repository

The are a production line with has steps that anybody needs to follow.

## Don't Have The Repository Downloaded In Actual Machine

First of all you need to clone this repository by navigate to an folder of your choice in this machine and call the command bellow.

```
	git clone https://github.com/eduardom4020/DataPrivacy.git
``` 

## Before Start Working

If this repository is already downloaded from your computer, you should call commands bellow before start programming.

```
	git status
```

In the response you will see **On branch BranchName**. Example: On branch master, where BranchName = master.

```
	git pull origin BranchName
```

This will keep the last branch you worked at, up to date. Now go to the master.

```
	git checkout master && git pull origin master
```

And if you have a new job to do, you will need to create a new branch with name convention bellow:

* Dev-JobName : For creating new functionalities, where JobName is the name you wish to give to your actual objective. Example: Dev-Write-Tutorial.


Now execute only one of the commands bellow:

```
	git checkout -b NewBranchName
```
If the job has no branch created yet.
**Before execute command above, make sure that you are in branch master and have executed pull command.**

Or

```
	git checkout BranchName && git pull origin BranchName && git merge master
```
**Check and correct all the merge conflicts if it happens**

## Working

You can now work freely, but ever make changes only in your branch, so don't call any command checkout in this stage, only if it's truly necessary.
**You can use git status to make sure that you are always in the same branch.**

Time by time you can push changes to this branch. Normaly you must make this before an uncertainly change of after the functionality is working well. To push use the following command:

```
	git add . && git commit -m "Put some commit message here" && git push origin BranchName
```

In **Put some commit message here** you need to put commit messages with the pattern:

* CREATED: Message -> Used only when a new branch is created. You need to specify why this branch was created.
* DOING: Message -> Modifications you are acctualy making.
* DONE: Message -> Last modification that is already made.
* TODO: Message -> An modification that needs to be make.
* BLOCKED: Message -> Modification that you cannot make and why.

**You must append these patterns in your commit message if necessary. Example: git add . && git commit -m "CREATED: Some reason DOING: One think" && git push origin BranchName**

**You can push various commits with same message, if modifications aren't that big.**

## Testing

After finish your job and make local revision (check if all of your latest modifications are working well) you need to integrate that with the branch named **Test.**

To do this run the following steps:

```
	git pull origin WorkedAtBranchName
```

Just for make sure that the branch you already have finished to work at isn't changed by other member at the same time that you were making your modifications.

```
	git checkout Test && git pull origin Test
```

Now this is to make sure that Test will be up to date.

```
	git merge WorkedAtBranchName
```

Resolve merge conflicts if was necessary.

```
	git push origin Test
```

**If you resolve a merge conflict you will need to run the command bellow instead of the command above:**

```
	git add . && git commit -m "Resolved Merge Conflict" && git push origin Test
```

When you do this, you need to contact your partners and wait for their aprove.

## Realeasing

After the crew made the tests, you can repeat the process above, but this time from Test to master:

```
	git pull origin Test
```

```
	git checkout master && git pull origin master
```

```
	git merge Test
```

```
	git push origin master
```

**If you resolve a merge conflict you will need to run the command bellow instead of the command above:**

```
	git add . && git commit -m "Resolved Merge Conflict" && git push origin master
```

### Members

Eduardo Melo
Victor Vieira
Igor Moura
