# 公開の仕方（日本語）
**公開に必要な5つのステップ**

1. githubでリポジトリを作る
1. 雛形をコピーして`yarn install`する
1. .env ファイルを修正する
1. deploy.sh を実行する
1. 公開するリポジトリでGithub Pagesを有効にする


## step1. githubでリポジトリを作る
github.comでリポジトリを作ってください。

## step2. 雛形をコピーして`yarn install`する
下記のコマンドをコピーして、プロジェクトのディレクトリ名を修正したのち、
これからプロジェクトを作るディレクトリでそれを実行してください。
```
git clone --depth=1 --branch=master git@github.com:fruitriin/VuePressOnGithubPageTemplate.git {your_project_dirname}
cd !$
rm -rf .git 
git init 
yarn install
```
やっていること:
- 新しいプロジェクトのディレクトリに雛形をコピー
- そこへ cd
- テンプレートの .git 履歴を削除
- git initしなおす
- VuePress他をインストール 


::: warning メモ
VuePressがyarnでのインストールが必須な間はyarnを使ってください。  
(webpack4に対応してないと依存解決ができない)
:::


## step3. .envファイルの修正
```bash
vi .env

```

```
# .env
GITHUB_USERNAME="exampleUser"
REPOSITORY="SampleRepository
```
`GITHUB_USERNAME` と `REPOSITORY` を先程作ったものに修正しましょう。


## 4. shellからデプロイ
```bash
bash deploy.sh
```
VuePressのビルドと`gh-pages`ブランチへのpushが始まります。
docsフォルダの下を修正して、サイトを更新したいときも同様に`deploy.sh`を実行してください。

!!! warning 注意
shではなくbashで実行する必要があります。
!!!

## 5. リポジトリの設定を変更してGitHub Pagesを有効にする
github.com上の先程pushした自分のリポジトリに移動して、リポジトリのsettingsページを開いてください。　　
**GitHub Pages section**まで移動して、セレクトボックスから `gh-branch` を選んで Save ボタンを押しましょう。

これで {yourname}.github.io/{repository}/ へのサイトの構築ができました！

## 付録.
### 作成したサイトだけじゃなくてプロジェクトも同じリポジトリで管理したい

git initが済んでいるので、リモートリポジトリを追加してpushすれば同じリポジトリで管理できます。

```
git remote origin git@github.com:{username}/{repository}.git 
git commit -m "VuePress Project" .
git push
```

*gh-pagesブランチはmasterブランチと別の.git履歴を持つことになります*

### VuePressの設定を修正したい

[公式ドキュメントはこちら](https://vuepress.vuejs.org/guide/basic-config.html)

### VuePressで使えるMarkdownについて
Markdown-itがVuePressでは使われています。  
また、いくつかのVuePress用の構文が追加されています。  
[VuePress \| Markdown Extensions](https://vuepress.vuejs.org/guide/markdown.html)を参照してください。


