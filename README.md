
# 📘 Celebal Internship 

## 🗂️ Week 1 Tasks: Linux Essentials, Git Basics & Version Control

---

### 🔹 Task 1: File Creation & Permission Management

**Objective:**  

Create a file, assign read, write, and execute permissions to owner, group, and others. Practice with `chmod`.

**Commands & Output:**

```bash
[root@localhost week1] touch myfile.txt
[root@localhost week1] ls -l myfile.txt
-rw-r--r--. 1 root root 0 May 28 15:06 myfile.txt

[root@localhost week1] chmod 700 myfile.txt
[root@localhost week1] ls -l myfile.txt
-rwx------. 1 root root 0 May 28 15:06 myfile.txt

[root@localhost week1] chmod 640 myfile.txt
[root@localhost week1] ls -l myfile.txt
-rw-r-----. 1 root root 0 May 28 15:06 myfile.txt
```

**Explanation:**  
- `chmod`: Changes file permissions using symbolic or numeric modes.
- `touch myfile.txt`: Creates an empty file named `myfile.txt`.
- `chmod 700`: Gives full permissions (read, write, execute) to the owner only.
- `chmod 640`: Sets read/write for owner, read for group, and no permissions for others.

---

### 🔹 Task 2: Basic Linux File Commands

**Objective:**  

Practice basic file/directory commands: `ls`, `cd`, `mkdir`, `rm`, `touch`, etc.

**Commands:**

```bash
[root@localhost ~] mkdir test_folder
[root@localhost ~] cd test_folder
[root@localhost test_folder] touch file1.txt
[root@localhost test_folder] ls
file1.txt
[root@localhost test_folder] rm file1.txt
[root@localhost test_folder] cd ..
[root@localhost ~]# rmdir test_folder
```

**Explanation:**  
- `mkdir`: Creates a new directory.
- `cd`: Changes directory.
- `touch`: Creates an empty file.
- `rm`: Deletes files.
- `rmdir`: Deletes an empty directory.

---

### 🔹 Task 3: File Navigation & Moving Files

**Objective:**  

Move files between folders and navigate using CLI command mv.

**Commands:**

```bash
[root@localhost ~]# mkdir test1 test2
[root@localhost ~]# touch test1/file.txt
[root@localhost ~]# mv test1/file.txt test2/
[root@localhost ~]# cd /root/celebal/week1/test2
[root@localhost folderB]# ls
file.txt
```

**Explanation:**  
- `mv`: Moves file from one folder to another.
- `cd` & `ls`: Navigate and list contents.

---

### 🔹 Task 4: User and Group Management

**Objective:**  
Create user/group and set proper file ownership and access.

**Commands:**

```bash
[root@localhost ~]# groupadd devops
[root@localhost ~]# useradd -m -G devops dev
[root@localhost ~]# passwd dev
[root@localhost ~]# usermod -aG wheel dev
[root@localhost week1]# userdel -r dev
[root@localhost week1]# id dev
id: ‘dev’: no such user

[root@localhost week1]# chown vivek:devops test1/
[root@localhost week1]# ls -l
total 0
-rwxrwxrwx. 1 root  root    0 May 28 15:06 myfile.txt
drwxr-xr-x. 2 vivek devops 25 May 28 17:11 test1
drwxr-xr-x. 2 root  root   25 May 28 17:10 test2
[root@localhost week1]# chmod 770 test2/
[root@localhost week1]# ls -l
total 0
-rwxrwxrwx. 1 root  root    0 May 28 15:06 myfile.txt
drwxr-xr-x. 2 vivek devops 25 May 28 17:11 test1
drwxrwx---. 2 root  root   25 May 28 17:10 test2

[root@localhost week1]# userdel -r vivek 
[root@localhost week1]# id vivek
id: ‘vivek’: no such user
[root@localhost week1]# groupdel devops
```

**Explanation:**  

* `groupadd <groupname>`
  ➤ Creates a new user group.

* `useradd -m -G <groupname> <username>`
  ➤ Adds a new user with a home directory and adds them to the specified group.

* `passwd <username>`
  ➤ Sets a password for the user.

* `usermod -aG wheel <username>`
  ➤ Adds the user to the `wheel` group for administrative (sudo) access.

* `userdel -r <username>`
  ➤ Deletes the user and their home directory.

* `id <username>`
  ➤ Displays user ID, group ID, and group membership. Returns an error if the user doesn't exist.

* `chown <user>:<group> <directory>`
  ➤ Changes ownership of a directory to the specified user and group.

* `chmod 770 <directory>`
  ➤ Grants full permissions (read, write, execute) to owner and group; no permissions to others.

* `groupdel <groupname>`
  ➤ Deletes the specified group.

---

### 🔹 Task 5: Exploring Linux Commands

**Objective:**  
Explore basic commands to view and manage content.

**Commands:**

```bash
[root@localhost ~]# echo "Welcome to Linux" > file.txt
[root@localhost ~]# cat file.txt
Welcome to Linux

[root@localhost ~]# head -n 1 file.txt
Welcome to Linux

[root@localhost ~]# tail -n 1 file.txt
Welcome to Linux

[root@localhost week1]# pwd
/root/celebal/week1
[root@localhost week1]# w
 17:22:52 up  3:45,  1 user,  load average: 0.01, 0.01, 0.00
USER     TTY        LOGIN@   IDLE   JCPU   PCPU WHAT
root     tty2      13:39    3:49m  0.08s  0.08s /usr/libexec/gnome-session-binary

[root@localhost ~]# whoami
root
```

**Explanation:**  
- `echo`: Writes text to file.
- `cat`, `head`, `tail`: View file contents.
- `whoami`: Displays current user.
- `pwd`: Prints the current working directory path.
- `w`:Displays who is logged in and what they are doing.

---

### 🔹 Task 6: Git Installation & Initialization

**Objective:**  
Install Git and configure it for the first time.

**Commands:**

```bash
[root@localhost ~]# dnf install git -y
[root@localhost ~]# git config --global user.name "Vivek Singh"
[root@localhost ~]# git config --global user.email "vivek@example.com"
[root@localhost week1]# git config --list
user.name=Vivek Shekhawat
user.email=shekhawatvsshp9694@gmail.com
[root@localhost week1]# mkdir git-demo
[root@localhost week1]# cd git-demo/
[root@localhost git-demo]# git init
```

**Explanation:**

* `dnf install git -y`: Installs Git package without confirmation.
* `git config --global user.name "Your Name"`: Sets global Git username.
* `git config --global user.email "youremail@example.com"`: Sets global Git email.
* `git config --list`: Lists current Git configuration.
* `mkdir git-demo`: Creates a directory named `git-demo`.
* `cd git-demo/`: Changes directory to `git-demo`.
* `git init`: Initializes a new Git repository in the current folder.

---

### 🔹 Task 7-10 : Remote Repo Setup & Initial Push,Git Branching & PR Merge,Undo Commit / File Removal,Merge Conflict

```bash
echo "Hello Git" > file1.txt
````

* Creates a file named `file1.txt` with the text "Hello Git".

```bash
git add file1.txt
```

* Stages `file1.txt` to be committed.

```bash
git commit -m "Initial commit"
```

Output:

```
[master (root-commit) d2da673] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 file1.txt
```

* Commits staged changes with the message "Initial commit".

```bash
git status
```

Output:

```
On branch master
nothing to commit, working tree clean
```

* Shows there are no changes to commit.

```bash
git log
```

Output:

```
commit d2da673f859cb3a3d02acab248b9387a93346ed3 (HEAD -> master)
Author: Vivek Shekhawat <shekhawatvsshp9694@gmail.com>
Date:   Wed May 28 17:39:42 2025 +0530

    Initial commit
```

* Displays commit history.

```bash
git remote add origin https://github.com/VivekSingh12330/celebalintern
```

* Adds a remote repository named `origin`.

```bash
git branch -M main
```

* Renames current branch from `master` to `main`.

```bash
git push -u origin main
```

Output (first attempt):

```
remote: Support for password authentication was removed on August 13, 2021.
fatal: Authentication failed for 'https://github.com/VivekSingh12330/celebalintern/'
```

* Push failed due to password authentication being disabled.

Output (second attempt):

```
! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/VivekSingh12330/celebalintern'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally.
```

* Push rejected because remote has commits that local branch doesn’t.

```bash
git pull --rebase origin main
```

Output:

```
Successfully rebased and updated refs/heads/main.
```

* Fetches remote changes and rebases local commits on top.

```bash
git push -u origin main
```

Output:

```
To https://github.com/VivekSingh12330/celebalintern
   9ed6e65..117d53e  main -> main
branch 'main' set up to track 'origin/main'.
```

* Push successful, sets upstream tracking for `main`.

```bash
git checkout -b feature-branch
```

Output:

```
Switched to a new branch 'feature-branch'
```

* Creates and switches to `feature-branch`.

```bash
echo "This is a feature branch file" > feature.txt
git add feature.txt
git commit -m "Added feature.txt in feature-branch"
```

Output:

```
[feature-branch f04475a] Added feature.txt in feature-branch
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt
```

* Adds and commits new file in feature branch.

```bash
git push -u origin feature-branch
```

Output:

```
To https://github.com/VivekSingh12330/celebalintern
 * [new branch]      feature-branch -> feature-branch
branch 'feature-branch' set up to track 'origin/feature-branch'.
```

* Pushes feature branch to remote and tracks it.

```bash
git checkout main
```

Output:

```
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```

* Switches back to main branch.

```bash
git merge feature-branch
```

Output:

```
Updating 117d53e..f04475a
Fast-forward
 feature.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt
```

* Merges feature branch into main with fast-forward.

```bash
git push origin main
```

* Pushes merged changes to remote main branch.

```bash
git reset --soft HEAD~1
```

* Moves HEAD back one commit but keeps changes staged.

```bash
git rm unwantedfile.txt
```

Output:

```
fatal: pathspec 'unwantedfile.txt' did not match any files
```

* File doesn't exist, so removal failed.

```bash
echo "This is an unwanted file" > unwantedfile.txt
git add unwantedfile.txt
git commit -m "Added file"
```

Output:

```
[main 89d141d] Added file
 2 files changed, 2 insertions(+)
 create mode 100644 feature.txt
 create mode 100644 unwantedfile.txt
```

* Added and committed unwantedfile.txt.

```bash
git push -u origin main
```

Output:

```
! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/VivekSingh12330/celebalintern'
```

* Push rejected because local branch is behind remote.

```bash
echo "Line B from main" > conflict.txt
git add conflict.txt
git commit -m "Main: Add Line B"
```

Output:

```
[main 6d3dbb5] Main: Add Line B
 1 file changed, 1 insertion(+)
 create mode 100644 conflict.txt
```

* Added new file conflict.txt in main.

```bash
git merge feature-branch
```

Output:

```
Merge made by the 'ort' strategy.
```

* Merged feature branch with main, auto-resolving conflicts.

```bash
git push origin main
```

Output:

```
To https://github.com/VivekSingh12330/celebalintern
   f04475a..4018e59  main -> main
```

* Pushed merged commits to remote.

```bash
git rm unwantedfile.txt
git commit -m "Removed unwantedfile.txt"
```

Output:

```
[main 054848c] Removed unwantedfile.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 unwantedfile.txt
```

* Removed unwantedfile.txt and committed removal.

```bash
git push origin main
```

Output:

```
To https://github.com/VivekSingh12330/celebalintern
   4018e59..054848c  main -> main
```

* Pushed removal commit to remote main branch.

---

### 🔹 Task 11: Common Git Commands

```bash
git log          # Shows commit history
git status       # Shows current changes
git diff         # Shows file differences
git stash        # Temporarily saves changes
git clone <url>  # Clones repo
git pull origin main  # Updates local repo
```

---

## Screenshots

### 1.
![1](screenshots/1.png).

### 2. Registration Successfully
![2](screenshots/2.png).

### 3. Login
![Login](screenshots/3_Login.png)

### 4. Dashboard
![Dashboard](screenshots/4_Dashboard.png)

### 5. Deposit Action
![Deposit Action](screenshots/5_Deposit_action.png)

### 6. Deposit Action Successfully
![Deposit Action Successfully](screenshots/6_Deposit_action_Successfully.png)

### 7. Withdraw Action
![Withdraw Action](screenshots/7_withdraw_action.png)

### 8. Withdraw Action Successfully
![Withdraw Action Successfully](screenshots/8_withdraw_action_Successfully.png)

### 9. Transfer Action
![Transfer Action](screenshots/9_transfer_action.png)

### 10. Transfer Action Successfully
![Transfer Action Successfully](screenshots/10_transfer_action_successfully.png)

### 11. Receiver Account
![Receiver Account](screenshots/11_receiver_account.png)

### 12. Logout Successfully
![Logout Successfully](screenshots/12_logout_successfully.png)


---
