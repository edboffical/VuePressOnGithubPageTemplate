# VuePress Template for Github Pages
![VuePress Template for Github Pages](./.resources/template_logo.png)

## Description in English
This is VuePress template for Github Pages.  
You can publish like [this site](https://fruitriin.github.io/vptest/) few minuts.   
Just you need these 5 steps!
 
 （日本語の説明はもうちょっと下にあります）
 
### 5 steps for publish
1. create your repo on github
1. git clone this template and yarn install
1. configure .env file
1. deploy into github
1. configure to enable Github Pages 

Then you publish your site!

More detail. [How To Deploy](/HowToDeploy/English.md)


### What changed from plane VuePress?
- some optimized deploy into github pages
- sidebar auto generation from file and directory under the docs   
(sorted from file and directory names.)
- and this documentation! 

### Requirements
- git
- write(push) permission to github from git command  
I think you can check `ssh git@github.com`
- yarn(not npm until VuePress need it) 
 
## 日本語の説明
VuePressをGithub Pagesで公開するための雛形です。
たった5つのステップで[こんなサイト](https://fruitriin.github.io/vptest/)を公開することができますよ！

### 公開のための5ステップ
1. githubでリポジトリを作る
1. 雛形をコピーして`yarn install`する
1. .env ファイルを修正する
1. deploy.sh を実行する
1. 公開するリポジトリでGithub Pagesを有効にする

これだけでページが公開できます！  
より詳しくは[How To Deploy（日本語）](/HowToDeploy/Japanese.md)をご覧ください。

### 何が違うの？
- github公開のためにちょっとだけ最適化してます
- サイドバーをdocs配下のファイル名とディレクトリ名から自動的に作ります。  
(ファイル名/ディレクトリ名でソートされます)
- そしてこのドキュメントがありますよ！

### 必要なもの
- git
- shell上からgitコマンドでgithubに書き込み（push）できること  
`ssh git@github.com` コマンドで確認することができると思います。
- yarn(VuePressが必要とする間はnpmではいけません) 

## Link
- [VuePress Official](https://vuepress.vuejs.org/)
- [fruitriin/VuePressOnGithubPageTemplate](https://github.com/fruitriin/VuePressOnGithubPageTemplate)

## License
MIT.

