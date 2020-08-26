# Github Notes

## Deploying HTML, CSS and JS to gh-pages

Move your files into a folder (e.g. site)

Inside repository

```
npm install gh-pages --save-dev
```

Open package.json and add after "license"
```
"homepage": "https://kyletejuco.github.io/{github-repo-name}"
```

Within "scripts" add
```
"deploy": "gh-pages -d site"
```

Add a gitignore and add
```
node_modules
```

Make sure your repository is initialized
```
git init
git add .
git commit -m "first commit"
git remote add origin {github-repo-url.git}
git push -u origin master
```

Deploy
```
npm run deploy
```

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
git add .
git commit -m "first commit"
git remote add origin {github-repo-url.git}
git push -u origin master
```

Add a gitignore and add
```
node_modules
```

Predeploy and Deploy
```
npm run predeploy
npm run deploy
```