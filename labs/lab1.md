---

# 🟢 LAB 1: Create My Academic Space

---

# 🎯 LAB OBJECTIVE

> “Create your academic profile repository, bring it to your system, and save your first version of work.”

---

# 🎯 PROBLEM WE ARE SOLVING

Faculty today:

* Don’t have a structured place for academic content
* Maintain files locally without backup
* Lose track of versions

---

# 💡 WHAT THIS LAB WILL ACHIEVE

By the end of this lab, participants will:

* Have their own repository on GitHub
* Understand local vs remote
* Learn how to save work using Git
* Understand staging (`git add`) and commit

---

# ⏱️ TIME: ~35–45 minutes

---

# 🧪 STEP-BY-STEP INSTRUCTIONS (FOR PARTICIPANTS)

---

## 🧩 Step 0: Create Repository on GitHub

1. Go to GitHub
2. Click **New Repository**
3. Enter:

   * Repository name: `my-academic-profile`
4. Select:

   * ✅ Add a README file
   * ❌ Do NOT add `.gitignore`
5. Click **Create Repository**

---

## 🧩 Step 1: Clone Repository to Your System

Open terminal / VS Code terminal and run:

```bash
git clone https://github.com/<your-username>/my-academic-profile.git
cd my-academic-profile
```

---

## 🧩 Step 2: Open Folder in VS Code

```bash
code .
```

(Or open manually)

---

## 🧩 Step 3: Create Your Bio File

Create a file named `bio.md`

Add content like:

```markdown
# My Academic Profile

## Name
Your Name

## Department
Your Department

## Courses Taught
- Course 1
- Course 2
```

Save the file.

---

## 🧩 Step 4: Check Git Status

```bash
git status
```

👉 Observe:

* `bio.md` is **untracked**

---

## 🧩 Step 5: Stage the File

```bash
git add bio.md
```

---

## 🧩 Step 6: Verify Staging

```bash
git status
```

👉 Now it should show:

* “Changes to be committed”

---

## 🧩 Step 7: Commit Your Changes

```bash
git commit -m "Added my academic bio"
```

---

## 🧩 Step 8: Push to GitHub

```bash
git push origin main
```

---

## 🧩 Step 9: Verify on GitHub

* Open your repository on GitHub
* Confirm:

  * `bio.md` is visible
  * Commit message is visible

---

