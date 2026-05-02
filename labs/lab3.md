Great—now we move to the **most important “aha” moment in Git**.

This is where people go from:

> “Git is a saving tool”
> to
> “Git lets me experiment safely”

---

# 🟡 LAB 3: Safe Experimentation Using Branches

---

# 🎯 LAB OBJECTIVE

> “Learn how to create a separate version of your work, make changes safely, and switch between versions.”

---

# 🎯 PROBLEM WE ARE SOLVING

Faculty often:

* Want to try a new syllabus / teaching method
* Are afraid of breaking existing content
* End up duplicating files like:

  * `syllabus_new.docx`
  * `syllabus_experiment_final.docx`

---

# 💡 WHAT THIS LAB WILL ACHIEVE

By the end, participants will:

* Understand what a branch is
* Create and switch branches
* Make changes in isolation
* Switch between versions safely

---

# ⏱️ TIME: ~35–45 minutes

---

# 🧪 STEP-BY-STEP INSTRUCTIONS (FOR PARTICIPANTS)

---

## 🧩 Step 1: Ensure You Are in Your Repo

```bash
cd my-academic-profile
```

---

## 🧩 Step 2: Check Current Branch

```bash
git branch
```

👉 You should see:

```
* main
```

---

## 🧩 Step 3: Create a New Branch

```bash
git branch improve-bio
```

---

## 🧩 Step 4: Switch to New Branch

```bash
git checkout improve-bio
```

---

## 🧩 Step 5: Verify Branch Switch

```bash
git branch
```

👉 Now you should see:

```
* improve-bio
  main
```

---

## 🧩 Step 6: Modify Your Bio

Open `bio.md` and update:

```markdown
## Achievements
- Published 3 research papers
- Received teaching excellence award
```

Save the file.

---

## 🧩 Step 7: Stage and Commit

```bash
git add bio.md
git commit -m "Added achievements section"
```

---

## 🧩 Step 8: Switch Back to Main

```bash
git checkout main
```

---

## 🧩 Step 9: Observe the File

Open `bio.md`

👉 Notice:

* **Achievements section is NOT there**

---

## 🧩 Step 10: Switch Back to Branch

```bash
git checkout improve-bio
```

👉 Now:

* Achievements section is back

---

# 🎤 TRAINER SCRIPT

---

### 🔹 Before Branch Creation

> “Right now, you have only one version of your work.”

> “What if you want to experiment without disturbing it?”

---

### 🔹 Introduce Branch

> “A branch is a separate line of work.”

> “It allows you to try changes safely.”

---

### 🔹 After Switching Branch

> “You are now working in a parallel version of your project.”

---

### 🔹 Before switching back to main

> “Let’s go back to the original version.”

---

### 🔹 After switching

Pause.

Ask:

> “Where did your changes go?”

---

Then say:

> “They are not lost—they exist in the other branch.”

---

### 🔹 After switching back again

> “Git lets you move between versions instantly.”

---

# 🧠 CONCEPTS INTRODUCED

* Branch
* Branch creation
* Branch switching
* Parallel development
* Isolation of changes

---

# 🔍 REFLECTION QUESTIONS + ANSWERS

---

## ❓ 1. What is a branch?

### ✅ Answer

> “A branch is a separate version of your project where you can work independently.”

---

---

## ❓ 2. Did Git create a copy of all files when we created a branch?

### ✅ Answer

> “No. Git does not duplicate everything—it uses a smart reference system.”

---

### 💡 Add

> “Branches are lightweight and efficient.”

---

---

## ❓ 3. Why didn’t we see changes in main?

### ✅ Answer

> “Because those changes were made in a different branch.”

---

---

## ❓ 4. Are changes lost when we switch branches?

### ✅ Answer

> “No. They are preserved in the branch where they were made.”

---

---

## ❓ 5. Why is branching useful?

### ✅ Answer

> “It allows safe experimentation without affecting the main version.”

---

---

## ❓ 6. Can multiple people work using branches?

### ✅ Answer

> “Yes. Each person can work on their own branch and later combine changes.”

---

---

# 🎯 END-OF-LAB TAKEAWAYS

Say:

> “You no longer need multiple files for experiments.”

> “You can maintain clean versions inside one project.”

---

# 🔗 TRANSITION TO NEXT LAB

End with:

> “Now we can create separate versions…”

> “But how do we combine them back into the main version?”

👉 Leads to:

**LAB 4: Merge (Combining Work)**

---

# 🧠 OPTIONAL ENHANCEMENT

Teach shortcut:

```bash
git checkout -b new-branch-name
```

👉 Creates + switches in one step

---

# ⚠️ COMMON ISSUES

* Forgot to commit before switching
* Editing wrong branch
* Confusion about current branch

👉 Always remind:

```bash
git branch
```

---

# 🔥 TEACHING INSIGHT

This is the **“magic moment” lab**

If they understand this:
👉 Git suddenly becomes powerful, not confusing

---

# ✅ DONE

You now have:

* Full branching lab
* Commands
* Script
* Q&A
* Flow

---

