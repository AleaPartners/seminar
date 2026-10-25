# セミナーLP

セミナー申込用のランディングページ（静的HTML/CSS）です。ビルド不要で、そのままGitHub Pagesで公開できます。

## ファイル構成

```
seminar-lp/
├── index.html   … 本文（文言・日時・講師情報はここを編集）
├── style.css    … デザイン（色・フォントは :root の変数で調整）
├── images/      … 写真やQRコードを入れるフォルダ（任意で作成）
└── README.md
```

## 編集のポイント

- **文言の差し替え**：`index.html` の「ここに〜」と書かれた箇所を置き換えます。
- **色の変更**：`style.css` 冒頭の `:root` 内の値（`--gold` など）を変更します。
- **写真の追加**：`images/` に画像を入れ、`index.html` の `placeholder` の部分を
  `<img src="images/hero.jpg" alt="...">` に差し替えます。
- **申込リンク**：`index.html` の `<a class="btn" href="#">` の `#` を申込フォームのURLに変更します。

## GitHub Pagesで公開する手順

1. GitHubで新しいリポジトリを作成し、このフォルダの中身をpushします。
2. リポジトリの **Settings → Pages** を開きます。
3. **Source** を `Deploy from a branch`、**Branch** を `main` / `/ (root)` に設定して Save します。
4. 数分後、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます。

### コマンド例（初回）

```bash
cd seminar-lp
git init
git add .
git commit -m "Initial seminar LP"
git branch -M main
git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
git push -u origin main
```
