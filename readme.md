# Github Notes

## Deploying a React App to gh-pages

Inside repository

```
npm install gh-pages --save-dev
```

Open package.json and add after "private"
```
"homepage": "https://kyletejuco.github.io/{github-repo-name}"
```

Within "scripts" add
```
"predeploy": "npm run build",
"deploy": "gh-pages -d build"
```

Make sure your repository is initialized
```
git init
git remote add origin {github-repo-url.git}
```

Predeploy and Deploy
```
npm run predeploy
npm run deploy
```