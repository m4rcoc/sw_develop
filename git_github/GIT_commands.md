
# GIT commands

git config --global user.name "Marco Condori"
git config --global user.email marco.condori.b@gmail.com 

git init

git clone "url/local_path" "dir_to"


Set remote repository ()
git remote add origin "url/local_path"

Change remote repository:
git remote set-url origin "url/local_path"

View remote repository url/path
git remote -v

git log --oneline

(git status , git add -A , git commit -m "" )


# GITHUB config

Ssh config:
1. From Host PC, open a terminal and execute: 
ssh-keygen -t rsa -b 4096 -C "marco.condori.b@gmail.com" [^1]


2. Copy the content of the PUBLIC key:
cat /Users/mcondori/.ssh/id_rsa.pub

3. From GitHub home page (signed in), go to Settings / SSH and GPG keys, and create/add new SSH key
 
[^1]: *NOTE*: remember the .ssh path where the key will saved (should created a private and public key)
In my case, it will save them in /Users/mcondori/.ssh/id_rsa.pub

