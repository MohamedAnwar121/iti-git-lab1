**Name:** Mohamed Abdelrahman Anwar

---

### Phase 1: Initial Setup and 4 Commits

```bash
# Create the file and add initial content
echo "print('Hello')" > app.py
git add app.py
git commit -m "Added app.py"

# Add Line 2
echo "print('Line 2')" >> app.py
git commit -am "Added Line 2 print"

# Add Line 3
echo "print('Line 3')" >> app.py
git commit -am "Added Line 3 print"

# Add Line 4
echo "print('Line 4')" >> app.py
git commit -am "Added Line 4 print"

```

### Phase 2: Delete Last 2 Commits

```bash
# Hard reset to remove the last two commits from history
git reset --hard HEAD~2

```

### Phase 3: New Commit After Deletion

```bash
# Add new logic and commit it
echo "print('New logic')" >> app.py
git add app.py
git commit -m "commit after deletion"

```

### Phase 4: Amend to "finish"

```bash
# Add 'lab Done' to the file
echo "# lab Done" >> app.py

# Update the previous commit with the new content and a new message
git add app.py
git commit --amend -m "finish"

```

### Phase 5: Revert and Push

```bash
# Create a new commit that undoes the last 3 commits
git revert HEAD~3..HEAD

# Push the final history to the remote repository
git push -u origin main

```

---
