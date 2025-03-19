Here's a structured homework assignment that will require students to practice using Git branches, logging history, reverting changes, resetting commits, checking out different states, and merging branches.  

---

## **Homework: Git Branching and History Management**  
### **Objective**  
The goal of this assignment is to help students gain hands-on experience with Git commands related to branches, commit history, and undoing changes.  

### **Prerequisites**  
- Git installed on the system  
- GitHub (or another Git remote repository) account  
- Basic understanding of Git concepts  

---

### **Instructions**  

1. **Initialize a New Git Repository**  
   - Create a new folder for your project:  
     ```sh
     mkdir git-homework && cd git-homework
     ```  
   - Initialize a Git repository inside the folder:  
     ```sh
     git init
     ```  

2. **Create and Modify Files**  
   - Create a file named `main.txt` and add the following content:  
     ```sh
     echo "This is the main branch file" > main.txt
     ```  
   - Stage and commit the file:  
     ```sh
     git add main.txt  
     git commit -m "Initial commit: added main.txt"
     ```  

3. **Create and Switch to a New Branch**  
   - Create a new branch named `feature-branch`:  
     ```sh
     git branch feature-branch
     ```  
   - Switch to the new branch:  
     ```sh
     git checkout feature-branch
     ```  
   - Modify `main.txt` to:  
     ```sh
     echo "This is the modified content in feature-branch" > main.txt
     ```  
   - Commit the changes:  
     ```sh
     git add main.txt  
     git commit -m "Modified main.txt in feature-branch"
     ```  

4. **View Commit History**  
   - Use the log command to see the commit history:  
     ```sh
     git log --oneline --graph --all
     ```  

5. **Resetting and Reverting**  
   - Create a new commit:  
     ```sh
     echo "This is an experimental line" >> main.txt
     git add main.txt  
     git commit -m "Added an experimental line"
     ```  
   - Use `git reset` to undo the last commit but keep the changes:  
     ```sh
     git reset --soft HEAD~1
     ```  
   - Check the commit history again:  
     ```sh
     git log --oneline
     ```  
   - If needed, use `git revert` to undo a specific commit while keeping history:  
     ```sh
     git revert <commit_hash>
     ```  

6. **Merge Feature Branch into Main**  
   - Switch back to `main` branch:  
     ```sh
     git checkout main
     ```  
   - Merge `feature-branch` into `main`:  
     ```sh
     git merge feature-branch
     ```  

7. **Push Changes to a Remote Repository**  
   - Create a repository on GitHub (or any remote Git service).  
   - Add the remote repository:  
     ```sh
     git remote add origin <repository_url>
     ```  
   - Push the changes:  
     ```sh
     git push -u origin main
     ```  

---

### **Submission**  
- Take screenshots of your terminal showing the execution of commands.  
- Provide the GitHub repository link.  
- Answer the following questions in a text file:  
  1. What is the difference between `git reset` and `git revert`?  
  2. How does `git merge` work? What happens when there is a conflict?  
  3. How can you switch between branches using Git?  

---

This assignment ensures students gain practical knowledge of Git while also reinforcing theoretical concepts. Let me know if you want any modifications! 🚀
