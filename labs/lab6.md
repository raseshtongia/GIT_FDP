Excellent—this is where your session becomes *social and engaging*.
Till now, they’ve worked individually. Now they experience:

> **“Git is not just for me—it’s for working together.”**

---

# 🔵 LAB 6: Collaboration – Working with Other Faculty

---

# 🎯 LAB OBJECTIVE

> “Learn how multiple people can work on the same project without overwriting each other’s work.”

---

# 🎯 PROBLEM WE ARE SOLVING

Faculty today:

* Share files over email/WhatsApp
* Overwrite each other’s changes
* Lose track of who changed what

---

👉 Result:

* Confusion
* Duplicate work
* Errors

---

# 💡 WHAT THIS LAB WILL ACHIEVE

By the end, participants will:

* Collaborate on the same repository
* Pull changes made by others
* Push their own changes
* Understand basic collaboration workflow

---

# ⏱️ TIME: ~40–50 minutes

---

# 👥 SETUP (IMPORTANT)

Ask participants to:

* Form **pairs (2 people per group)**

Define:

* Person A
* Person B

---

# 🧪 STEP-BY-STEP INSTRUCTIONS (FOR PARTICIPANTS)

---

## 🧩 Step 1: Share Repository Access

### Person A:

* Go to repo on GitHub
* Settings → Collaborators
* Add Person B

### Person B:

* Accept invite

---

## 🧩 Step 2: Person B Clones Repo

```bash id="m5m9ph"
git clone https://github.com/<personA-username>/my-academic-profile.git
cd my-academic-profile
```

---

## 🧩 Step 3: Person A Makes Change

Person A:

* Open `bio.md`
* Add:

```markdown id="vpt7li"
## Courses Taught
- Data Structures
- Operating Systems
```

Then:

```bash id="j3rlb8"
git add bio.md
git commit -m "Added courses taught section"
git push origin main
```

---

## 🧩 Step 4: Person B Pulls Changes

```bash id="g0hksb"
git pull origin main
```

👉 Verify:

* New section appears

---

## 🧩 Step 5: Person B Makes Change

Add:

```markdown id="c5q1oz"
## Publications
- Paper 1
- Paper 2
```

Then:

```bash id="v2nb7r"
git add bio.md
git commit -m "Added publications section"
git push origin main
```

---

## 🧩 Step 6: Person A Pulls Changes

```bash id="54nd0u"
git pull origin main
```

👉 Verify:

* Publications section appears

---

# 🎤 TRAINER SCRIPT

---

### 🔹 Before Pairing

> “Now we simulate real collaboration.”

> “You are no longer working alone.”

---

### 🔹 Before Step 3

> “One person will make changes and publish them.”

---

### 🔹 Before Step 4

> “The second person will bring those changes into their system.”

---

### 🔹 Explain Pull

> “`git pull` = download + update your project”

---

### 🔹 Before Step 5

> “Now the second person contributes.”

---

### 🔹 Before Step 6

> “Now the first person syncs again.”

---

### 🔹 After completion

> “This is how real teams work every day.”

---

# 🧠 CONCEPTS INTRODUCED

* Collaboration
* Push and Pull
* Shared repository
* Synchronization

---

# 🔍 REFLECTION QUESTIONS + ANSWERS

---

## ❓ 1. What does `git pull` do?

### ✅ Answer

> “It downloads changes from the remote repository and updates your local project.”

---

---

## ❓ 2. Why didn’t Person B see Person A’s changes immediately?

### ✅ Answer

> “Because their local repository was not updated yet.”

---

---

## ❓ 3. What happens if we don’t pull before working?

### ✅ Answer

> “We may work on outdated files and create conflicts later.”

---

---

## ❓ 4. What does `git push` do?

### ✅ Answer

> “It uploads your commits to the remote repository.”

---

---

## ❓ 5. Can multiple people work on the same file?

### ✅ Answer

> “Yes, but they must synchronize regularly.”

---

---

## ❓ 6. What is the safe workflow?

### ✅ Answer

> “Pull → Make changes → Add → Commit → Push”

---

---

## ❓ 7. What happens if both people edit same line?

### ✅ Answer

> “Git will create a conflict that needs manual resolution.”

---

---

# 🎯 END-OF-LAB TAKEAWAYS

Say:

> “You no longer need to email files.”

> “You can collaborate in a structured and safe way.”

---

# 🔗 TRANSITION TO NEXT LAB

End with:

> “Now your work is collaborative…”

> “But how do we make it visible as a portfolio?”

👉 Leads to:

**LAB 7: Publish Your Work (GitHub + Portfolio)**

---

# 🧠 OPTIONAL ENHANCEMENT

Show commit history:

* Contributions from both users

👉 Reinforces collaboration visually

---

# ⚠️ COMMON ISSUES

* Forgot to pull before working
* Push rejected (needs pull first)
* Wrong repo URL

👉 Handle calmly

---

# 🔥 TEACHING INSIGHT

This lab creates:

> “Trust in Git for teamwork”

---

# ✅ DONE

You now have:

* Collaboration lab
* Pair activity
* Commands
* Script
* Q&A
* Flow

---

