
# GIT commands

```console
git config --global user.name "Marco Condori"
git config --global user.email marco.condori.b@gmail.com 

git init

git clone "url/local_path" "dir_to"

git log --oneline
git status
git add -A
git commit -m ""
```


Set remote repository ()
```console
git remote add origin "url/local_path"
```

Change remote repository:
```console
git remote set-url origin "url/local_path"
```

View remote repository url/path
```console
git remote -v
```


# GITHUB config

Ssh config:
1. From Host PC, open a terminal and execute: 
ssh-keygen -t rsa -b 4096 -C "marco.condori.b@gmail.com" [^1]


2. Copy the content of the PUBLIC key:
cat /Users/mcondori/.ssh/id_rsa.pub

3. From GitHub home page (signed in), go to Settings / SSH and GPG keys, and create/add new SSH key
 
[^1]: *NOTE*: remember the .ssh path where the key will saved (should created a private and public key)
In my case, it will save them in /Users/mcondori/.ssh/id_rsa.pub


# Procedure for new repositories

1.  Create a github repository (include README.md)
2.  Clone the repository on Host PC [^1]
3.  Add/copy sources for the first commit (Initial version of the project)
4.  Check in local that the remote repository is OK
```console
git remote -v
```
5.  Push and check from Github [^2]
```console
git push -u origin main
```


[^1]: In this point, you should have correctly configured the ssh configuration
[^2]: Be careful with the name of the branch: master <-> main (to rename: *git branch -m master main* )

# Example of .gitignore:

The typical example is for node_modules folder:

1. Create the file .gitignore in the workspace folder and put:
```console
node_modules
```
