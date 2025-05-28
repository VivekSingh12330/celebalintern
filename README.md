Linux and Git Hands-On Assignment – Celebal Internship
This document contains step-by-step tasks and commands performed during the Linux and Git hands-on session under the Celebal Internship program.
Task 1: File Creation & Permission Management
Objective: Learn to create a file and assign different permissions to the owner, group, and others.

Commands Used:
- touch test1.txt       # Creates an empty file named test1.txt
- chmod 764 test1.txt   # Sets permissions: owner (read, write, execute), group (read, write), others (read)
- ls -l test1.txt       # Displays file permissions

Explanation:
Permission 764 means:
- Owner: 7 (read/write/execute)
- Group: 6 (read/write)
- Others: 4 (read only)

Task 2: Basic Linux Commands
Objective: Practice using basic Linux commands to manipulate files and directories.

Commands Used:
- mkdir week1          # Creates a directory named week1
- cd week1             # Navigates into week1 directory
- touch file1.txt      # Creates a new file inside week1
- ls -l                # Lists directory contents with details
- rm file1.txt         # Deletes file1.txt

Task 3: Directory Navigation & File Movement
Objective: Learn to move files across directories.

Commands Used:
- mkdir dirA dirB      # Create two directories
- touch dirA/demo.txt  # Create a text file inside dirA
- mv dirA/demo.txt dirB/  # Move demo.txt to dirB
- cd dirB              # Go to dirB
- ls                   # Verify file is moved

Task 4: User & Group Management
Objective: Learn to manage users and groups and assign access permissions.

Commands Used:
- groupadd devops             # Create a new group
- useradd vivek -G devops     # Create a new user and add to group
- mkdir /opt/test1            # Create a secure directory
- chown vivek:devops /opt/test1  # Change ownership to user and group
- chmod 770 /opt/test1        # Grant full access to owner and group

Task 5: Common Linux Commands
Objective: Practice essential Linux commands for scripting and automation.

Commands Used:
- pwd                         # Show present working directory
- echo "Hello" > hello.txt    # Write to a file
- cat hello.txt               # View file contents
- cp hello.txt copy.txt       # Copy file
- whoami                      # Display current user

Task 6: Git Installation & Configuration
Objective: Install Git and set global configuration.

Commands Used:
- dnf install git -y                   # Install Git
- git config --global user.name        # Set Git username
- git config --global user.email       # Set Git email

Task 7: Setup Remote Repository and Push to Main
Objective: Initialize local Git repo, link to remote, and push.

Commands Used:
- git init                              # Initialize local repository
- git remote add origin <repo-url>      # Link to remote repository
- touch README.md
- git add .
- git commit -m "Initial commit"
- git pull --rebase origin main         # Sync with remote
- git push -u origin main               # Push code

Task 8: Branching & Merging
Objective: Learn to work with branches.

Commands Used:
- git checkout -b feature               # Create and switch to 'feature' branch
- echo "Feature" > feature.txt
- git add feature.txt
- git commit -m "Added feature"
- git push -u origin feature            # Push to GitHub
- Merge via GitHub pull request

Task 9: Undo Last Commit / Remove File
Objective: Undo Git commits and remove files.

Commands Used:
- git reset --soft HEAD~1              # Undo last commit
- git rm unwanted.txt                  # Remove file
- git commit -m "Removed unwanted.txt"
- git push

Task 10: Merge Conflicts
Objective: Simulate and resolve Git merge conflicts.

Steps:
- Create same file with different content on two branches
- Merge branches
- Resolve conflicts manually
- git add <resolved-file>
- git commit -m "Resolved conflict"

Task 11: More Git Commands
Objective: Explore additional useful Git commands.

Commands Used:
- git log          # View commit history
- git status       # Show working tree status
- git stash        # Temporarily save changes
- git diff         # Show file changes

