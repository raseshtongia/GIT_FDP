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

