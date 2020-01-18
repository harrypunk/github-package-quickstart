# TLDR publish a package to github in 1min
1. A access token with ```read:packages``` and ```write:packages```.  
https://github.com/settings/tokens

2. Edit ```~/.npmrc```  
```
//npm.pkg.github.com/:_authToken=TOKEN
```
3. Edit ```package.json```, must use scope ```@```  
```json

{
  "name": "@harrypunk/github-package-quickstart",
  "repository": "https://github.com/harrypunk/github-package-quickstart",
  "publishConfig": { "registry": "https://npm.pkg.github.com/" }
}

```
4. Publish
```bash
npm publish
```
