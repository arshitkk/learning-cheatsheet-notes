# **GitHub Push Cheatsheet**

## **Index (Table of Contents)**

1. [Push a Directory/File for the First Time](#1-push-a-directoryfile-for-the-first-time)
2. [Update for Later Changes](#2-update-for-later-changes)
3. [Open Source Contribution](#3-open-source-contribution) (To be filled later)

---

## **1. Push a Directory/File for the First Time**

To push a directory or files to GitHub for the first time, follow these steps:

### **Step 1:** Initialize Git Repository

```bash
git init
```

### **Step 2:** Add Files or Directories

To add all files:

```bash
git add .
```

To add a specific file:

```bash
git add <file_name>
```

### **Step 3:** Commit Changes

```bash
git commit -m "Your commit message"
```

(Here, `-m` Stands for "message", and is used to provide a commit message.)

### **Step 4:** Set Remote Repository

```bash
git remote add origin <repository_URL>
```

Replace `<repository_URL>` with your GitHub repository URL.

```bash
git remote add origin https://github.com/username/repository-name.git
```

### **Step 5:** Push to GitHub

```bash
git push -u origin main
```

( Here, `-u` Stands for "upstream". This sets the remote repository (origin) and branch (main) as the default for future push and pull commands.)

---

## **2. Update for Later Changes**

### **Step 1:** Add Changes

```bash
git add .
```

### **Step 2:** Commit Changes

```bash
git commit -m "Updated message"
```

### **Step 3:** Push Changes

```bash
git push origin main
```

### **Step 4 (Optional):** If Errors

- If the remote repository has changes, you might need to pull them before pushing:

  ```bash
  git pull origin main --allow-unrelated-histories
  ```

- Force Push (`Optional`, **USE WIth CAUTION 💀**):

  If you want to overwrite remote changes with your local changes (force push):

  ```bash
  git push -f origin main
  ```

  *(resolve any conflicts, commit, and push again.)*

---

## **3. Open Source Contribution**

(To be filled later)

---

This structure now includes a table of contents with links to each section. You can fill in section 3 with details when needed. Let me know if you need any modifications!
