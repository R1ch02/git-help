# __Git helper__

## Create local repository

###  1) Make new directory and init git inside it

```bash
mkdir new-directory
cd new-directory
git init
```

###  for delete you can use
	
```bash
rm -r new-directory
```

###  2) Bond your local repository with remote one

```bash
git remote add origin [your link ssh or https]
```

### 3) If you prefer ssh you can generate key and add it in the github or gitlab
	
```bash
ssh-keygen -t ed25519
```
	
_-t is letting us to show the type of the encryption_
	
You can use cat to print ssh-key.pub and copy it yourself with _Ctrl+Alt+C_

```bash
cd ~
cd .ssh
cat ssh-key.pub
```
### Now you can work with this directory as local repository and send changes to the remote-one by

```bash
git add some-changes.txt
git commit -m "Changed some-changes.txt"
git push 
```
	
### Hash, logs, HEAD

#### Every commit has it's own hash. Hash is like an id to commit so you can track changes with it.

#### To find commit you need. You can use command _git log_

```bash
git log
```

Or git log --oneline to see every commit as 1 line

```bash
git log --oneline
```

#### Also there is a term HEAD. HEAD is a pointer to the last commit you have done in this branch.

You can check information about it by command _cat_

```bash
cat ./git/HEAD
```

###Stages of data

There is 4 stages that you can work with

#### 1) untracked 

git doesn't track changes in this file

#### 2) tracked

git tracks changes in the this file

#### 3) staged

Also tracked. You added file on the stage by command _git add_

```bash
git add README.md
```

Next commit will have its changes

#### 4)modified

Also tracked. Something changed inside this file, and next commit will updated to new version.

