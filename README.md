Git Branching and Merging Workflow Practice

📌 Overview

This project demonstrates a complete Git workflow including branching, committing, pushing, and merging with conflict resolution using `main`, `dev`, and `test` branches.

---

🚀 Project Steps (1-line)

1. Create 3 files: index.html, style.css, app.py
2. Initialize Git repo and push files to GitHub (main branch)
3. Create a new branch "dev" from main
4. Edit index.html and style.css in dev branch, commit and push
5. Create another branch "test" from main
6. Edit style.css and app.py in test branch, commit and push
7. Switch to main branch and update files if needed, commit and push
8. Merge dev branch into main and resolve conflicts
9. Merge test branch into main and resolve conflicts
10. Verify final code in main branch

---

⚙️ Execution Steps (Commands)

🔹 Step 1: Create project files

```bash
mkdir git-project
cd git-project

touch index.html style.css app.py
```

---

🔹 Step 2: Initialize Git and push to GitHub

```bash
git init
git add .
git commit -m "Initial commit"

git branch -M main
git remote add origin <your-git-repo-url>
git push -u origin main
```

---

🔹 Step 3: Create dev branch

```bash
git branch dev
OR
git switch -c dev # Directly creates and switches to that branch.
OR
git checkout -b dev
```

---

🔹 Step 4: Modify files in dev branch

Edit files:

```html
vi index.html
OR
nano index.html

<!-- index.html -->
<h1>Dev Branch</h1>
```

```css
/* style.css */
body { background-color: lightblue; }
```

```bash
git add .
git commit -m "Updated index and style in dev"
git push origin dev
```

---

🔹 Step 5: Create test branch from main

```bash
git switch main
git switch -c test
```

---

🔹 Step 6: Modify files in test branch

```css
/* style.css */
body { background-color: lightgreen; }
```

```python
# app.py
print("Test branch changes")
```

```bash
git add .
git commit -m "Updated style and app in test"
git push origin test
```

---

🔹 Step 7: Update main branch

```bash
git switch main
```

(Optional edit any file)

```bash
git add .
git commit -m "Updated main branch"
git push origin main
```

---

🔹 Step 8: Merge dev into main

```bash
git merge dev
git push origin main
```

---

🔹 Step 9: Merge test into main

```bash
git merge test
```

If conflict occurs:

```bash
# Open conflicting file and fix manually
git add .
git commit -m "Resolved merge conflict"
git push origin main
```

---

🔹 Step 10: Verify

```bash
git branch
git log --oneline --graph
```

---

🧠 Key Concepts Learned

* Git initialization and setup
* Branch creation (`dev`, `test`)
* Commit and push workflow
* Merge strategies
* Conflict resolution
* Real-world Git workflow

---

💡 Conclusion

This project provides hands on practice with Git branching and merging strategies used in real development environments.

---
