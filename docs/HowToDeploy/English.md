# how to deploy in English
**5 steps need for start to publish**

1. create your repo on github
1. git clone this template and yarn install
1. configure .env file
1. deploy into github
1. configure to enable Github Pages 


## step1. create repository to publish
Create your new repository on github.com

## step2. git clone this template and yarn install
just copy these lines and change project name.  
and then past your shell in your workspace.
```
git clone --depth=1 --branch=master git@github.com:fruitriin/VuePressOnGithubPageTemplate.git {your_project_dirname}
cd !$
rm -rf .git 
git init 
yarn install
```
these command do:
- clone from template into your new project directory
- cd to there
- remove template .git history
- git init
- install VuePress another 

::: warning Note
**You must need to use yarn until VuePress need it.**
:::


## step3. configure .env file
```bash
vi .env

```

```
# .env
GITHUB_USERNAME="exampleUser"
REPOSITORY="SampleRepository
```
change `GITHUB_USERNAME` and `REPOSITORY` to your own.


## 4. deploy from your shell
```bash
bash deploy.sh
```
It will start to build VuePress project and push it as gh-pages branch.
When you add/edit markdowns, need execute deploy.sh again to publish. 

::: warning Note
Need to use bash not sh
:::

## 5. configure your repository setting 
Move to your repository on github.com, and go setting.
And then, down to **GitHub Pages section.**
Select `gh-branch` and push save.

Finally, you publish into {yourname}.github.io/{repository}/ !

## Appendix.
### This Project(not only generate site) Also push same repository.

Already you did git init, so add remote repository and push, you can do it.

```
git remote origin git@github.com:{username}/{repository}.git 
git commit -m "VuePress Project" .
git push
```

These command push to project at first.(I think it push as master branch)
::: tip
`gh-pages` branch has another .git history in your repository.
:::
### How to more configure VuePress

[Official Document here](https://vuepress.vuejs.org/guide/basic-config.html)

### Markdown flavor in VuePress
Markdown-it use in VuePress.
Some Extension in VuePress, official document is here.  
[VuePress \| Markdown Extensions](https://vuepress.vuejs.org/guide/markdown.html)


