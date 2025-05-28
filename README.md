
# 📘 Celebal Internship – Week 1: Linux & Git Assignment

## 🗂️ Week 1 Tasks: Linux Essentials, Git Basics & Version Control

---

### 🔹 Task 1: File Creation & Permission Management

**Objective:**  
Create a file and practice assigning permissions using `chmod`.

**Commands & Output:**

```bash
[root@localhost week1]# touch myfile.txt
[root@localhost week1]# ls -l myfile.txt
-rw-r--r--. 1 root root 0 May 28 15:06 myfile.txt

[root@localhost week1]# chmod 700 myfile.txt
[root@localhost week1]# ls -l myfile.txt
-rwx------. 1 root root 0 May 28 15:06 myfile.txt

[root@localhost week1]# chmod 640 myfile.txt
[root@localhost week1]# ls -l myfile.txt
-rw-r-----. 1 root root 0 May 28 15:06 myfile.txt
```

**Explanation:**  
- `touch myfile.txt`: Creates an empty file named `myfile.txt`.
- `chmod 700`: Gives full permissions (read, write, execute) to the owner only.
- `chmod 640`: Sets read/write for owner, read for group, and no permissions for others.

---

### 🔹 Task 2: Basic Linux File Commands

**Objective:**  
Learn basic file/directory operations.

**Commands:**

```bash
[root@localhost ~]# mkdir test_folder
[root@localhost ~]# cd test_folder
[root@localhost test_folder]# touch file1.txt
[root@localhost test_folder]# ls
file1.txt
[root@localhost test_folder]# rm file1.txt
[root@localhost test_folder]# cd ..
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
Move files between folders and navigate using CLI.

**Commands:**

```bash
[root@localhost ~]# mkdir folderA folderB
[root@localhost ~]# touch folderA/fileA.txt
[root@localhost ~]# mv folderA/fileA.txt folderB/
[root@localhost ~]# cd folderB
[root@localhost folderB]# ls
fileA.txt
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
[root@localhost ~]# useradd -G devops vivek
[root@localhost ~]# mkdir /opt/test1
[root@localhost ~]# chown vivek:devops /opt/test1
[root@localhost ~]# chmod 770 /opt/test1
```

**Explanation:**  
- `groupadd` & `useradd`: Create group and user.
- `chown`: Assign user and group ownership.
- `chmod 770`: Full access to owner/group, none to others.

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

[root@localhost ~]# whoami
root
```

**Explanation:**  
- `echo`: Writes text to file.
- `cat`, `head`, `tail`: View file contents.
- `whoami`: Displays current user.

---

### 🔹 Task 6: Git Installation & Initialization

**Objective:**  
Install Git and configure it for the first time.

**Commands:**

```bash
[root@localhost ~]# dnf install git -y
[root@localhost ~]# git config --global user.name "Vivek Singh"
[root@localhost ~]# git config --global user.email "vivek@example.com"
[root@localhost ~]# git init
```

**Explanation:**  
- `git config`: Sets username and email.
- `git init`: Initializes a local Git repository.

---

### 🔹 Task 7: Remote Repo Setup & Initial Push

**Objective:**  
Connect local repo to GitHub and push initial commit.

**Commands:**

```bash
[root@localhost ~]# touch README.md
[root@localhost ~]# echo "# Celebal Internship" > README.md
[root@localhost ~]# git add .
[root@localhost ~]# git commit -m "Initial commit"
[root@localhost ~]# git remote add origin https://github.com/VivekSingh12330/celebalintern
[root@localhost ~]# git branch -M main
[root@localhost ~]# git pull --rebase origin main  # in case of conflict
[root@localhost ~]# git push -u origin main
```

**Explanation:**  
- `git remote add`: Links repo to GitHub.
- `git push`: Uploads code to GitHub.

---

### 🔹 Task 8: Git Branching & PR Merge

**Objective:**  
Work with branches and merge them via PR.

**Commands:**

```bash
[root@localhost ~]# git checkout -b feature-1
[root@localhost ~]# echo "Feature added" > feature.txt
[root@localhost ~]# git add .
[root@localhost ~]# git commit -m "Added feature"
[root@localhost ~]# git push -u origin feature-1
```

**Next:**  
Go to GitHub → Create Pull Request → Merge to main

---

### 🔹 Task 9: Undo Commit / File Removal

**Commands:**

```bash
# Undo last commit but keep changes
[root@localhost ~]# git reset --soft HEAD~1

# Remove file from repo
[root@localhost ~]# git rm unwanted.txt
[root@localhost ~]# git commit -m "Removed unwanted.txt"
[root@localhost ~]# git push
```

---

### 🔹 Task 10: Merge Conflict

**Objective:**  
Simulate and resolve a Git merge conflict.

**On `main`:**

```bash
[root@localhost ~]# echo "Hello from main" > conflict.txt
[root@localhost ~]# git add .
[root@localhost ~]# git commit -m "main update"
[root@localhost ~]# git push
```

**On `feature` branch:**

```bash
[root@localhost ~]# git checkout -b conflict-branch
[root@localhost ~]# echo "Hello from branch" > conflict.txt
[root@localhost ~]# git add .
[root@localhost ~]# git commit -m "branch update"
[root@localhost ~]# git push origin conflict-branch
```

Now merge PR via GitHub → Resolve conflicts → Commit.

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

## ✅ All Tasks Completed

```md
![Task Screenshot](screenshots/task1.png)
```

---
