# Celebalintern

---

````markdown
# 💻 Linux & Git Assignment – Celebal Internship

This document contains a comprehensive list of tasks completed during the internship project using **Linux** and **Git** tools.

---

## ✅ Task 1: Create a File and Assign Permissions

**Objective:** Create a file and assign read, write, and execute permissions to owner, group, and others.

### Commands Used:
```bash
touch file1.txt
ls -l file1.txt
chmod 754 file1.txt    # rwxr-xr--
ls -l file1.txt
````

📸 Screenshot:
`![Permissions Screenshot](screenshots/task1_permissions.png)`

---

## ✅ Task 2: Execute Basic Linux Commands

**Objective:** Learn and execute basic file and directory manipulation commands.

### Commands Used:

```bash
mkdir myfolder
cd myfolder
touch myfile.txt
ls
rm myfile.txt
cd ..
rmdir myfolder
```

📸 Screenshot:
`![Basic Commands Screenshot](screenshots/task2_basic.png)`

---

## ✅ Task 3: Navigate Directories and Move Files

**Objective:** Navigate through directories, list file contents, and move files.

### Commands Used:

```bash
mkdir folder1 folder2
touch folder1/testfile.txt
mv folder1/testfile.txt folder2/
ls folder2/
```

📸 Screenshot:
`![Navigation Screenshot](screenshots/task3_navigation.png)`

---

## ✅ Task 4: Create User and Group, Manage Permissions

**Objective:** Add new user/group and assign permissions.

### Commands Used:

```bash
groupadd devops
useradd vivek -G devops
mkdir /opt/test1
chown vivek:devops /opt/test1
chmod 770 /opt/test1
```

📸 Screenshot:
`![User Management Screenshot](screenshots/task4_user_group.png)`

---

## ✅ Task 5: More Linux Commands

**Objective:** Practice and understand various Linux commands.

### Examples Used:

```bash
whoami
uname -r
df -h
free -m
history
```

📸 Screenshot:
`![More Linux Commands Screenshot](screenshots/task5_more_commands.png)`

---

## ✅ Task 6: Introduction to Git – Installation and Basics

**Objective:** Learn Git installation and use basic Git commands.

### Commands Used:

```bash
dnf install git -y
git --version
git config --global user.name "Vivek Singh"
git config --global user.email "you@example.com"
git init
```

📸 Screenshot:
`![Git Init Screenshot](screenshots/task6_git_init.png)`

---

## ✅ Task 7: Setup Remote Repository and Push

**Objective:** Link local repo to GitHub and push code.

### Commands Used:

```bash
git remote add origin https://github.com/VivekSingh12330/celebalintern
git branch -M main
git add .
git commit -m "Initial commit"
git pull --rebase origin main
git push -u origin main
```

📸 Screenshot:
`![Git Push Screenshot](screenshots/task7_git_push.png)`

---

## ✅ Task 8: Create Branch, Push and Merge

**Objective:** Create a branch, commit and push changes, and merge to main.

### Commands Used:

```bash
git checkout -b feature1
echo "This is feature1" > feature1.txt
git add feature1.txt
git commit -m "Add feature1"
git push -u origin feature1
# Go to GitHub UI and create a Pull Request to merge `feature1` into `main`
```

📸 Screenshot:
`![Branch Merge Screenshot](screenshots/task8_merge.png)`

---

## ✅ Task 9: Undo Last Commit / Remove File

**Objective:** Undo the last commit or delete a remote file using CLI.

### Undo Last Commit (keep changes locally):

```bash
git reset --soft HEAD~1
```

### Delete File from Repo:

```bash
git rm unwanted.txt
git commit -m "Remove unwanted.txt"
git push
```

📸 Screenshot:
`![Undo Screenshot](screenshots/task9_undo.png)`

---

## ✅ Task 10: Merge Conflicts

**Objective:** Handle merge conflicts while merging branches.

### Scenario:

Modified the same file in both `main` and `feature2`, then tried to merge.

### Commands Used:

```bash
git checkout main
git merge feature2
# Conflict occurs
# Manually resolve conflict in the file
git add conflicted_file.txt
git commit -m "Resolved merge conflict"
```

📸 Screenshot:
`![Merge Conflict Screenshot](screenshots/task10_conflict.png)`

---

## ✅ Task 11: More Git Commands

**Objective:** Practice advanced Git commands.

### Commands Used:

```bash
git log --oneline
git diff
git stash
git stash apply
git tag v1.0
git show v1.0
```

📸 Screenshot:
`![More Git Screenshot](screenshots/task11_git_more.png)`

---

## 📌 Conclusion

These tasks gave hands-on experience in:

* Linux File Permissions
* User and Group Management
* Directory Navigation and Shell Commands
* Git Basics, Branching, Merging, and Conflict Resolution

Feel free to explore the repository, and check out the [GitHub Repo](https://github.com/VivekSingh12330/celebalintern) for source code and screenshots.

---

```

Let me know if you’d like a `.docx` or `.pdf` version of this as well.
```
