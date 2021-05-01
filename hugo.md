---
title: "Hugo"
date: 2021-01-17T00:13:26-08:00
draft: true
---
# hugo installation, publish and matainance
*base on Mac OS*
### install hugo
- install brew
- use brew to install hugo
```
brew install hugo
```
- check version
```
hugo version
```
### generate website 
- generate your website folder
```
hugo new site myblog
```
### get a theme
- <https://themes.gohugo.io/>

### start site on local host
```
hugo server -t m10c -- buildDrafts
```
*m10c is the theme name*
- use "hugo server" to check local website later

### deploy on github page
- creat a new repository, the name must same as the user name + .github.io
- put all your local file into the pulic folder, all files in public folder are ready to be pushed to github repo
```
hugo --theme=m10c --baseUrl="https://jiliangli1997.github.io/" --buildDrafts
// in myblog 
```
- push public to repo first time
```
cd public 
git init
git add .
git commit -m "hugo"
git remote add origin https://github.com/jiliang1997/jiliangli1997.github.io.git
git push -u origin master
// under public 
```
- after first time, just need these for **update any change**
```
hugo --theme=m10c --baseUrl="https://jiliangli1997.github.io/" --buildDrafts
// in myblog 
cd public
git add .
git commit -m "hugo"
git push -u origin master
// under public 
```

### write a blog
```
hugo new post/name.md
```
