Perfect—this is where everything comes together.

If Lab 3 was the **“aha moment”**, Lab 4 is the **“real-world usefulness moment.”**

---

# 🟠 LAB 4: Combining Work Using Merge

---

# 🎯 LAB OBJECTIVE

> “Learn how to bring changes from one branch into another and understand how Git handles conflicts.”

---

# 🎯 PROBLEM WE ARE SOLVING

Faculty often:

* Create multiple versions of content
* Struggle to combine them
* Lose changes while merging manually
* Overwrite each other’s work

---

# 💡 WHAT THIS LAB WILL ACHIEVE

By the end, participants will:

* Merge one branch into another
* Understand what a merge does
* Experience and resolve a conflict
* Gain confidence in combining work

---

# ⏱️ TIME: ~40–50 minutes

---

# 🧪 STEP-BY-STEP INSTRUCTIONS (FOR PARTICIPANTS)

---

## 🧩 Step 1: Ensure You Are in Your Repo

```bash
cd my-academic-profile
```

---

## 🧩 Step 2: Switch to Main Branch

```bash
git checkout main
```

---

## 🧩 Step 3: Merge Your Branch

```bash
git merge improve-bio
```

---

## 🧩 Step 4: Verify Changes

Open `bio.md`

👉 You should now see:

* Achievements section added

---

## 🧩 Step 5: Push Changes

```bash
git push origin main
```

---

# ⚠️ NOW WE CREATE A CONFLICT (IMPORTANT PART)

---

## 🧩 Step 6: Switch Back to Branch

```bash
git checkout improve-bio
```

---

## 🧩 Step 7: Modify Same Section

Edit `bio.md`

Change:

```markdown
## Contact
email@example.com
```

To:

```markdown
## Contact
faculty@university.edu
```

Save.

---

## 🧩 Step 8: Commit Change

```bash
git add bio.md
git commit -m "Updated contact email in branch"
```

---

## 🧩 Step 9: Switch to Main

```bash
git checkout main
```

---

## 🧩 Step 10: Modify SAME LINE in Main

Edit `bio.md`

Change:

```markdown
## Contact
email@example.com
```

To:

```markdown
## Contact
contact@college.edu
```

Save.

---

## 🧩 Step 11: Commit Change

```bash
git add bio.md
git commit -m "Updated contact email in main"
```

---

## 🧩 Step 12: Try Merging Again

```bash
git merge improve-bio
```

👉 You will see:
**MERGE CONFLICT**

---

## 🧩 Step 13: Open File and Resolve Conflict

You will see something like:

```markdown
<<<<<<< HEAD
contact@college.edu
=======
faculty@university.edu
>>>>>>> improve-bio
```

---

### Fix it manually:

```markdown
## Contact
faculty@university.edu
```

(or choose one or combine)

---

## 🧩 Step 14: Stage Resolved File

```bash
git add bio.md
```

---

## 🧩 Step 15: Complete Merge

```bash
git commit -m "Resolved merge conflict in contact section"
```

---

## 🧩 Step 16: Push Final Version

```bash
git push origin main
```

---

# 🎤 TRAINER SCRIPT

---

### 🔹 Before First Merge

> “We created a separate version earlier.”

> “Now we want to bring those changes back into the main version.”

---

### 🔹 After Merge

> “Git automatically combined your work.”

---

### 🔹 Before Conflict Simulation

> “Now let’s simulate a real-world situation.”

> “Two people edit the same part of a document.”

---

### 🔹 After Conflict Appears

Pause.

Say:

> “This is NOT an error. This is Git asking for your decision.”

---

### 🔹 While Resolving

> “Git never assumes—it lets you decide what is correct.”

---

### 🔹 After Resolution

> “You have successfully merged conflicting changes.”

---

# 🧠 CONCEPTS INTRODUCED

* Merge
* Automatic merge
* Merge conflict
* Conflict resolution
* Safe combination of work

---

# 🔍 REFLECTION QUESTIONS + ANSWERS

---

## ❓ 1. What does `git merge` do?

### ✅ Answer

> “It combines changes from one branch into another.”

---

---

## ❓ 2. Why did the first merge not create a conflict?

### ✅ Answer

> “Because the changes were in different parts of the file.”

---

---

## ❓ 3. Why did the second merge create a conflict?

### ✅ Answer

> “Because both branches modified the same part of the file.”

---

---

## ❓ 4. Did Git lose any data during conflict?

### ✅ Answer

> “No. Git preserved both versions and asked you to choose.”

---

---

## ❓ 5. Who resolves the conflict?

### ✅ Answer

> “The user (you) decides which version is correct.”

---

---

## ❓ 6. Is conflict bad?

### ✅ Answer

> “No. It’s a normal part of collaboration.”

---

---

## ❓ 7. What happens after resolving and committing?

### ✅ Answer

> “The branches are successfully merged into one consistent version.”

---

---

# 🎯 END-OF-LAB TAKEAWAYS

Say:

> “Git does not overwrite work blindly.”

> “It helps you safely combine changes—even when there is conflict.”

---

# 🔗 TRANSITION TO NEXT LAB

End with:

> “Now we can experiment and combine work…”

> “But sometimes we don’t want to track every file in our project.”

👉 Leads to:

**LAB 5: Using .gitignore**

---

# 🧠 OPTIONAL ENHANCEMENT

Show visual:

```bash
git log --oneline --graph
```

👉 Helps them see branch merge graph

---

# ⚠️ COMMON ISSUES

* Forgetting to resolve conflict fully
* Not staging after resolving
* Confusion seeing conflict markers

👉 Walk slowly here

---

# 🔥 TEACHING INSIGHT

This lab builds **trust in Git**

Before:

> “Git might overwrite my work”

After:

> “Git protects my work”

---

# ✅ DONE

You now have:

* Merge lab
* Conflict simulation
* Commands
* Script
* Q&A
* Flow

---

