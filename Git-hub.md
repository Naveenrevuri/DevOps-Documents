# Step 1: Create Git-hub account
## GitHub ki login avvu (www.github.com)
 1)Create New Repository
  . Repository name: eg. my-demo-project
  . Description: optional
  . Public or Private select cheyyi
  . Initialize with README (optional, local nunchi push cheyali ante clear untundi)
 'Cretae Repository Get URL, e.g.
 .https://github.com/<username>/my-demo-project.git

# Step 2: Ready Local Code
  ->Locatio of File Eg: cd my-demo-project
  -> CMD

# Step 3: Git init 
   ```bash
 git init
```
# Step-4: Add File
```bash
git add .
```
# Step-5:Commit Code
```bash
git commit -m "Initial commit"
```
# Step-6: Add Remote repository
```bash
git remote add origin https://github.com/<username>/my-demo-project.git
```
```bash
git remote -v
```

# Step 7: Push Local code ni GitHub 
```bash
git branch -M main
git push -u origin main
```
# Changes push
```bash
git add .
git commit -m "Your commit message"
git push
```

# Git Revert
 -> Remove Our changes from central Repo based on ID
 ```bash
  git revert
```

