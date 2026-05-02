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
