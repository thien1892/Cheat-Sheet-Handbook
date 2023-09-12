# Insall Node and NPM
```bash
# link: https://www.coursera.org/learn/react-basics/resources/FTd5h
sudo apt update
sudo apt install nodejs 
# veryfy
node --version && npm --version
```

# Create an app in react
```bash
# update: npm install react-scripts@latest
# link: https://create-react-app.dev/
npx create-react-app my-app
#or: npm init react-app my-app
cd my-app
npm start
```

# Some cml use in WSL
```bash
# cd to Downloads
cd /mnt/c/Users/thien1892/Downloads
# zip exclude subfolder
zip -r file_4.zip projects-final-portfolio/ -x projects-final-portfolio/node_modules/**\*
# install packet.json
npm install
```
# Create react app and push to remote git repo
```bash
# Step 1: Conecting to gitHub via SSH
# Step 2: Create a new react-app
npm init react-app [MY_APP]
cd [MY_APP]
# Step 3: Create git repo in github.com -> copy link https
# Step 4: In [MY_APP]
git init
git add .
git remote add origin [https://[...].git]
git commit -m "this is comment"
git push --force origin HEAD:main
```

# Use react-router
```javascript
// Step1: install react-router-dom:
npm i react-router-dom --save
// Step2: in file ./src/index.js
import {BrowerRouter} from "react-router-dom";
root.render(
  <BrowserRouter>
    <App />
  </BrowserRouter>
);
// Step3: in file ./src/App.js
import { Routes, Route, Link} from 'react-router-dom';
import Homepage from "./Homepage" //this is file another view
//This code in a comonent App
<nav>
    <Link to="/">HomePage</Link>
</nav>
<Routes>
    <Route path='/' element = {<HomePage/>}/>
</Routes>
```