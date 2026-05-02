Excellent—this is exactly the **capstone lab** your session needs.
This will simulate a *real-world academic collaboration workflow* using branches, PRs, and conflict resolution.

We’ll design this so it feels like:

> “Two faculties co-authoring a course document”

---

# 🔴 LAB 8: Collaborative Editing with Branches, PRs & Conflict Resolution

---

# 🎯 LAB OBJECTIVE

> “Understand how multiple people work on the same file using branches, pull requests, and how Git handles conflicts.”

---

# 🎯 REAL-WORLD CONTEXT

> “Two faculty members are co-creating a syllabus document.”

Both:

* Start from same base
* Work independently
* Modify the same section

👉 Result:

* Conflict during merge

---

# 💡 WHAT THIS LAB WILL ACHIEVE

Participants will:

* Work on separate branches
* Push branches to GitHub
* Create Pull Requests (PRs)
* Experience merge conflict
* Resolve conflict properly

---

# ⏱️ TIME: ~60 minutes

---

# 👥 SETUP

Form **pairs**:

* Person A
* Person B

👉 Both should already have access to same repo (from Lab 6)

---

# 🧪 STEP-BY-STEP INSTRUCTIONS

---

# 🧩 Step 1: Create Base File (Done by Person A)

In `main` branch:

Create `syllabus.md`

```markdown id="3x8l1t"
# Course: Data Structures

## Unit 1: Introduction
- Basics of Data Structures

## Unit 2: Arrays
- Array operations

## Unit 3: Linked Lists
- Types of Linked Lists
```

Then:

```bash id="2m2r4v"
git add syllabus.md
git commit -m "Added base syllabus"
git push origin main
```

---

# 🧩 Step 2: Person B Pulls Latest

```bash id="ps3m3t"
git pull origin main
```

---

# 🧩 Step 3: Create Separate Branches

### Person A:

```bash id="2df8yz"
git checkout -b improve-unit-1
```

### Person B:

```bash id="yt3dr1"
git checkout -b improve-unit-1-alt
```

---

# 🧩 Step 4: BOTH Modify SAME SECTION (Important)

---

### Person A edits:

```markdown id="3y6k6k"
## Unit 1: Introduction
- Basics of Data Structures
- Real-life examples
```

---

### Person B edits:

```markdown id="4y93a2"
## Unit 1: Introduction
- Basics of Data Structures
- Historical background
```

---

# 🧩 Step 5: Commit Changes

### Person A:

```bash id="r1q8p2"
git add syllabus.md
git commit -m "Added real-life examples to Unit 1"
git push origin improve-unit-1
```

---

### Person B:

```bash id="s6l9d1"
git add syllabus.md
git commit -m "Added historical background to Unit 1"
git push origin improve-unit-1-alt
```

---

# 🧩 Step 6: Create Pull Requests (on GitHub)

On GitHub:

---

### Person A:

* Create PR: `improve-unit-1 → main`
* Merge it (no conflict yet)

---

### Person B:

* Create PR: `improve-unit-1-alt → main`

👉 Now GitHub will show:
**⚠️ Conflict detected**

---

# 🧩 Step 7: Observe Conflict on GitHub

Show them:

* “This branch has conflicts”
* Cannot merge automatically

---

# 🧩 Step 8: Resolve Conflict LOCALLY (Recommended)

---

### Person B runs:

```bash id="z6r7k8"
git checkout improve-unit-1-alt
git pull origin main
```

👉 This will trigger conflict

---

# 🧩 Step 9: Open File and See Conflict

Inside `syllabus.md`:

```markdown id="fw8k2a"
<<<<<<< HEAD
- Historical background
=======
- Real-life examples
>>>>>>> main
```

---

# 🧩 Step 10: Resolve Conflict

Modify to:

```markdown id="6y2g6k"
## Unit 1: Introduction
- Basics of Data Structures
- Real-life examples
- Historical background
```

---

# 🧩 Step 11: Complete Merge

```bash id="h2j7m1"
git add syllabus.md
git commit -m "Resolved conflict by combining both contributions"
git push origin improve-unit-1-alt
```

---

# 🧩 Step 12: Merge PR on GitHub

Now:

* PR will be mergeable
* Click **Merge**

---

# 🎤 TRAINER SCRIPT

---

### 🔹 Before Branching

> “Both of you are working on the same syllabus—but independently.”

---

### 🔹 Before conflict

> “Let’s see what happens when two people edit the same content.”

---

### 🔹 When GitHub shows conflict

Pause.

Say:

> “This is real-world collaboration.”

---

### 🔹 While showing conflict markers

> “Git shows both versions—it never deletes anything.”

---

### 🔹 During resolution

> “You decide the final version—not Git.”

---

# 🧠 CONCEPTS INTRODUCED

* Branch-based collaboration
* Pull Requests (PRs)
* Merge conflicts
* Conflict resolution workflow

---

# 🔍 REFLECTION QUESTIONS + ANSWERS

---

## ❓ 1. Why did Person A’s PR merge without conflict?

### ✅ Answer

> “Because no conflicting changes existed at that time.”

---

---

## ❓ 2. Why did Person B face a conflict?

### ✅ Answer

> “Because the same part of the file was modified differently.”

---

---

## ❓ 3. Did Git lose any changes?

### ✅ Answer

> “No. Git preserved both versions.”

---

---

## ❓ 4. What is a Pull Request?

### ✅ Answer

> “A request to merge changes from one branch into another.”

---

---

## ❓ 5. Who resolves conflicts?

### ✅ Answer

> “The user decides the correct version.”

---

---

## ❓ 6. What is the safe workflow for collaboration?

### ✅ Answer

> “Create branch → Make changes → Push → PR → Merge”

---

---

## ❓ 7. How can conflicts be minimized?

### ✅ Answer

> “Pull frequently and avoid editing same sections simultaneously.”

---

---

# 🎯 END-OF-LAB TAKEAWAYS

Say:

> “Conflicts are not errors—they are decisions.”

> “Git ensures no work is lost during collaboration.”

---

# 🔥 TEACHING INSIGHT

This lab demonstrates:

> **Trust + Control + Collaboration**

---

# 🎉 FINAL IMPACT LINE

End with:

> “Now imagine multiple faculty building a syllabus together…”

Pause.

> “This is how it can be done—cleanly and safely.”

---

# ✅ COMPLETE

You now have:

* Full collaboration + PR lab
* Real conflict simulation
* GitHub + local resolution
* Strong narrative

---

# 🚀 If You Want Next Level

We can:

* Add **visual diagrams of branching + PR flow**
* Create a **Git cheat sheet PDF**
* Design a **post-workshop assignment for faculty**

Just tell me 👍
