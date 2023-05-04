# About

This repo is to test deploying default create-react-app on Github. <br>
Hosted Github site can be accessed here: http://bklimey.github.io/react-deploy-gh

Based on:
1. https://blog.logrocket.com/deploying-react-apps-github-pages/
2. https://www.youtube.com/watch?v=Q9n2mLqXFpU

# Instructions
> Note: Assuming Node.js and git are already installed
1. On local machine, create a new react project using <br>
`npx create-react-app "react-deploy-gh"` (`"react-deploy-gh"` can be other name)
2. Nagivate into folder <br>
`cd react-deploy-gh`
3. Setup Git for project <br>
`git init`
4. Create new empty repo called `react-deploy-gh` (can be other name) in Github
5. Commit and push local repo to Github
```
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/bklimey/react-deploy-gh.git
git push -u origin main
```
> `bklimey` should be your Github username and `react-deploy-gh` should be your repo name
6. Install `gh-pages` using <br>
`npm install gh-pages --save-dev`
7. Update `package.json` by adding <br>
`"homepage": "http://bklimey.github.io/react-deploy-gh",`
![image](https://user-images.githubusercontent.com/79616664/236174348-c48f786b-ef28-4615-85c2-d96950f1878a.png)
and <br>
`"predeploy": "npm run build",` <br>
`"deploy": "gh-pages -d build",` <br>
![image](https://user-images.githubusercontent.com/79616664/236174424-50565099-1eef-4918-b246-cb586a6626b7.png)
8. Push change to Github
9. Deploy app using <br>
`npm run deploy`
10. Website can now be viewed at http://bklimey.github.io/react-deploy-gh
