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
