# Web小説家診断

スマホ向けの静的診断ページです。`index.html` だけで動きます。

## GitHub Pagesで公開する手順

```bash
cd /Users/ishigakikatsuaki/web-novel-diagnosis
gh auth login -h github.com
git init
git add .
git commit -m "Add web novel diagnosis"
gh repo create web-novel-diagnosis --public --source=. --remote=origin --push
gh api -X POST repos/:owner/web-novel-diagnosis/pages -f source.branch=main -f source.path=/
```

公開URLは通常この形になります。

```text
https://<GitHubユーザー名>.github.io/web-novel-diagnosis/
```
