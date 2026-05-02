Great—this lab adds an important layer of *professional discipline*.

So far they’ve learned:

* Save ✔️
* Track ✔️
* Experiment ✔️
* Merge ✔️

Now we teach:

> **“Not everything should be tracked”**

---

# 🔵 LAB 5: Ignoring Unnecessary Files using `.gitignore`

---

# 🎯 LAB OBJECTIVE

> “Learn how to prevent unwanted files from being tracked by Git.”

---

# 🎯 PROBLEM WE ARE SOLVING

In real academic workflows:

* Systems generate temporary files
* Editors create hidden files
* Downloads/logs clutter folders

Examples:

* `.DS_Store` (Mac)
* `temp.txt`
* backup files
* compiled outputs

---

👉 If not handled:

* Repository becomes messy
* Unnecessary files get committed
* Confusion increases

---

# 💡 WHAT THIS LAB WILL ACHIEVE

By the end, participants will:

* Understand `.gitignore`
* Prevent files from being tracked
* Keep repository clean

---

# ⏱️ TIME: ~25–30 minutes

---

# 🧪 STEP-BY-STEP INSTRUCTIONS (FOR PARTICIPANTS)

---

## 🧩 Step 1: Ensure You Are in Repo

```bash id="z5h2fs"
cd my-academic-profile
```

---

## 🧩 Step 2: Create Unwanted Files

```bash id="1p4h5l"
touch temp.txt
touch notes.log
```

---

## 🧩 Step 3: Check Status

```bash id="m3z1y7"
git status
```

👉 You will see:

* temp.txt
* notes.log
  as **untracked files**

---

## 🧩 Step 4: Create `.gitignore` File

```bash id="d5y1k7"
touch .gitignore
```

---

## 🧩 Step 5: Add Rules

Open `.gitignore` and add:

```id="3y0k3s"
temp.txt
*.log
```

Save.

---

## 🧩 Step 6: Check Status Again

```bash id="n8g6q1"
git status
```

👉 Observe:

* Files are now ignored (not shown)

---

## 🧩 Step 7: Stage and Commit `.gitignore`

```bash id="9a6l9k"
git add .gitignore
git commit -m "Added gitignore to exclude temp and log files"
```

---

## 🧩 Step 8: Push Changes

```bash id="1kqk9c"
git push origin main
```

---

# 🎤 TRAINER SCRIPT

---

### 🔹 Before Step 2

> “Not everything in your folder is important.”

> “Some files are temporary or system-generated.”

---

### 🔹 After `git status`

> “Git tries to track everything unless told otherwise.”

---

### 🔹 Before `.gitignore`

> “We need a way to tell Git what to ignore.”

---

### 🔹 After adding rules

> “Now Git will pretend these files don’t exist.”

---

### 🔹 Important teaching moment

> “This keeps your project clean and professional.”

---

# 🧠 CONCEPTS INTRODUCED

* `.gitignore`
* Pattern-based ignoring (`*.log`)
* Clean repositories
* Selective tracking

---

# 🔍 REFLECTION QUESTIONS + ANSWERS

---

## ❓ 1. What is `.gitignore`?

### ✅ Answer

> “It is a file where you specify which files Git should ignore.”

---

---

## ❓ 2. Why do we need it?

### ✅ Answer

> “To prevent unnecessary or temporary files from being tracked.”

---

---

## ❓ 3. Does `.gitignore` delete files?

### ✅ Answer

> “No. It only tells Git to ignore them.”

---

---

## ❓ 4. What happens if a file is already committed?

### ✅ Answer

> “`.gitignore` will NOT affect it.”

---

### 💡 Add

> “You must remove it from tracking manually first.”

---

---

## ❓ 5. What does `*.log` mean?

### ✅ Answer

> “It tells Git to ignore all files ending with `.log`.”

---

---

## ❓ 6. Can we ignore folders?

### ✅ Answer

> “Yes. You can specify folder names in `.gitignore`.”

---

---

## ❓ 7. Will ignored files appear in `git status`?

### ✅ Answer

> “No. Git hides them from tracking.”

---

---

# 🎯 END-OF-LAB TAKEAWAYS

Say:

> “A clean repository is a professional repository.”

> “You should only track what is meaningful.”

---

# 🔗 TRANSITION TO NEXT LAB

End with:

> “Now we can control what gets tracked…”

> “But how do we work with others on the same project?”

👉 Leads to:

**LAB 6: Collaboration (Working with Others)**

---

# 🧠 OPTIONAL ENHANCEMENT

Show real-world examples:

* Ignore `node_modules/`
* Ignore `.env`

---

# ⚠️ COMMON ISSUES

* Forgetting to save `.gitignore`
* Expecting `.gitignore` to remove already tracked files

---

# 🔥 TEACHING INSIGHT

This lab introduces **discipline and best practices**

---

# ✅ DONE

You now have:

* `.gitignore` lab
* Commands
* Script
* Q&A
* Flow

---

