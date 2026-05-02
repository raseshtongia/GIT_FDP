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

