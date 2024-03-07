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
### *Now you can work with this directory as local repository and send changes to the remote-one by

```bash
git add some-changes.txt
git commit -m "Changed some-changes.txt"
git push 
```
	
		 


