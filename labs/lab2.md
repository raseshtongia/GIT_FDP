Perfect—this is where Git starts to *click* for most people.

Lab 1 gave them **“I can save”**
Lab 2 gives them **“I can track and understand changes over time”**

---

# 🟢 LAB 2: Track Changes Over Time

---

# 🎯 LAB OBJECTIVE

> “Understand how Git tracks changes and maintains history of your work.”

---

# 🎯 PROBLEM WE ARE SOLVING

Faculty often:

* Update documents repeatedly
* Forget what changed
* Cannot go back to previous versions
* Lose clarity on evolution of content

---

# 💡 WHAT THIS LAB WILL ACHIEVE

By the end, participants will:

* Make multiple versions of a file
* View commit history
* Understand how changes are tracked
* Appreciate commit messages

---

# ⏱️ TIME: ~30–40 minutes

---

# 🧪 STEP-BY-STEP INSTRUCTIONS (FOR PARTICIPANTS)

---

## 🧩 Step 1: Open Existing Repository

```bash
cd my-academic-profile
```

---

## 🧩 Step 2: Open `bio.md` and Update It

Add new sections:

```markdown
## Research Interests
- Artificial Intelligence
- Data Science

## Experience
- 5 years teaching experience
```

Save the file.

---

## 🧩 Step 3: Check Status

```bash
git status
```

👉 Observe:

* File is modified

---

## 🧩 Step 4: Stage the Changes

```bash
git add bio.md
```

---

## 🧩 Step 5: Commit Changes

```bash
git commit -m "Added research interests and experience"
```

---

## 🧩 Step 6: Make Another Change

Edit `bio.md` again:

Add:

```markdown
## Contact
email@example.com
```

Save.

---

## 🧩 Step 7: Repeat Process

```bash
git add bio.md
git commit -m "Added contact details"
```

---

## 🧩 Step 8: View History

```bash
git log
```

👉 Observe:

* Multiple commits
* Messages
* Author
* Time

---

## 🧩 Step 9: Push Changes

```bash
git push origin main
```

---

## 🧩 Step 10: View History on GitHub

* Open repo
* Click **Commits**
* Observe timeline

---

# 🎤 TRAINER SCRIPT

---

### 🔹 Before Step 2

> “In real life, your profile keeps evolving.”

> “Let’s simulate that evolution.”

---

### 🔹 Before `git status`

> “Let’s ask Git—what changed?”

---

### 🔹 After status

> “Git is tracking changes automatically—but not saving them yet.”

---

### 🔹 Before commit

> “Every commit is a checkpoint in your journey.”

---

### 🔹 After second commit

> “Now you don’t just have a file—you have a *history*.”

---

### 🔹 Before `git log`

> “Let’s see how Git remembers everything.”

---

### 🔹 While showing log

Explain:

* Commit ID
* Message
* Time

---

### 🔹 Before push

> “Let’s send this history to GitHub.”

---

# 🧠 CONCEPTS INTRODUCED

* File modification tracking
* Multiple commits
* Commit history
* Importance of commit messages

---

# 🔍 REFLECTION QUESTIONS + ANSWERS

---

## ❓ 1. What does Git store when we commit?

### ✅ Answer

> “Git stores a snapshot of your project at that point in time.”

---

### 💡 Add

> “It doesn’t just store the file—it stores the entire state of your project.”

---

---

## ❓ 2. Can we go back to an older version?

### ✅ Answer

> “Yes. Git keeps all previous commits, so you can return to any version.”

---

---

## ❓ 3. What is the purpose of commit messages?

### ✅ Answer

> “They describe what changed in that version.”

---

### 💡 Add

> “Good messages help you and others understand history later.”

---

---

## ❓ 4. What happens if we don’t commit regularly?

### ✅ Answer

> “You lose the ability to track changes clearly.”

---

### 💡 Add

> “Your history becomes unclear and harder to manage.”

---

---

## ❓ 5. What is the difference between file versioning vs Git?

### ✅ Answer

> “Manual versioning creates separate files.”

> “Git keeps everything in one place with structured history.”

---

---

## ❓ 6. Where is this history stored?

### ✅ Answer

> “Inside your repository (in the hidden `.git` folder).”

---

---

## ❓ 7. Can we see this history on GitHub?

### ✅ Answer

> “Yes. After pushing, GitHub shows your commit timeline.”

---

---

# 🎯 END-OF-LAB TAKEAWAYS

Say:

> “Now you are not just saving files—you are tracking their evolution.”

> “You can see what changed, when, and why.”

---

# 🔗 TRANSITION TO NEXT LAB

End with:

> “Now we can track changes…”

> “But what if you want to try something new without affecting your current version?”

👉 Leads to:

**LAB 3: Branching (Safe Experimentation)**

---

# 🧠 OPTIONAL ENHANCEMENT

Show:

```bash
git log --oneline
```

👉 Cleaner view → easier understanding

---

# ⚠️ COMMON ISSUES

* Forgot to save file
* Commit message typo
* Confusion between add/commit

---

# 🔥 TEACHING INSIGHT

This lab builds the **core mental shift**:

> From “files” → to “history of work”

---

# ✅ DONE

You now have:

* Full lab flow
* Commands
* Script
* Q&A
* Transition

---
