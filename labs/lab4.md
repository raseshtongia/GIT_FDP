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
