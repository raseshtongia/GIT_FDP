Here’s a **clear, no-nonsense step-by-step guide** to setting up SSH keys for Git (works perfectly with Git Bash on Windows).

---

# 🔑 1. Check if you already have SSH keys

In Git Bash:

```bash
ls ~/.ssh
```

If you see files like:

```bash
id_ed25519
id_ed25519.pub
```

you already have a key → you can reuse it (or create a new one anyway if you want clean separation).

---

# 🔐 2. Generate a new SSH key

Run:

```bash
ssh-keygen -t ed25519 -C "you@example.com"
```

### You’ll be prompted:

* **File location** → press Enter (default is fine)
* **Passphrase** → optional but recommended

This creates:

```bash
~/.ssh/id_ed25519
~/.ssh/id_ed25519.pub
```

---

# ▶️ 3. Start the SSH agent

```bash
eval "$(ssh-agent -s)"
```

---

# ➕ 4. Add your key to the agent

```bash
ssh-add ~/.ssh/id_ed25519
```

---

# 📋 5. Copy your public key

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the full output (starts with `ssh-ed25519`).

---

# 🌐 6. Add key to your Git platform

### For GitHub:

1. Go to Settings → SSH and GPG keys
2. Click **New SSH key**
3. Paste the key
4. Save

---

### For GitLab:

1. Preferences → SSH Keys
2. Paste key → Save

---

# 🧪 7. Test your connection

For GitHub:

```bash
ssh -T git@github.com
```

Expected:

```
Hi username! You've successfully authenticated...
```

---

# 🔁 8. Use SSH instead of HTTPS

When cloning, use:

```bash
git clone git@github.com:username/repo.git
```

NOT:

```bash
https://github.com/username/repo.git
```

---

# ⚙️ 9. (Optional but useful) SSH config file

Create/edit:

```bash
nano ~/.ssh/config
```

Example:

```ini
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519
```

---

# 🧠 Pro tips (worth knowing)

### ✅ Use different keys for work & personal

```bash
ssh-keygen -t ed25519 -C "work@example.com" -f ~/.ssh/id_ed25519_work
```

Then map via config:

```ini
Host github-work
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_work
```

---

### ✅ Persist SSH agent (Windows tip)

Git Bash doesn’t always remember keys after restart. You may need to re-run:

```bash
ssh-add ~/.ssh/id_ed25519
```

---

### ✅ Check loaded keys

```bash
ssh-add -l
```

---

## 🚨 Common mistakes

* Copying **private key** instead of `.pub`
* Using HTTPS instead of SSH
* Forgetting to start `ssh-agent`
* Wrong file permissions (rare on Windows, common on Linux)

---

## ✅ Minimal quick setup (if you want fast)

```bash
ssh-keygen -t ed25519 -C "you@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

→ paste into GitHub

---

If you want, I can also help you:

* set up **multiple GitHub accounts with SSH**
* or debug if your SSH connection fails (very common issue)
