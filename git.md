# Create react app and push to remote git repo
```bash
# Step 1: Conecting to gitHub via SSH
# Step 2: Create a new react-app
npm init react-app [MY_APP]
cd [MY_APP]
# Step 3: Create git repo in github.com -> copy link https
# Step 4: In [MY_APP]
git init
git config --global user.name thien1892
git config --global user.email thien1892@gmail.com
git add .
git remote add origin [https://[...].git]
git commit -m "this is comment"
git push --force origin HEAD:main

# or
git init
git config --global user.name thien1892
git config --global user.email thien1892@gmail.com
git branch -M main
git remote add origin [https://[...].git]

git add .
git commit -m "initialize repos"
git push -u origin main
```

# Remove directory from Git
```bash
# Remove directory from Git and local
git rm -r one-of-the-directories // This deletes from filesystem
git commit . -m "Remove duplicated directory"
git push origin <your-git-branch> (typically 'master', but not always)

# Remove directory from Git but NOT local
git rm -r --cached myFolder

# delete a branch
git branch -d [NAME BRANCH]
```

