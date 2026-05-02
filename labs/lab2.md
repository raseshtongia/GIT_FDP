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
