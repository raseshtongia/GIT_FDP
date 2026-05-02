Perfect—here is your **complete, ready-to-run Lab 1**. You can literally conduct the session from this.

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

# 🎤 TRAINER SCRIPT (WHAT YOU SAY DURING THE LAB)

---

### 🔹 Before Step 1

> “We are creating your academic workspace online.”

> “Think of this as your personal academic folder—but smarter.”

---

### 🔹 After Clone

> “Now your project exists in two places:
>
> * On GitHub (remote)
> * On your system (local)”

---

### 🔹 Before `git status`

> “Let’s ask Git—what does it see right now?”

---

### 🔹 Before `git add`

> “Git does NOT automatically track everything.”

> “You must tell it what you want to include.”

---

### 🔹 Explain Staging

> “`git add` moves your changes into a staging area.”

Analogy:

> “It’s like selecting items before checkout.”

---

### 🔹 Before Commit

> “Commit is like saving a snapshot of your work.”

---

### 🔹 Before Push

> “Right now, your work is only on your system.”

> “Push sends it to GitHub—so it’s saved and shareable.”

---

### 🔹 After Push

> “Now your work is online—this is your academic space.”

---

# 🧠 CONCEPTS INTRODUCED

* Repository
* Local vs Remote
* Clone
* Working directory
* Staging area (`git add`)
* Commit
* Push

---

# 🔍 REFLECTION QUESTIONS (ASK PARTICIPANTS)

---

## ❓ 1. Where can you see your file online?

### ✅ Answer

> “On your repository page on GitHub.
> Once you pushed, GitHub now has a copy of your work.”

---

---

## ❓ 2. What happens if your system crashes?

### ✅ Answer

> “Your work is safe—as long as you pushed it to GitHub.”

> “You can clone it again anytime.”

---

### ⚠️ Important addition

> “If you didn’t push, those changes are only on your system and can be lost.”

---

---

## ❓ 3. What did `git add` actually do?

### ✅ Answer

> “It told Git which changes to include in the next commit.”

---

### 💡 Add

> “It moved your file from working area → staging area.”

---

---

## ❓ 4. Why do we need both commit and push?

### ✅ Answer

> “Commit saves locally. Push uploads to GitHub.”

---

---

## ❓ 5. What happens if we skip `git add`?

### ✅ Answer

> “Git will not include that file in the commit.”

---

# 🎯 END-OF-LAB TAKEAWAYS

Say this clearly:

> “You have now created your academic repository.”

> “You have saved your work in a structured way.”

> “And you have backed it up online.”

---

# 🔗 TRANSITION TO NEXT LAB

End with:

> “Now we saved one version…”

> “But what happens when you update your profile again?”

👉 Leads naturally to:

**LAB 2: Tracking Changes Over Time**

---

# 🧠 OPTIONAL ENHANCEMENT (IF TIME)

Ask them to:

* Add one more section (e.g., Research Interests)
* Repeat add → commit → push

👉 Reinforces learning

---

# ✅ DONE

You now have:

* Complete lab sheet
* Commands
* Teaching script
* Q&A
* Flow

---


# 🧠 1. Best Analogy for Local → Stage → Commit → Push → Remote

You want **one analogy that maps everything cleanly**. The best one I’ve seen work for non-technical audiences is:

## 🛒 “Shopping + Warehouse” Analogy

### 🏠 Local (Your Working Directory)

> Your home or workspace where you prepare items

* You edit files here
* Nothing is saved officially yet

---

### 🧺 Staging Area (`git add`)

> Your shopping basket

* You pick what you want to include
* You can add/remove items before checkout

👉 Key idea:

> “You are selecting what goes into the next version”

---

### 🧾 Commit

> Billing / invoice (final purchase record)

* A snapshot is created
* Stored locally
* Permanent record of what you selected

👉 Key idea:

> “This is your official saved version”

---

### 🚚 Push

> Sending items to a warehouse

* You upload your commits
* Now they are stored safely elsewhere

---

### 🏢 Remote (GitHub)

> Central warehouse (shared + backed up)

* Accessible from anywhere
* Others can collaborate

---

### 🎯 One-line summary you can say:

> “Work at home → select items → save a snapshot → send it to the cloud”

---

# 🧠 2. Does Commit Survive a System Crash?

Short answer: **No, not by itself**

---

## ✅ Truth:

> A commit is saved locally, but if your system is lost, that commit is lost too.

---

## 💡 So what’s the difference?

### `git add`

* Temporary
* Prepares changes
* Can be changed easily

---

### `git commit`

* Permanent (within your local repo)
* Creates a version in history

---

### 🚨 But BOTH are local

Only after:

```bash
git push
```

👉 your work becomes:

* backed up
* recoverable

---

## 🎯 Best way to explain:

> “Commit protects you from mistakes.
> Push protects you from losing your system.”

---

# 🧠 3. Undoing `git add` + Multiple Files

These are practical questions—they *will* come up.

---

## ❓ Undo `git add` (unstage a file)

```bash
git restore --staged filename
```

👉 Example:

```bash
git restore --staged bio.md
```

---

## ❓ Add multiple files

### Option 1: Add all files

```bash
git add .
```

---

### Option 2: Add specific files

```bash
git add file1.md file2.md
```

---

## ❓ Unstage multiple files

### All files:

```bash
git restore --staged .
```

---

### Specific files:

```bash
git restore --staged file1.md file2.md
```

---

## 🎯 Teaching Tip

Say:

> “Staging is reversible. Commit is not easily reversible.”

---

# 🧠 4. Why “master” → “main”?

This is less technical, more historical/social—but worth knowing.

---

## ✅ Short Answer

> The default branch name changed from “master” to “main” to use more inclusive and neutral terminology.

---

## 💡 Context

Earlier:

* “master” was default branch name

Later:

* Many communities moved toward inclusive language
* “main” became the standard

Platforms like GitHub adopted this change

---

## 🎯 What you should say in session:

> “Earlier, the default branch was called ‘master’. Now it is ‘main’. Functionally, nothing has changed—it’s just a name.”

---

# 🧠 Bonus Insight (Very Useful)

## ❓ Why does Git even have staging?

This is a hidden but powerful concept.

---

### Without staging:

* Every change gets committed automatically
* No control

---

### With staging:

You can:

* commit only selected changes
* organize commits cleanly

---

### 🎯 Best line to say:

> “Staging gives you control over what goes into each version.”

---

# 🧠 Final Summary (You Can Use This Verbally)

> “Git works in layers:
>
> * You make changes locally
> * You select what to include
> * You save a version
> * You upload it for safety and sharing”

---
